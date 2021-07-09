---
title: [Custom calendar overview]
last_updated: 5/5/2021
toc: true
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

With a custom calendar, you can choose when the year, quarter, or week starts, and search using date-related keywords.

You can create custom calendars for different purposes within your company, including:
- Retail calendars, like 4-4-5, 4-5-4, or 5-4-4
- Fiscal calendars, where the year or quarter starts on a different date each year
- Pharmaceutical calendars, where the week runs from Friday through Thursday
- Calendars in different languages

## Options

In a custom calendar, you can set the following:
- The starting date of a year
- The starting dates of quarters
- The starting day of the month
- The starting day of the week
- The words used for the days of the week, months and quarters

## Search features

You can use your custom calendar to search the following ways:
- Using date keywords, like `this quarter` and `q3`
- Using date formulas with the `fiscal` option specified (See [Fiscal and Gregorian calendars]({{ site.baseurl }}/advanced-search/formulas/date-formulas.html#fiscal-and-gregorian-calendars))
- Overriding the calendar used in the search bar by typing your custom calendar’s name
- Binding a calendar with a column under the table detail page. Example: Binding `Lineorder` `commitdate` with the French calendar.
- Specifying a calendar in the formula

## Limitations
- Only supported for Snowflake connections at this time.
- Calendar name must be unique across connections in a cluster.
- When creating or updating a calendar, a table is created in the external database.
- When deleting a calendar, the mapping to the table is removed from ThoughtSpot, but the table is not dropped from the external database.
- Queries using the search bar do not filter suggestions by connection.
- Date format must use *MM/DD/YYYY*. No other formats are supported.
- Calendars, by default, use English names for days of the week, and month, but can be manually changed by downloading and editing the calendar file
- Maximum scope of the date dimension is 90 years
- Maximum length of a calendar year is 12 months
- Calendar displays quarter numbers based on the Gregorian calendar (which starts on January 1st). If your custom calendar begins any other date, you must adjust the quarter numbers to align with your calendar. For example: If your custom calendar begins on April 1st, the calendar would incorrectly show April, May and June as quarter 2. In this case, you would need to correct this to indicate those months are quarter 1 and correct the subsequent months to have the correct quarter.

## Prerequisites

- Before you can create a custom calendar, you must contact [ThoughtSpot Support]({{ site.baseurl }}/admin/misc/contact.html) to enable the custom calendar feature on your cluster.

- For a user to create a custom calendar, they must have the required permissions to create a table in the Snowflake database used in the connection where they want to create their custom calendar.

## Related information

[Create a custom calendar]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-cust-cal-create.html#)  
[Update a custom calendar]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-cust-cal-update.html#)  
[Delete a custom calendar]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-cust-cal-delete.html#)   