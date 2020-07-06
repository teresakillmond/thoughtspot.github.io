---
title: [Add a MySQL database connection]
last_updated: 7/6/2020
toc: true
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
You can add a connection to a MySQL database using ThoughtSpot DataFlow.

Follow these steps:


{% include content/dataflow/add-database-connection.md %}

4. After you select the MySQL **Connection type**, the rest of the connection properties appear.

    <details>
      <summary>See the <strong>Create connection</strong> screen for MySQL</summary>
        <p>
        <img src="../../images/dataflow-mysql-create.png" alt="Create MySQL connection" /></p>
    </details>

    * [Connection name]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-connection-name)<br/>Name your connection.<br/>Mandatory field.
    * [Connection type]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-connection-type)<br/>Choose the MySQL connection type.<br/>Mandatory field.
    * [Host]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-host)<br/>Specify the hostname or the IP address of the MySQL system<br/>Mandatory field.
    * [Port]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-port)<br/>Specify the port associated to the MySQL system<br/>Mandatory field.
    * [User]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-user)<br/>Specify the user id that will be used to connect to the MySQL system. This user should have necessary privileges to access the data in the databases<br/>Mandatory field.
    * [Password]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-password)<br/>Specify the password for the App User<br/>Mandatory field.
    * [Version]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#dataflow-mysql-conn-version)<br/>Specify the MYSQL version being connected to.<br/>Optional field.

   See [Connection properties]({{ site.baseurl }}/data-integrate/dataflow/dataflow-mysql-reference.html#connection-properties).

5. Click **Create connection**.   