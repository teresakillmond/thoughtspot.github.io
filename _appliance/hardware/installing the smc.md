---
title: [Installing the Super Micro Computer]
last_updated: [10/31/2019]
summary: "Learn how to install the Super Micro Computer (SMC) Appliance."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
{: id="Installation-Prerequisites"}
## Installation Prerequisites

Ensure that you have the following items, information, and understanding of policies before you proceed:

<table>
<tr>
<td>&#10063;</td>
<td>Appliance quick start guide, to locate IPMI and data network ports. See <a href="#step-1-connect-switches-to-10gbe-ports">Appliance Port Location</a>.</td></tr>

<tr>
<td>&#10063;</td>
<td>Data center with proper cooling</td></tr>

<tr>
<td>&#10063;</td>
<td>AC power</td></tr>

<tr>
<td>&#10063;</td>
<td>10GbE switch, with enabled IPv6 broadcast and multicast. You need one per node.</td></tr>
<tr>
<td>&#10063;</td>
<td>10GbE network cables, either direct attach copper (DAC) or fiber. Refer to <a href="#step-1-connect-switches-to-10gbe-ports">Step 1: Connect switches to 10GbE ports</a> for more information to decide between the two types.</td></tr>

<tr>
<td>&#10063;</td>
<td>100Mbps or 1Gbps switch for IPMI, for Out of Band Management. You need one per node.</td></tr>

<tr>
<td>&#10063;</td>
<td>Cat5 network cables</td></tr>

<tr>
<td>&#10063;</td>
<td>Rack space (2U or 3.5 inches per appliance) and power strip</td></tr>

<tr>
<td>&#10063;</td>
<td>Monitor and keyboard</td></tr>

<tr>
<td>&#10063;</td>
<td>10G connection: SFP+ for switch side</td></tr>

<tr>
<td>&#10063;</td>
<td>Networking information, for data, management IPs, DNS, timezone, and default gateway IP. Contact your network administrator for this information, and fill out the ThoughtSpot site survey so that you have a quick reference.</td></tr>

<tr>
<td>&#10063;</td>
<td>Network policies</td></tr>
</table>

See [Network policies]({{ site.baseurl }}/appliance/firewall-ports.html).

{: id="about-hardware"}
## About the Hardware
You can deploy ThoughtSpot on two different appliance hardware platforms: Haswell and Skylake. Both of the platforms provide the same performance. Refer to [Haswell and Skylake hardware details]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#hardware-details) for details on their physical differences.

{: id="hardware-details"}
| Details | Haswell | Skylake |
| --- | --- | --- |
| Dimensions | 2 RU chassis (17.25" x 3.47" x 28.5" (WxHxD)) | 2 RU chassis (17.6" x 3.47" x 28.75" (WxHxD)) |
| # of nodes | Populated with 1 to 4 nodes | Populated with 1 to 4 nodes |
| Node specifications | Each node is independent and consists of a server board (removable from rear), 1x 200GB SSD, 3x 2TB HDD | Each node is independent and consists of a server board (removable from rear), 1x 240GB SSD, 3x 2TB HDD |
| Max power consumption | 2000 W | 2200 W |
| Required power input | 200-240V / 11.8 - 9.8A / 50-60Hz | 220-240 VAC  50-60 Hz |

{: id="hardware-front-back-diagrams"}
### Hardware front and back view diagrams
These pictures show the front and back views of each appliance.

{: id="haswell-front-back"}
### Haswell Front View
![The front of the Haswell appliance]({{ site.baseurl }}/images/smc-haswell-front-view.png "The front of the Haswell appliance")

### Haswell Back View
![The back of the Haswell appliance]({{ site.baseurl }}/images/smc-haswell-back-view.png "The back of the Haswell appliance")

{% include note.html content="The nodes on the back are in a reverse N shape, with Node A at the bottom right and Node D at the top left." %}

{% include note.html content="The Haswell appliance shown here is not fully populated, as it only has three nodes. Your appliance may be populated with 1-4 nodes, depending on the ordered configuration. If you order less than four nodes, ThoughtSpot fills the empty slot with a filler panel." %}

