---
title: [SpotApps]
last_updated: 7/28/2020
summary: "SpotApps, ThoughtSpot's scriptable applications, allow you to migrate multiple objects to and from clusters."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

The SpotApps feature is in <span class="label label-beta">Beta</span> for 6.2. Talk to your ThoughtSpot contact if you are interested in SpotApps.

SpotApps take advantage of [Scriptability]({{ site.baseurl }}/admin/scriptability/scriptability.html), ThoughtSpot's solution for exporting, enhancing, and migrating ThoughtSpot objects, to provide you with scriptable applications you can use in multiple clusters.   

Once you connect to your data, you can work with your ThoughtSpot contacts to deploy ThoughtSpot's scriptable applications, or SpotApps, which provide an easy way for you to start getting value from your data.

ThoughtSpot offers [pre-built SpotApps](#pre-built-spotapps), which leverage your data in Snowflake or Redshift to provide pre-built Pinboards, Answers, Views, Tables and Worksheets. You can also [create your own SpotApps](#create-spotapps) by exporting multiple objects of the same type in one zip file, or an object and its associated data sources, and migrating these objects to another environment.

{: id="pre-built-spotapps"}
## Pre-built SpotApps
ThoughtSpot offers 3 pre-built SpotApps: Salesforce, procurement, and accounts receivable. These applications leverage your data in Snowflake, AWS Redshift, Azure Synapse, or Google BigQuery to provide pre-built Pinboards, Answers, Views, Tables and Worksheets.

For example, if you choose to use the Procurement SpotApp, the **Search** page contains a Worksheet for your users to query on, called "Procurement Analytics Solution."

![Procurement Worksheet Search]({{ site.baseurl }}/images/scriptable-app-procurement-search.png "Procurement Worksheet Search")

Your users may want to understand what Answers and Pinboards are before they start searching, or they may only want to view pre-built objects. They can view any of the pre-existing objects, such as this Exec Summary Pinboard:

![Exec summary]({{ site.baseurl }}/images/exec-summary-pinboard.png "Exec summary")

When you are ready to move to a production environment, you can migrate these Pinboards, Answers, Views, and Worksheets to your new environment using [Scriptability]({{ site.baseurl }}/admin/scriptability/scriptability.html), ThoughtSpot's flat-file editing and migration system for ThoughtSpot objects.

{: id="create-spotapps"}
## Create and export SpotApps
You can create your own SpotApps in two ways:

You may have a specific Pinboard that you would like to migrate to another cluster, but that cluster may not contain the Worksheets and Tables that the Pinboard's data comes from. When you export any object, you have the option to export its associated data sources as well, creating a SpotApp that you can migrate to another cluster without worrying about missing dependencies. The SpotApp .zip file contains a document called the `Manifest` file, which defines the objects you exported, and their underlying data sources.

![Choose what to export]({{ site.baseurl }}/images/scriptability-cloud-select-export.png "Choose what to export")

Similarly, you might want to migrate all the Answers on one cluster to another. You can select them all on the **Answers** list page, and export them as a SpotApp in .zip format. You can also choose to export their associated data sources in the same file.

See [Scriptability]({{ site.baseurl }}/admin/scriptability/scriptability.html) for more information on exporting and importing objects.