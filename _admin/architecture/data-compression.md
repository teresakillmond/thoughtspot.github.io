---
title: [In-memory data compression]
last_updated: 8/17/2020
summary: "In-memory data compression lowers RAM requirements and reduces the number of VMs you need for in-memory data, reducing deployment costs for appliance and cloud platforms."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
The cost to deploy ThoughtSpot on an appliance or cloud platform depends on your data capacity. ThoughtSpot release 6.2 includes improvements to in-memory data compression. These improvements lower your RAM requirements and reduce the number of VMs you need for in-memory data, when deploying on a cloud platform.

In release 6.2, ThoughtSpot added two new compression algorithms to the Dictionary compression that ThoughtSpot already supports. ThoughtSpot now supports **LZ4**, for `INT`, `BIGINT`, `DOUBLE`, and `FLOAT` data types, and **RLE**, for strings.

These improvements to in-memory data compression may result in up to 20-50% compression of your in-memory data, reducing your cloud and appliance costs.

In-memory data compression is turned on by default for new clusters on release 6.2. If you upgrade from an older release to 6.2, this feature is ***not*** on by default. After you upgrade to 6.2, ThoughtSpot compresses any new tables you create, but does not compress your existing tables. To enable compression of your existing in-memory data after you upgrade to 6.2, or to find out if it could lower your data costs, [contact ThoughtSpot Support]({{ site.baseurl }}/appliance/contact.html).

{% include note.html content="ThoughtSpot compresses <strong><em>only</em></strong> your fact tables, not your dimension tables." %}

## View your in-memory data compression information
You can view compression ratios for your overall system, and for each table individually.

To view compression ratios for your overall system, you must have **Admin** privileges. Navigate to the Administration Portal by clicking on the **Admin** tab from the top navigation bar. Select **Overview** from the side navigation bar that appears.

![Admin Portal - Overview Pinboard]({{ site.baseurl }}/images/admin-portal-overview-pinboard.png "Admin Portal - Overview Pinboard")

You can see the compression ratio from the **Relational Data Cache** panel on the first row of the System Overview Pinboard. Here, the compression ratio is 1:1.34.

![Relational Data Cache - Compression Ratio]({{ site.baseurl }}/images/in-memory-data-compression-ratio-overall.png "Relational Data Cache - Compression Ratio")

To view compression ratios for each table individually, navigate to the **Table Information** table. Click on the **Data** tab from the top navigation bar. Select **Usage > Data**.

You can see the compression ratio from the **Compression Ratio** column, when you scroll all the way to the right on the table. Here, the compression ratio for the first table is 1:100.09.

![Table Information - Compression Ratio]({{ site.baseurl }}/images/in-memory-data-compression-ratio-specific-table.png "Table Information - Compression Ratio")