---
title: [Aggregate filters]
summary: Learn about aggregate filters.
last_updated: 06/11/2021
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

When working with query filters, you can switch to finer-grained or coarser-grained representation of your data. ThoughtSpot then re-aggregates the query to generate your new results and visualizations. Similarly, ThoughtSpot re-aggregates the query when you include or exclude the filter condition in the interface.

## Include or exclude filter condition

With `query_filters()+{filter_condition}` or `query_filters()-{filter_condition}`, you can aggregate the results when including or excluding a filter condition.

### Example

Filter condition: `Ship Mode='car'`

When you search on category `Customer ID sales` by `customer id` and category `Ship Mode='car’`, you can add a formula that calculate sales by category for each customer:

```
sales by Customer ID and Category = group_aggregate (
   sum(Sales),
   {Category, Customer ID },
   query_filters()+{Ship Mode='air'}
   )
```

ThoughtSpot aggregates the results  in the following manner:

* Dimensions: ‘Category’ and ‘Customer ID’
* Filters: ‘air’ and ‘car’.


### Add a column to query filter

When you add the `query_filters()-{column}` clause to the expression, ThoughtSpot enables you to aggregate the results _while removing_ the expression related to the column.

### Example

Filter condition: `Ship Mode='car'`

When you search on category `Customer ID sales` by `customer id` and category `Ship Mode='car'`, you can add a formula that calculate sales for each customer, _while ignoring_ the filter on the column:

```
sales by Customer ID and Category = group_aggregate (
   sum(Sales),
   {Customer ID, Category},
   query_filters()-{Ship Mode}
   )
```

In this case, ThoughtSpot aggregates the results in  the following manner:
* Dimensions: Customer ID
* Filters: none, because ignored 