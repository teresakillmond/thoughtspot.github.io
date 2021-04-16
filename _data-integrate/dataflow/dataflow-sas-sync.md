---
title: [Sync data through a SAS connection]
last_updated: 10/27/2020
toc: true
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

After using ThoughtSpot DataFlow to establish a connection to a SAS database, you can create automatic data updates, to seamlessly refresh your data.

{% include content/dataflow/sync-for-databases.md %}

4. Specify the sync properties for SAS:

   * [Column delimiter]({{ site.baseurl }}/data-integrate/dataflow/dataflow-sas-reference.html#dataflow-sas-sync-column-delimiter)<br/>Specify the column delimiter character.
   * [Enclosing character]({{ site.baseurl }}/data-integrate/dataflow/dataflow-sas-reference.html#dataflow-sas-sync-enclosing-character)<br/>Specify if the text columns in the source data needs to be enclosed in quotes.
   * [Escape character]({{ site.baseurl }}/data-integrate/dataflow/dataflow-sas-reference.html#dataflow-sas-sync-escape-character)<br/>Specify this if the text qualifier is mentioned. This should be the character which escapes the text qualifier character in the source data.
   * [TS load options]({{ site.baseurl }}/data-integrate/dataflow/dataflow-sas-reference.html#dataflow-sas-sync-ts-load-options)<br/>Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code>

   See [Sync properties]({{ site.baseurl }}/data-integrate/dataflow/dataflow-sas-reference.html#sync-properties) for details, defaults, and examples.

5. Save your work by clicking **Save**.<br/>Alternatively, click **Save and sync now** to save your work and sync data at the same time.