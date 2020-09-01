---
title: [Cassandra connection reference]
summary: Learn about the fields used to create a Cassandra connection with ThoughtSpot DataFlow.
last_updated: 07/03/2020
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for a Cassandra connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-cassandra-connection-properties">
<dlentry id="dataflow-cassandra-conn-connection-name"><dt>Connection name</dt><dd id="connection-name-description">Name your connection.</dd><dd id="connection-name-required">Mandatory field.</dd><dd id="connection-name-example"><strong>Example:</strong><br/>CassandraConnection</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-connection-type"><dt>Connection type</dt><dd id="connection-type-description">Choose the Cassandra connection type.</dd><dd id="connection-type-required">Mandatory field.</dd><dd id="connection-type-example"><strong>Example:</strong><br/>Cassandra</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-host"><dt>Host</dt><dd id="host-description">Specify the hostname or the IP address of the Cassandra system</dd><dd id="host-required">Mandatory field.</dd><dd id="host-example"><strong>Example:</strong><br/>www.example.com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-port"><dt>Port</dt><dd id="port-description">Specify the port associated to the Cassandra system</dd><dd id="port-required">Mandatory field.</dd><dd id="port-example"><strong>Example:</strong><br/>1234</dd><dd id="port-default"><strong>Default:</strong><br/>9042</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-user"><dt>User</dt><dd id="user-description">Specify the user to connect to Cassandra. This user must have data access privileges.</dd><dd id="user-required">Mandatory field.</dd><dd id="user-example"><strong>Example:</strong><br/>userdi</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-password"><dt>Password</dt><dd id="password-description">Specify the password for the User.</dd><dd id="password-required">Mandatory field.</dd><dd id="password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-authentication"><dt>Authentication</dt><dd id="authentication-description">Specifies the type of security protocol to connect to the instance. Based on the type of security select the authentication type and provide details.                                                                                     </dd><dd id="authentication-required">Mandatory field.</dd><dd id="authentication-example"><strong>Example:</strong><br/>Kerberos</dd><dd id="authentication-valid-values"><strong>Valid Values:</strong><br/>None, SSL, LDAP, Kerberos</dd><dd id="authentication-default"><strong>Default:</strong><br/>None</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-row-scan-depth"><dt>Row scan depth</dt><dd id="row-scan-depth-description">The maximum number of rows to scan to look for the columns available in a table. Set this property to gain more control over how the provider applies data types to collections.</dd><dd id="row-scan-depth-required">Optional field.</dd><dd id="row-scan-depth-example"><strong>Example:</strong><br/>-1</dd><dd id="row-scan-depth-default"><strong>Default:</strong><br/>100</dd><dd id="row-scan-depth-other"><strong>Other notes:</strong><br/>Advanced Configuration</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-kdc-host"><dt>KDC host</dt><dd id="kdc-host-description">Specify KDC Host Name where as KDC (Kerberos Key Distribution Center) is a service than runs on a domain controller server role. </dd><dd id="kdc-host-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="kdc-host-example"><strong>Example:</strong><br/>my_email@example.com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-user-keytab"><dt>User keytab</dt><dd id="user-keytab-description">To authenticate via a key-tab you must have supporting key-tab file which is generated by Kerberos Admin and also requires the user principal associated with Key-tab ( Configured while enabling Kerberos)</dd><dd id="user-keytab-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="user-keytab-example"><strong>Example:</strong><br/>/app/keytabs/labuser.keytab</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-default-realm"><dt>Default realm</dt><dd id="default-realm-description">A Kerberos realm is the domain over which a Kerberos authentication server has the authority to authenticate a user, host or service. </dd><dd id="default-realm-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="default-realm-example"><strong>Example:</strong><br/>name.example.com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-kerberos-service-kdc"><dt>Kerberos service KDC</dt><dd id="kerberos-service-kdc-description">Specify the Kerberos KDC of the service.</dd><dd id="kerberos-service-kdc-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="kerberos-service-kdc-example"><strong>Example:</strong><br/>www.example.com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-kerberos-service-realm"><dt>Kerberos service realm</dt><dd id="kerberos-service-realm-description">Specify the Kerberos realm of the service.</dd><dd id="kerberos-service-realm-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="kerberos-service-realm-example"><strong>Example:</strong><br/>EXAMPLE.COM</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-kerberos-spn"><dt>Kerberos SPN</dt><dd id="kerberos-spn-description">Specify the service principal name (SPN) for the Kerberos Domain Controller.</dd><dd id="kerberos-spn-required">Mandatory field.<br/>For Kerberos authentication only.</dd><dd id="kerberos-spn-example"><strong>Example:</strong><br/>cassandra/www.example.com@EXAMPLE.COM</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-ldap-user"><dt>LDAP user</dt><dd id="ldap-user-description">Specify the default LDAP user used to connect to and communicate with the server, it must be set if the LDAP server do not allow anonymous bind.</dd><dd id="ldap-user-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="ldap-user-example"><strong>Example:</strong><br/>userdi</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-ldap-password"><dt>LDAP password</dt><dd id="ldap-password-description">Specify the password for the LDAP User.</dd><dd id="ldap-password-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="ldap-password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-ldap-server"><dt>LDAP server</dt><dd id="ldap-server-description">Specify the host name or IP address of the LDAP server.</dd><dd id="ldap-server-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="ldap-server-example"><strong>Example:</strong><br/>my_email@example.com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-ldap-port"><dt>LDAP port</dt><dd id="ldap-port-description">Specify the port number that is associated to the LDAP server</dd><dd id="ldap-port-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="ldap-port-example"><strong>Example:</strong><br/>1234</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-search-filter"><dt>Search filter</dt><dd id="search-filter-description">Specify the search filter for looking up usernames in LDAP.</dd><dd id="search-filter-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="search-filter-example"><strong>Example:</strong><br/> sAMAccountName=</dd><dd id="search-filter-default"><strong>Default:</strong><br/>uid</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-search-base"><dt>Search base</dt><dd id="search-base-description">Specify the search base for the LDAP server, used to look up users.</dd><dd id="search-base-required">Mandatory field.<br/>For LDAP authentication only.</dd><dd id="search-base-example"><strong>Example:</strong><br/>DC=maxcrc,DC=com</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-trust-store-path"><dt>Trust store path</dt><dd id="trust-store-path-description">Specify the TLS/SSL client certificate store for SSL Client Authentication (2-way SSL)</dd><dd id="trust-store-path-required">Mandatory field.<br/>For SSL authentication only.</dd><dd id="trust-store-path-example"><strong>Example:</strong><br/>trust store path</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-trust-store-password"><dt>Trust store password</dt><dd id="trust-store-password-description">Specify the password for the TLS/SSL client certificate.</dd><dd id="trust-store-password-required">Mandatory field.<br/>For SSL authentication only.</dd><dd id="trust-store-password-example"><strong>Example:</strong><br/>password</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-certificate-type"><dt>Certificate type</dt><dd id="certificate-type-description">Specify the type of key store containing the TLS/SSL client certificate.</dd><dd id="certificate-type-required">Mandatory field.<br/>For SSL authentication only.</dd><dd id="certificate-type-example"><strong>Example:</strong><br/>JKSFILE</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-certificate-subject"><dt>Certificate subject</dt><dd id="certificate-subject-description">Specify the subject of the TLS/SSL client certificate.</dd><dd id="certificate-subject-required">Mandatory field.<br/>For SSL authentication only.</dd><dd id="certificate-subject-example"><strong>Example:</strong><br/>CN=www.example.com</dd><dd id="certificate-subject-default"><strong>Default:</strong><br/>*</dd></dlentry>
<dlentry id="dataflow-cassandra-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify the options associated with the JDBC URL.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/><code>jdbc:sqlserver://[serverName[\instanceName][:portNumber]]</code>
</dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
</dl>


## Sync properties

<dl id="dataflow-cassandra-sync-properties">
<dlentry id="dataflow-cassandra-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>1</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any printable ASCII character or decimal value for ASCII character</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>1</dd></dlentry>
<dlentry id="dataflow-cassandra-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if the text columns in the source data needs to be enclosed in quotes.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>DOUBLE</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>SINGLE, DOUBLE</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>DOUBLE</dd><dd id="enclosing-character-other"><strong>Other notes:</strong><br/>This is required if the text data has newline character or delimiter character.</dd></dlentry>
<dlentry id="dataflow-cassandra-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify the escape character if using a text qualifier in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>Any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-cassandra-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/><code>--max_ignored_rows 0</code></dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/><br/><code> --null_value ""</code><br/><code> --escape_character ""</code><br/><code> --max_ignored_rows 0</code></dd><dd id="ts-load-options-default"><strong>Default:</strong><br/><code> --max_ignored_rows 0</code></dd></dlentry>
</dl>