---
title: [Use the tsload service to load data]
last_updated: 6/2/2020
summary: "Learn how to load files using the tsload service."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
Another option for loading data in bulk, is to use the tsload service. The tsload service is a collection of APIs.

This page highlights the following:
- Setting up your cluster to use the tsload service
- Using the reference client for writing automated ETL jobs
- Server and authentication details
- API workflow inside the client

## Setting up your cluster

1. SSH as admin into your ThoughtSpot cluster: `ssh admin@<cluster-ip-address or hostname>`.

2. Open the config file at the following location:
   `/usr/local/scaligent/release/production/orion/etl_http_server/prod.config`  

3. If your cluster is behind a load balancer, you must disable the internal etl server's load balancer. Contact ThoughtSpot support for assistance with this step.

4. By default, bad-records are saved in one of the mounted drives. If that is not possible, they are saved to `/tmp`. To modify this location, contact ThoughtSpot support.

5. If your cluster has been upgraded from an earlier version, validate that your SSL certificates are bound to the service. Contact ThoughtSpot support for assistance with this step.

   {% include note.html content="For clusters created in version 6.2 or later, certificates are bound to the service by default." %}

6. Check if the **etl_http_server**, responsible for the tsload service, is accessible by pinging it:
   ```
   curl -i https://localhost:8442/ts_dataservice/v1/public/ping
   HTTP/1.1 200 OK

   Ping Received.
   ```    

## Reference client

The included Python3 client is provided for you to use it as a starting point for writing automated ETL jobs in Python.

A reference python client is located at: <todo-Anand to send the link>
This requires python3 and the details of the methods are documented within the above client.

The client includes the following methods:
- **login**: Requires ThoughtSpot username and password
- **startLoad**: Prepares the load with parameters that include table, schema, and db. It also includes tokenizing parameters, like : field separator etc.
  - This returns a new IP address (when the internal load balancer is enabled)
  - This also returns a `cycle_id`. This `cycle_id` determines the load-session corresponding to the given load parameters. All the successive calls will need to use this cycle_id as a parameter, including the getStatus.
  - LoadDataParam JSON
    ```
  {
	"target": {
		"database": "mytest",
		"schema": "falcon_default_schema",
		"table": "one"
	},
	"format": {
		"date_time": {
			"date_format": "%Y%m%d",
			"time_format": "%H-%M-%S",
			"date_time_format": "%Y%m%d %H:%M",
			"converted_to_epoch": false,
			"second_fraction_start": ".",
			"skip_second_fraction": false
		},
		"boolean": {
			"true_format": "T",
			"false_format": "F",
			"use_bit_values": false
		},
		"type": "CSV",
		"field_separator": ",",
    "trailing_field_separator": true,
		"enclosing_character": "^",
		"escape_character": "^",
		"has_header_row": true,
		"null_value": “(null)”,
		"flexible": false
  	},
  	"load_options": {
  		"empty_target": true,
  		"max_ignored_rows": 10
  	}
  }
    ```
- **load**: in this example, a file is being uploaded in a single call. In reality, this could be a post-call with data directly instead of a file.
  - This can also be broken into multiple load calls for load data incrementally.
  - This simply uploads and starts processing the file, but the load is not complete just by calling this method.
  - This method returns immediately, and the actual parsing, etc is done asynchronously.
  - To get the status at any point, the **getStatus** method can be used.
- **commitLoad**: This method commits the current ingested data into the Falcon database.
  - This method returns immediately, and the commit is done asynchronously.
  - Again calling the **getStatus** method can provide the actual status.
- **getStatus**: Returns the status of the load at that time
  - **getStatus JSON**
    ```
    {
    	"buffered_data": "0 Bytes",
    	"cycle_id": "78aecb14-34c5-4da8-b08f-517de22d9701",
    	"end_time": "Mon, 08 Jun 2020 20:46:21 IST",
    	"ignored_row_count": "0",
    	"ingested_network_bw": "0 Bytes",
    	"internal_stage": "DONE",
    	"rows_written": "2",
    	"size_written": "34 Bytes",
    	"start_time": "Mon, 08 Jun 2020 20:46:19 IST",
    	"status": {
    		"code": "OK"
    	}
    }
    ```  

## Server and authentication details

### Ports and Server

Port number: 8442, HTTPS REST endpoints

{% include note.html content="Port 8442 is open by default in ThoughtSpot release 6.1 or later." %}

The load server resides on a different port compared to standard ThoughtSpot services. This is because the service tends to carry heavy file-load operations, and having a separate web server creates the needed isolation between standard ThoughtSpot services and tsload operations.

By default, this service runs on all nodes of a ThoughtSpot cluster. This provides load distribution to address possible simultaneous loads. The tsload server uses its own load balancer. If an external load balancer is used, the tsload requests must be sticky, and the tsload load balancer should be disabled.

### Authorization and Authentication

This uses the existing ThoughtSpot authentication mechanism to authenticate the user, using the **Login** API. Each upload session must be authenticated using this API.

tsload is available only to users who have the “Administrator” or “Manage Data” privilege in the ThoughtSpot environment.

## API workflow

The typical workflow of the API inside the client is the following:

1. `<standard-thoughspot-cluster-url> Login`.

2. `<standard-thoughspot-cluster-url> StartLoad`.
   If the tsload-LoadBalancer is turned on, this returns the new IP address (for one of the nodes in the cluster).

3. `<thoughtspot-node-ip-returned-from-2> Load`.
   1. Repeat this step until all the rows are sent.
   2. In the case of a file, you can call this in one operation. In the case of a stream, you call this multiple times, thus avoiding buffering large data on the client side.

4. `<thoughtspot-node-ip-returned-from-2> EndLoad`.
   1. This will start the commit process.
   2. It’ll take some time for the data to be committed to Falcon Database.

5. `<thoughtspot-node-ip-returned-from-2> GetStatus`.
   1. To monitor the state of the commit.
   2. Wait until it returns “DONE”.

## Related information

[tsload service API reference]({{ site.baseurl }}/reference/tsload-service-api-ref.html)   