{: id="skylake-front-back"}
### Skylake Front View
![The front of the Skylake appliance]({{ site.baseurl }}/images/smc-skylake-front-view.png "The front of the Skylake appliance")

### Skylake Back View
![The back of the Haswell appliance]({{ site.baseurl }}/images/smc-skylake-back-view.png "The back of the Haswell appliance")

{% include note.html content="The nodes on the back are in a reverse N shape, with Node A at the bottom right and Node D at the top left." %}

{% include note.html content="The Skylake appliance shown here is fully populated with four nodes." %}

{: id="Connect-the-Appliance"}
## Connect the Appliance

After you rack and stack the appliance, you can begin to configure it. If needed, review the [Hardware Appliance Overview]({{ site.baseurl }}/appliance/hardware/inthebox.html).

Follow these steps to connect the appliance. Refer to [Appliance Port Location]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#step-1-connect-switches-to-10gbe-ports) and [Appliance Power Button]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#step-3-turn-on-nodes).

### Step 1: Connect switches to 10GbE ports
Connect the 10GbE port of each node, as illustrated in [Appliance Port Location]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#step-1-connect-switches-to-10gbe-ports), to the 10GbE switches on your own rack using either fiber or DAC cables.

 Refer to the [Cable reference]({{ site.baseurl }}/appliance/hardware/cable-reference.html) for information on the cable types:
 * [Fiber Cables]({{ site.baseurl }}/appliance/hardware/cable-reference.html#fiber-cables)
 * [DAC Cables]({{ site.baseurl }}/appliance/hardware/cable-reference.html#dac-cables)

 {% include note.html content="Ask your hardware vendor for more details about what they supply and what you need to buy." %}

{: id=appliance-port-location}
Depending on which version of the SMC appliance you have, Haswell or Skylake, your 10GbE ports are in a different spot on the back of the appliance. Here is a picture of the back of each appliance.

{: id="smc-appliance-haswell-location-ports"}

![The data and management ports are on the back of the SMC Haswell appliance.]({{ site.baseurl }}/images/smc-haswell-location-ports-new.png "The back of the SMC Haswell appliance")

{% include note.html content="The above image of the Haswell appliance has a GBIC plugged in next to the highlighted 10GbE data port." %}

{: id="smc-appliance-skylake-location-ports"}

![The data and management ports are on the back of the SMC Skylake appliance.]({{ site.baseurl }}/images/smc-appliance-skylake-location-ports.png "The back of the SMC Skylake appliance")

* Connect to switches **only** the appliances (4 nodes each) that you want to use in the cluster.  
* You must power off or disconnect from the switch all other appliances or nodes. This prevents accidental configuration of incorrect nodes.  
* You must connect all nodes, even if using only one node, to a 10G switch. Verify that the connection is valid by pinging the gateway. To ping the gateway, enter `ping <default gateway IP>`. Ask your network administrator for your default gateway IP if you have not already listed it in your ThoughtSpot site survey.


### Step 2: Connect IPMI ports
Connect the IPMI port of each node to the management switch; see [Appliance Port Location]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#step-1-connect-switches-to-10gbe-ports).

### Step 3: Turn on nodes
Turn on the power for the nodes by pressing the power button; see [Appliance Power Button]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#step-3-turn-on-nodes).

{: id="smc-appliance-power-button"}
| Haswell Appliance | &#32; &#32; &#32; | Skylake Appliance |
| ---- | ---- | ---- |
| ![The power button is at the front of the Haswell appliance.]({{ site.baseurl }}/images/smc-haswell-power-button-new.png "The power button on the front of the Haswell SMC appliance")| &#32; | ![The power button is at the front of the Skylake appliance]({{ site.baseurl }}/images/smc-appliance-skylake-power-button.png "The power button on the front of the Skylake SMC appliance") |

{% include note.html content="There is one power button for each node." %}

### Step 4: Log in
Connect the keyboard and the mouse to the appliance, and log in using the *admin* user credentials for the console.

{: id="Configure-Node-in-Terminal"}
## Configure Nodes in Terminal
Once you have connected the appliance, you can begin to configure the nodes in your Mac Terminal or Windows terminal emulator.

### Step 1: Change to the `install` directory
In your terminal, change directory to `/home/admin/install` by running the command `cd /home/admin/install`. You may have to use the `home/admin` directory if your `/install` subdirectory does not exist.

### Step 2: Run the `get-config` command
Run the `tscli cluster get-config` command to get a list of the nodes that must be configured for the new cluster, and redirect it to the file `nodes.config`.  More information on this procedure can be found in the [nodes.config file reference]({{ site.baseurl }}/appliance/hardware/nodesconfig-example.html).


### Step 3: Configure the network of nodes
Add your specific network information for the nodes in the `nodes.config` file, as demonstrated in the [autodiscovery of one node example]({{ site.baseurl }}/appliance/hardware/nodesconfig-example.html#autodiscovery-of-one-node-example) in the [nodes.config file reference]({{ site.baseurl }}/appliance/hardware/nodesconfig-example.html). Fill in the areas specified in [Parameters of the `nodes.config` file]({{ site.baseurl }}/appliance/hardware/parameters-nodesconfig.html) with your specific network information. If you have  additional nodes, complete each node within the nodes.config file in the same way. Make sure that you do not edit any part of the nodes.config file except the sections explained in [Parameters of `nodes.config`]({{ site.baseurl }}/appliance/hardware/parameters-nodesconfig.html). Deleting quotation marks, commas, or other parts of the code could cause setup to fail.



### Step 4: Run the `set-config` command
Configure the nodes in the `nodes.config` file using the `set-config` command [(set-config)]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#set-config-command). Run `$ cat nodes.config | tscli cluster set-config`.

{: id="set-config-command"}

#### Set-config
```
$ cat nodes.config | tscli cluster set-config

Connecting to local node-scout  
Setting up hostnames for all nodes  
Setting up networking interfaces on all nodes  
Setting up hosts file on all nodes  
Setting up IPMI configuration  
Setting up NTP Servers  
Setting up Timezone  
Done setting up ThoughtSpot
```
#### Set-config error recovery
If the set-config fails with the following warning, restart the node-scout service by running `sudo systemctl restart node-scout`[(Restart node-scout service)]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#node-scout-restart).

{: id="node-scout-restart"}

#### Restart node-scout service
If you have this error, restart the node-scout.
```

Connecting to local node-scout WARNING: Detected 0 nodes, but found configuration for only 1 nodes.  
Continuing anyway. Error in cluster config validation: [] is not a valid link-local IPv6 address for node: 0e:86:e2:23:8f:76 Configuration failed.
Please retry or contact support.
```
Restart node-scout with the following command, then retry the [set-config command]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#set-config-command).

`$ sudo systemctl restart node-scout`

The command output should be the following:
```
$ cat nodes.config | tscli cluster set-config

Connecting to local node-scout  
Setting up hostnames for all nodes  
Setting up networking interfaces on all nodes  
Setting up hosts file on all nodes  
Setting up IPMI configuration  
Setting up NTP Servers  
Setting up Timezone  
Done setting up ThoughtSpot
```


### Step 5: Confirm node configuration with the `get-config` command
Confirm the node configuration with the `get-config` command [(Confirm node configuration)]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#confirm-node-configuration).

{: id=confirm-node-config}
#### Confirm node configuration
```
$ tscli cluster get-config

{  
  "ClusterId": "",  
  "ClusterName": "",  
  "DataNetmask": "255.255.252.0",  
  "DataGateway": "192.168.4.1",  
  "IPMINetmask": "255.255.252.0",  
  "IPMIGateway": "192.168.4.1",  
  "Timezone": "America/Los_Angeles",  
  "NTPServers": "0.centos.pool.ntp.org,1.centos.pool.ntp.org,2.centos.pool.ntp.org,3.centos.pool.ntp.org",  
  "DNS": "192.168.2.200,8.8.8.8",  
  "SearchDomains": "example.company.com",  
  "Nodes": {  	
	"ac:1f:6b:8a:77:f6": {  
  	"NodeId": "ac:1f:6b:8a:77:f6",  
  	"Hostname": "Thoughtspot-server1",  
  	"DataIface": {  
    	"Name": "eth2",  
    	"IPv4": "192.168.7.70"  
  	},  
  	"IPMI": {  
    	"IPv4": "192.168.5.70"  
  	}  
	}  
  }  
}
```
{: id="cluster-install"}
## Install Cluster
All nodes have now been configured. Next, you must install the cluster using the release tarball (est. time 1 hour). Make sure you can connect to ThoughtSpot remotely. If you can, you can run the installer on your local computer. If you have not received a link to download the release tarball, open a support ticket at [ThoughtSpot Support](https://support.thoughtspot.com) to access the release tarball.

{: id="run-installer"}
### 1. Run the Installer  
Copy the downloaded release tarball to /home/admin. Then you can run the `tscli cluster create` command and edit the output with your specific cluster information. For more information on this process, refer to [Using the `cluster create` command]({{ site.baseurl }}/appliance/hardware/cluster%20create.html) and [Parameters of the `cluster create` command]({{ site.baseurl }}/appliance/hardware/parameters-cluster-create.html).


The cluster installation automatically reboots all the nodes after the install. Wait at least 15 minutes for the installation process to complete. The system is rebooting, which takes a few minutes. Log into any node to check the current cluster status, using the command `tscli cluster status`.

### 2. Check Cluster Health
Once the cluster is installed, check its status with the `tscli cluster status` command [(Cluster Status)]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#check-cluster-health).

{: id="check-cluster-health"}

### Cluster Status
```
$ tscli cluster status
Cluster: RUNNING
Cluster name    : thoughtspot
Cluster id      : 1234X11111
Number of nodes : 3
Release         : 6.0
Last update     = Wed Oct 16 02:24:18 2019
Heterogeneous Cluster : False
Storage Type    : HDFS

Database: READY
Number of tables in READY state: 2185
Number of tables in OFFLINE state: 0
Number of tables in INPROGRESS state: 0
Number of tables in STALE state: 0
Number of tables in ERROR state: 0

Search Engine: READY
Has pending tables. Pending time = 1601679ms
Number of tables in KNOWN_TABLES state: 1934
Number of tables in READY state: 1928
Number of tables in WILL_REMOVE state: 0
Number of tables in BUILDING_AND_NOT_SERVING state: 0
Number of tables in BUILDING_AND_SERVING state: 128
Number of tables in WILL_NOT_INDEX state: 0
```
### 3. Finalize Installation

After the cluster status changes to “Ready,” log into the ThoughtSpot application on your browser.
Follow these steps:

1. Start a browser from your computer.
2. Enter your secure IP information on the address line.
    ```
    https:<IP-address>
    ```
3. If you don't have a security certificate for ThoughtSpot, you must bypass the security warning to proceed:
  * Click **Advanced**
  * Click **Proceed**
4. The ThoughtSpot login page appears.
5. In the [ThoughtSpot login window]({{ site.baseurl }}/appliance/hardware/installing%20the%20smc.html#ts-login), enter admin credentials, and click **Sign in**.
  ThoughtSpot recommends changing the default admin password.

{: id="ts-login"}
![ThoughtSpot's login window]({{ site.baseurl }}/images/ts-login-page.png "Log into ThoughtSpot. Enter Username, Password, and click Sign in. You may select Remember me option.")

## References
Use these references for successful installation and administration of ThoughtSpot.

* [The `nodes.config` file]({{ site.baseurl }}/appliance/hardware/nodesconfig-example)
* [Parameters of the `nodes.config` file]({{ site.baseurl }}/appliance/hardware/parameters-nodesconfig.html)
* [Using the `cluster create` command]({{ site.baseurl }}/appliance/hardware/cluster%20create.html)
* [Parameters of the `cluster create` command]({{ site.baseurl }}/appliance/hardware/parameters-cluster-create.html)
* [Cable Reference]({{ site.baseurl }}/appliance/hardware/cable-reference.html)
* [ThoughtSpot Documentation](https://docs.thoughtspot.com)
* [Contact Support]({{ site.baseurl }}/appliance/contact.html)