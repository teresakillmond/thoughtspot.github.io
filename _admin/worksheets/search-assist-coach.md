---
title: [Search Assist Coach]
last_updated: 3/23/2021
summary: "You can create your own Search Assist example queries, so your users can learn how to use ThoughtSpot's relational search on your own data."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

## Search Assist overview

[Search Assist]({{ site.baseurl }}/end-user/onboarding/search-assist.html) walks you through simple search scenarios using sample data. It demonstrates how anyone can get answers to their data questions by typing in the Search bar.

The initial example asks, ***What were sales for all products in 2019?***

Search Assist guides you to phrase this search as ***sales product 2019***.

The search then returns the Answer as a table.

Search Assist's default queries run on sample retail data, which is not specific to your company's use case or data. You may want to use your own data to train users to search data. With Search Assist Coach, you can use data from your own Worksheets to create example queries that appear to users when they first log into ThoughtSpot and go through onboarding.

## Create Search Assist lessons
You can only create your own Search Assist lessons on Worksheets, using the Search Assist Coach. You must have the **can manage data** permission.

To create your own lessons, follow these steps:

1. Navigate to the Worksheet for which you would like to create example queries.

2. Select the **Search Assist** tab, under the Worksheet name.

3. You see the 4 templates for lessons you can create. The templates are:
- What were `measure` by `attribute` in `filter`?<br>
    **For example:** What were `sales` by `region` in `2019?`
- What were your `keyword measure` for `attribute` in `filter`?<br>
    **For example:** What were your `top selling` for `products` in `this quarter`?
- What is the `measure` of `filter` per `time filter` by `attribute`?<br>
    **For example:** What is the `quantity purchased` of `shirts` per `monthly` by `city`?
- What were `measure` for `filter` in `filter` versus `filter filter`?<br>
    **For example:** What were `sales` for `shirts` in `california` versus `arizona last week`?

4. Click on any template to edit it with your specific data information. In this example, we edit Lesson 1: What were `measure` by `attribute` in `filter`?

    ![Create your own lesson: Lesson 1 template]({{ site.baseurl }}/images/search-assist-sample-query.png "Create your own lesson: Lesson 1 template")

    You can edit the language as well as the data-specific parameters. For example, since this example uses `Quantity Purchased` for its `measure`, we must change *What were* to *What was the*.

    {% include note.html content="You can only change certain aspects of the query. You cannot totally make up your own queries. While you can alter the language and specify your own measures, attributes, and filters, you cannot change the order in which the query elements appear." %}

5. After you fill in all the parameters for a lesson, the Answer your query generates appears below the query. Review the Answer to ensure it makes sense and provides good context for your users.

6. Select **Save**.

    ![Completed Search Assist query]({{ site.baseurl }}/images/search-assist-finished-example.png "Completed Search Assist query")

7. Your users see the sample queries you created when they first log into ThoughtSpot and go through the onboarding process.