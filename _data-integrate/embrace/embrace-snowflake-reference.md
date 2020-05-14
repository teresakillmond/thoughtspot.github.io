---
title: [Snowflake connection reference]
summary: Learn about the fields used to create a Snowflake connection with ThoughtSpot Embrace.
last_updated: 01/24/2020
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields of a Snowflake connection in ThoughtSpot Embrace. You need specific information to establish a seamless and secure connection.

 - **Connection name**: Mandatory. Enter a new Snowflake connection name.
 - **Connection description**: Optional. Provide a short description about your connection.
 - **Account name**: Mandatory. Enter the account name associated with your Snowflake connection.
The account name is part of the URL that you use to access the Snowflake UI. It is the portion of the URL before **snowflakecomputing.com**.  
  *Example*: If your URL is **https://abcd.xyz.efg.snowflakecomputing.com**, your account name is **abcd.xyz.efg**.
 - **User**: Mandatory. Enter the Snowflake account username.
 - **Password**: Mandatory. Enter the Snowflake account password.
 - **Role**: Mandatory. Specify the privilege of the user.
 - **Warehouse**: Mandatory. Specify the warehouse associated with the connection.
 - **Database**: Optional. Specify the database associated with the account.
 - **Schema**: Optional. Specify the schema associated with the database.