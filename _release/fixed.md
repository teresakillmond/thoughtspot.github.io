---
title: ["Fixed issues"]
keywords: "fixed issues"
last_updated: 04/09/2020
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
These are the issues we fixed in recent ThoughtSpot Releases.

<ul>
   <li><a href="#5-3-2-cu3">5.3.2 CU3 Fixed issues</a></li>
   <li><a href="#5-3-2-cu2">5.3.2 CU2 Fixed issues</a></li>
   <li><a href="#5-3-2-cu1">5.3.2 CU1 Fixed issues</a></li>
   <li><a href="#5-3-2">5.3.2 Fixed issues</a></li>
   <li><a href="#5-3-1">5.3.1 Fixed issues</a></li>
   <li><a href="#5-3">5.3 Fixed issues</a></li>

   <li>
     <details>
      <summary>5.2.X Releases</summary>
        <ul>
          <li><a href="#5-2-3">5.2.3 Fixed issues</a></li>
          <li><a href="#5-2-2">5.2.2 Fixed issues</a></li>
          <li><a href="#5-2-1">5.2.1 Fixed issues</a></li>
          <li><a href="#5-2">5.2 Fixed issues</a></li>
       </ul>
     </details>
   </li>

   <li>
     <details>
      <summary>5.1.X Releases</summary>
        <ul>
          <li><a href="#5-1-4">5.1.4 Fixed issues</a></li>
          <li><a href="#5-1-3">5.1.3 Fixed issues</a></li>
          <li><a href="#5-1-2">5.1.2 Fixed issues</a></li>
          <li><a href="#5-1-1">5.1.1 Fixed issues</a></li>
          <li><a href="#5-1">5.1 Fixed issue</a></li>
        </ul>
      </details>
    </li>  

    <li>
      <details>
       <summary>5.0.X Releases</summary>
         <ul>
           <li><a href="#5-0-4">5.0.4 Fixed issue</a></li>
           <li><a href="#5-0">5.0 Fixed issues</a></li>
          </ul>
        </details>
      </li>

      <li>
        <details>
          <summary>4.X Releases</summary>
            <ul>
              <li><a href="4-5-1">4.5.1 Fixed issues</a></li>
              <li><a href="4-5">4.5 Fixed issues</a></li>
              <li><a href="4-4">4.4 Fixed issues</a></li>
            </ul>
          </details>
        </li>
      </ul>

<a id="5-3-2-cu3"></a>
## 5.3.2 CU3 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.3.2 CU3.

- Exported PDF, CSV, and XLSX files display caption tags.

- Administrators are not able to edit a worksheet.

- A legend in a chart is not displayed correctly when the _monthly_ attribute is used in a search.

- After upgrade to 5.3.2 CU2, users cannot access a ThoughtSpot instance previously accessed through SSO.

- Users cannot sign in to a ThoughtSpot instance through SSO.

- Changes made to a schema through TQL are not reflected when viewed in the ThoughtSpot UI.

<a id="5-3-2-cu2"></a>
## 5.3.2 CU2 Fixed issue

This is the issue we fixed in ThoughtSpot Release 5.3.2 CU2.

- Visualizations that worked in the past, display an error message.

<a id="5-3-2-cu1"></a>
## 5.3.2 CU1 Fixed issue

This is the issue we fixed in ThoughtSpot Release 5.3.2 CU1.

- Rows that don't exist in TQL appear when filtering in the ThoughtSpot UI.

<a id="5-3-2"></a>
## 5.3.2 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.3.2.   

- Delayed search enabled in a previous release version does not work after upgrade to 5.3.1.

- Pop-up messages sometimes cover the entire width of the screen.

- _Share_, _Copy a link_, and _Send feedback_ cannot be disabled when ThoughtSpot is embedded.

- An error in the date range occurs when drilling down in a custom calendar.

- When the network check fails during a self-service upgrade, it retries indefinitely.

- If formulas have a less-than sign (<) followed by text, the text following the less-than sign does not display in a table.

- Removing a column from a search query increases the number of rows displayed.

- A search that uses the `group_max` function displays an incorrect result when filtering is applied.

<a id="5-3-1"></a>
## 5.3.1 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.3.1.

- Using a custom calendar, and doing a query that filters on a date field causes a database error.

- Signing in to ThoughtSpot multiple times in quick succession causes a 500 error.

- When row-level security is used, a 2-column join in a fan-trap query does not work if the column contains NULL data/values.

- Opening certain pinboards can cause the Google Chrome browser to freeze.

- Columns renamed in a worksheet revert back to their original names later.

- Columns cannot be deleted from a worksheet.

- Using a custom calendar and filtering date values by year, month or quarter does not work.

- Canadian postal codes do not appear on maps.

- The Admin > Style Customization page indicates the wrong pixel dimensions required for a wide application logo.

- Certain HTTP security headers are not implemented.

<a id="5-3"></a>
## 5.3 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.3.

### Display and Rendering

- A problem where dates do not display properly in the query details pane of an answer is now fixed.  
- An issue where the color coding of columns is not displayed in a PDF downloaded from a worksheet is fixed.  
- A problem where using **Copy and edit** in a saved answer causes the screen to go blank has been fixed.  
- An issue where axis labels are missing from some visualizations is now fixed.  
- A problem where URLs that appear within an Answer are red, instead of blue, is now fixed.  
- An issue where an answer that has no measures causes it to display blank is now fixed.  
- A problem where weekly and monthly charts are not showing weekly and monthly aggregation correctly is now fixed.

### Pinboards

- A problem where the column tooltip in a pinboard does not show last updated information has been fixed.  
- An issue where the filter dialog box is unresponsive when opened from pinboard is now fixed.  
- A problem when pinning an answer to a pinboard where the pinboard list is very slow to display is now fixed.  
- An issue where scheduled pinboard emails fail to send to a specific recipient with a valid email address is now fixed.  
- A problem where a stacked bar chart does not work in a pinboard is now fixed.  
- An issue where an exclude filter does not work properly on a pinboard is now fixed.  
- A problem where a user cannot edit a pinboard, even though they have the proper permissions to do so is fixed.  
- An issue where emails fail to send from scheduled pinboards that contain Japanese characters in their title is now fixed.

### Search

- A problem where nulls are excluded from a query, even when they have not been excluded using a filter is now fixed.  
- An issue where searches on a pinboard don’t include cached queries has been fixed.  

### Administration

- An issue where running the `tscli cluster` command causes a failed security check is now fixed.   
- A problem where the Informatica ODBC cannot connect to ThoughtSpot is now fixed.<br>

### Answers

- A problem where a saved answer cannot be opened when it uses an aggregate function is now fixed.

<a id="5-2-3"></a>
## 5.2.3 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.2.3.   

- An issue where LDAP sync does not sync users after upgrade to release 5.2.2 is now fixed.

- A problem where certain types of joins do not work when row-level security is used is now fixed.

- An issue where opening certain pinboards can cause the Google Chrome browser to freeze is now fixed.

- A problem in custom calendar where filtering the date values by year, month or quarter does not work is now fixed.

- An issue where syncing users using the public API does not work is now fixed.

- A problem where Canadian postal codes do not appear on maps is now fixed.

<a id="5-2-2"></a>
## 5.2.2 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.2.2.

- An issue where PDFs downloaded from a Pinboard are poorly formatted is now fixed.

- An occasional problem where the login process is slow has been fixed.

- An issue where the filter dialog box freezes when opened from a Pinboard, or the filter icon in the left panel is now fixed.

- Previously, when the `unique_count_if` aggregate function was used in both the numerator and denominator of a division formula in a search query, it caused only the numerator value to be returned. This problem is now fixed.

- A problem where the `unique_count_if` aggregate function does not parse an expression is now fixed.

<a id="5-2-1"></a>
## 5.2.1 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.2.1.   

- An issue where column tooltips do not display last-updated information is now fixed.

- An error that occurs when attempting to save changes to the title of a visualization is now fixed.

- An issue with the user-onboarding walkthrough intermittently failing to load is now fixed.

- Reliability of the filter dialog when opened from a Pinboard or the left panel has been improved.

- An issue with a NAS mount disconnecting during restore of a cluster is now fixed.

- A problem where tables in a Google Chrome tab become misaligned is now fixed.

- Corrupted metadata after an upgrade which made some worksheets uneditable is now fixed.

- An issue where greyed-out search phrases could not be edited while in delayed search mode is now fixed.

- The database manager memory limit has been increased to 16 GB to improve performance.

- An issue where tables created with incorrect DDL syntax could be imported without errors is now fixed.

- A problem with date filters in the Japanese locale is now fixed.

- An issue with refreshing materialization of views is now fixed.

- Occasional slow navigation between the Answer and Pinboard pages has been fixed.

- A problem where scheduled Pinboard emails failed to send to a specific recipient with a valid email address message is now fixed.

- Embedded Pinboards no longer occasionally display a Pin button.

<a id="5-2"></a>
## 5.2 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.2.

- Table user experience improvements:
   * The column header is now left-aligned.
   * Column widths can be made very narrow.

- Chart user experience improvements:
   * When sorting by date on the x-axis, the date format no longer changes and the axis no longer disappears.
   * You can now sort using a sort field that is not in your chart.

<a id="5-1-4"></a>
## 5.1.4 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.1.4.

- An error that occurred when saving changes to the title of a visualization is now fixed.

- An issue where some worksheets became uneditable after an upgrade, due to corrupted metadata, is now fixed.

- A problem with date filters in the Japanese locale is now fixed.

- An issue with refreshing materialization of views is now fixed.

<a id="5-1-3"></a>
## 5.1.3 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.1.3.

- Downloading an R visualization no longer causes an empty page to be displayed.

- A problem where tables in a Google Chrome tab become misaligned is now fixed.

- Custom scatter charts no longer disappear from pinboards after an upgrade.

- An issue where the Copy-and-edit button incorrectly appears on embedded visuals is now fixed.

- Occasional slow navigation between the Answer and Pinboard pages has been fixed.

- A normal bar chart in a pinboard which is changed to a stacked bar chart no longer reverts to the normal bar chart after the pinboard is saved, browser is closed, and pinboard is reopened.

vA problem where using the exclude filter on pinboards causes the wrong results to be displayed is now fixed.

- Usage-based indexing of search has been improved.

- A problem where the `tscli ssl rm-cert` command was used to remove a cert, but did not revert it back to the default cert is now fixed.

- When a search that uses no attributes results in fan-trap queries, the measure values shown are no longer incorrect.

- A problem where some users could not log in through SSO after an upgrade has been fixed.

- Fan-trap queries no longer have more grouping columns than necessary.

- An issue with worksheets showing incomplete compound-column joins has been fixed.

- A problem where the user interface becomes slow during a data load has been fixed.

- CSVs downloaded by certain row-level-security users are no longer empty.

<a id="5-1-2"></a>
## 5.1.2 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.1.2.

- Search no longer stops working under certain conditions like fast typing, or copying and pasting of a search query.

- Selecting 'Copy and Edit' in an answer, pinboard visualization, insight, SpotIQ pinboard or view, no longer causes the user to be signed out.

- HDFS images for a cluster are now created prior to pushing the HDFS configuration. This ensures images are fresh during an upgrade.

- When removing a node, the node calling command no longer results in unreachability due to misconfigured firewall settings.

- Permissions issues with `tsload` and `tql` are now fixed, so the **thoughtspot** user can load data.

- Database stability has been improved.

<a id="5-1-1"></a>
## 5.1.1 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.1.1.

-  Geo Bubble map labels can now be disabled or enabled through a data labels checkbox.

-  Filter panel failure to open during formula creation has been fixed.

-  Custom R analysis failure when run from Custom Analyze has been fixed.

-  Microsoft Internet Explorer button display problem in Edit Group, Add a New Group, and Custom Analysis has been fixed.

-  Tooltips in line, scatter, and radar charts have been improved to avoid tooltip display when far from a data point.

-  Microsoft Internet Explorer problem with saving the name of an answer has been fixed.

-  Previously, admin style and font customizations for tables and charts were off by default. They are now on by default.

-  Search phrase autocomplete has been fixed to prevent unnecessary red highlighting of values.

-  Geo Bubble and Geo Heatmap issue where chart displays momentarily and then disappears has been fixed.

-  Zoom on Geo maps can now be done using a mouse scroll wheel.

<a id="5-1"></a>
## 5.1 Fixed issue

We fixed the following issue in ThoughtSpot Release 5.1.

- The X and Y axes were previously flipped on [bar charts and stacked bar charts]({{ site.baseurl }}/end-user/search/about-bar-charts.html). This has been fixed.

<a id="5-0-4"></a>
## 5.0.4 Fixed issue

We fixed the following issue in ThoughtSpot Release 5.0.4.

- Deprecated SSH cryptographic settings are used.

<a id="5-0"></a>
## 5.0 Fixed issues

These are the issues we fixed in ThoughtSpot Release 5.0.

- Changes to metadata result in rebuilding the search index, even though the data has not changed.

- A search returns an unexpected answer, because the last aggregation performed during execution was doing a `MIN()` rather than a `SUM()`.

- Timeouts cause a cluster crash in some cases when a right outer join was used.

- The space allocation chart does not update.

<a id="4-5-1"></a>
## 4.5.1 Fixed issues

These are the issues we fixed in ThoughtSpot Release 4.5.1.

- Filters now work on formula-derived columns where the formula returns a numeric value of a type other than the integer types. In the past, filtering on a DOUBLE type formula-derived column required that the formula convert any DOUBLE values to an integer (INT32 or INT64). Now this type conversion is not necessary.

- A problem was resolved where changes to metadata resulted in rebuilding the search index, even though the data had not changed.

- A problem was resolved where a search was returning an unexpected answer, because the last aggregation performed during execution was doing a MIN() rather than a SUM().

- A problem was resolved where timeouts were causing a cluster crash in some cases when a right outer join was used.

- A problem was resolved where user names were accidentally being sent along with cluster metrics.

- A problem was resolved where the space allocation chart was not getting updated.

- A problem was resolved where indexes failed to build for empty tables.

- An issues with upgrade was resolved which caused the appliance to boot from an incorrect partition causing users to be found missing.

- A problem was resolved where you could not add a column to the search in cases where there was a long list of columns on the Search page. Clicking on a column name caused the column names to shift, such that you could no longer double click on the column name to add it to the search.

- A problem was resolved where SpotIQ sometimes did not return a result unless a process was restarted.

- A problem was resolved where where deadlock issues with the Search service caused indexing to fail.

- A problem was resolved where if the word "top" occurred as a data value, you could not use "top" as a keyword.

- A problem was resolved where periodic backups was delayed.

- A problem was resolved where adding columns to a worksheet and saving it resulted in timeouts and an <code>HTTP_UNAUTHORIZED(401)</code> status.

- A problem was resolved where idle sessions were never timing out.

- An underlying system issue was resolved that caused a saved answer to fail with a read bar error if the answer was created on a relationship(s) which was based on a hidden column(s).

- A problem was resolved where sorting on a primary key column produced duplicates for some values, both when viewing results in the ThoughtSpot application and when using TQL.

- A problem was resolved where after upgrading, some pinboards could not be opened and instead returned a red bar error.

- A problem was resolved where the number format wasn't being honored when the column contained a currency. Setting the format for three digits after the decimal resulted in displaying only two.

- An issue was resolved where hidden fields in source data prevented users from creating answers related to other columns in that data.

- A problem was resolved where drill down on multiple buckets did not apply all date filters.

- An issue was resolved that potentially made ThoughtSpot at risk for Jackson JSON Library Vulnerabilities.

- A problem was resolved where a node failed due to a bad DIMM (Dual In-Line Memory Module), but didn't failover successfully.

- A problem was resolved where data loaded very slowly.

- An issue was resolved where the ThoughtSpot application was potentially vulnerable to Cross-Site Request Forgery (CSRF) . The potential was removed from the application interactions. Any ThoughtSpot API customers will have to be updated to be compliant with this new feature. The primary things that could be affected:

  - Sync scripts that manage users and groups creation.
  - Scripts that use the public APIs to fetch data.

- The easiest way to diagnose this would be to check for the inability of the script to log in to the system. Please contact ThoughtSpot Support to get guidance on the steps to resolve the issue.

<a id="4-5"></a>
## 4.5 Fixed issues

These are the issues we fixed in ThoughtSpot Release 4.5.

- A problem was resolved where insufficient memory caused services on a cluster to crash repeatedly.

- A problem was resolved where idle sessions were never timing out.

- A problem was resolved where indexes failed to build for empty tables.

- A problem was resolved where users were unable to scroll in IE with pivot tables.

- An issues with upgrade was resolved which caused the appliance to boot from an incorrect partition causing users to be found missing.

- A problem was resolved where where deadlock issues with the Search service caused indexing to fail.

- A problem was resolved where periodic backups was delayed.

- Adding columns to a worksheet and saving them resulted in timeouts and an <code>HTTP_UNAUTHORIZED(401)</code> status. This problem resulted from an internal <code>SESSION</code> handling error. This problem was resolved in this release.

- A problem was resolved where <code>tsadmin</code> and <code>guest</code> were prevented from uploading a CSV upload and received a red bar error instead.

- A problem with memory links during upgrade was resolved.

- A problem was resolved where Google Chrome version 65 broke the formatting of headlines in pinboards. This issue was reported as a Product Support Advisory for versions 3.x and 4.x releases older than 4.4.1.4.

- An underlying system issue was resolved that caused a saved answer to fail with a red bar error if the answer was created on a relationship(s) which was based on a hidden column(s).

- A pinned answer that relied on an underlying join between two worksheets one of which included a filter failed to display properly. This problem was resolved in this release.

- After upgraded customer appliance from 4.4.0.11 to 4.4.1.2 GA, some pinboards could not be opened and instead returned a red bar error. This issue was resolved.

- Some customers reported that several data buckets were relative to calendar year/quarter/month rather than relative to the financial year.
  - QUARTER_OF_YEAR
  - MONTH_OF_YEAR
  - MONTH_OF_QUARTER
  - WEEK_OF_YEAR_ISO
  - WEEK_OF_QUARTER
  - DAY_OF_YEAR
  - DAY_OF_QUARTER

- An issue was resolved where hidden fields in source data prevented users from creating answers related to other columns in that data.

- Customers were receiving a <code>RowSecurityManager not implemented for Atlas.</code> message when scheduling a pinboard. This problem was the result of legacy features in the system. These features no longer are checked.

- A problem was resolved where drill down on multiple buckets did not apply all date filters.

- A problem was resolved that caused segmentation faults which in turn caused crashes in a cluster during an upgrade.

- An issue was resolved that potentially made ThoughtSpot at risk for Jackson JSON Library Vulnerabilities.

- A problem was resolved with the <strong>Show underlying data</strong> function ignoring the "last period" filter. This filter is no longer ignored.

- A problem was resolved where the presence of a date bucket filter after a measure column was ignored in query execution.

- Issues were resolved that potentially exposed ThoughtSpot to two vulnerabilities: "Meltdown" and "Spectre", along with variants. These vulnerabilities only applied when the ThoughtSpot application was sharing hardware with other applications, such as cloud deployments. When deployed in a virtualized environment, either on prem or in AWS, the virtual environment needed to patch the OS for it. When deployed on its own appliance, these vulnerabilities should not have affected ThoughtSpot.

- An issue was fixed that occurred when plotting a formula that has either NaN or Infinity as some of the values. In this case, the pivot table treated the first instance of NaN/Infinity and every subsequent value as a single value and plots it in one cell. This problem was fixed.

- A problem was resolved where <code>near</code> keywords returned a red bar error.

- An issue was resolved where requests to update a formula failed due to the complexity of the nesting.

- Non-admin user could still see hidden fields. In queries, these users were asked to disambiguate these even though they were hidden. This problem was resolved.

- An issue was fixed where the installation path was not properly updated resulting in an environment pointing to old versions of <code>tsload</code> and <code>tql</code>. Now, the standard path is updated during an upgrade.

- A problem was resolved where a saved answer from version 4.3 failed after upgrade because they referred to old table names.

- When query has keywords that map to date column and Period Ago date buckets then SpotIQ Insight for that query did not work even though the user-created query succeeded. This SpotIQ bug was resolved.

- When a query had keywords that mapped to a date column as well as to date buckets, SpotIQ Analysis failed for that query. For example, in query <code>revenue in Q1 1992</code> the last part represents date buckets. If <code>Q1 1992</code> maps to a date column then SpotIQ analysis failed. The query itself worked and any answer/pinboard that based on these queries were fine. This problem was resolved.

- A problem was resolved where NPS surveys were appearing when ThoughtSpot was provided through embedded content. This should no longer occur.

- A problem was occurring where upgrade to a new version caused several types of formulas that relied on aggregated data to stop working. Problems were recorded involving:

  - Unique or count not functional when using Aggregated date.
  - Group_count not functional as well.
  - Group_max giving duplicated result.

  This problem was resolved and should no longer appear

- A problem was resolved where ThoughtSpot would throw an error if the query involved multiple date filters on the same date column. This has been fixed in this release.

- A problem was resolved where the <code>tscli ssl set-min-version</code> failed because the minimum value was incorrect internally. The internal issue was resolved.

- An issue with the callhome metrics feature caused problems during upgrade. This problem was resolved.

- A problem was resolved where deleting a relationship failed if either side of that relationship was a worksheet.

- A problem was resolved where Zookeeper reported reaching a descriptor limit. This report was returned in error. ThoughtSpot no longer reports this.

- A problem was resolved where data loaded very slowly.

- A problem where Strict Transport Security was not enforced was fixed. The product now supports Strict Transport Security.

- An issue was resolved where the ThoughtSpot application was potentially vulnerable to Cross-Site Request Forgery (CSRF) . The potential was removed from the application interactions. Any ThoughtSpot API clients will have to be updated to be compliant with this new feature. The primary clients that would be effected:

  - Sync scripts that manage users and groups creation.
  - Scripts that use the public APIs to fetch data.

- The easiest way to diagnose this would be the inability of the script to login to the system. Please contact support to get guidance on the steps to resolve the issue.

- A problem was resolved with the <code>JESSIONID</code> value. Previously, setting the <strong>Remember Me</strong> option on the login page, caused the server to set a new <code>JSESSIONID</code> on the client after the user logs out. This new <code>JSESSIONID</code> was used for the next authenticated user session, regardless of the user's identity. This no longer happens. Instead, users that re-login after setting <strong>Remember Me</strong> are given a new <code>JSESSIONID</code>.

- Dates on the *<strong>Data</strong>* page was corrected so that dates now sort chronologically.

- Previously, the application allowed cookies to contain information related to session state. An option was added to set more secure cookie handling in the application.

- Previously, the login form on the ThoughtSpot application provided an autocomplete feature. Autocomplete is no longer support. Turning off <code>autocomplete</code> prevents intruders from compromising ThoughtSpot from a workstation unattended using a previously stored user ID and/or password.

- Previously, alerts were time stamped with in PDT. This was fixed, now <code>tscli alert list</code> shows alerts display in the cluster's local timezone.

- The system now validates both the format and the size of profile pictures, previously these were not checked.

<a id="4-4"></a>
## 4.4 Fixed issues

These are the issues we fixed in ThoughtSpot Release 4.4.

- Aggregation over group_max returned a red bar error. This was resolved, users can now aggregate over a `group_max` function.

- A problem with editing formulas was resolved where users were repeatedly and unnecessarily presented with disambiguation options.

- An issue was resolved where a bar on the chart label did not match the underlying data. The data was correct, the label was not.

- An issue was corrected where, if one snapshot deletion failed in any fashion, any subsequent attempts to delete a snapshot failed.

- Users were unable to edit a KPI formula if the KPI formula was pinned to a pinboard.

- Users were able to <strong>Select All</strong> for 1000+ items in a pinboard filter. This action was available but not supported and caused users to believe pinboard filters were not working. Now, the option to <strong>Select All</strong> no longer functions when there are 1000+ items in a filter.

- Users were unable to restore a database backup without first renaming the backup. Renaming is no longer required.

- Creating a formula on `cumulative_sum` function mistakenly caused an error to appear. This action no longer causes an error.

- Some installations saw worksheet performance degrade for worksheets with a large number of columns. Users can now set a configuration option to avoid these problems.

- Previously setting both the browser and the ThoughSpot profile value failed to display numbers and date formats in the proper locale. This problem was corrected. Setting the ThoughtSpot profile to the proper locale results in the appropriate display of date and number formats. It also causes translated strings to appear in the interface where they exist.

- Active directory (AD) synchronization was not working. Moreover, if AD security group had no members in it, then the synchronization did not recognize the group at all. These problems were corrected, empty groups are recognized and users moved between groups now are properly synchronized by ThoughtSpot.

- A problem was resolved where the round function returned a negative zero when it should have returned a 0 (zero).

- Visualizations that relied on chasm trap worksheet were not immediately updated when a formula was changed. The workaround was to manually update the visualization. This was corrected. The system now updates the visualization automatically when an underlying formula is changed.

- On a worksheet with a chasm trap, join between a fact and dimension did not work properly when grouping by a measure on the dimension table. This was fixed.

- Using `safe_divide` and `sum` did not work with formula on formula. This problem was fixed.

- Data connected schedules did not adjust for daylight savings time. Now, the schedules adjust as expected.

- The ThoughtSpot tomcat instance went into crash loop when a generic relationship includes `IS NULL` operator. Now, this relationship no longer causes this problem.

- An ODBC connection between Alteryx and ThoughtSpot was failing. This problem was solved by updating the ODBC drivers to the latest versions.

- An issue was fixed where an unnecessary right-outer join was being applied to row-level security RLS-introduced joins. This situation led to impacts on query performance.

- A problem was resolved with multiple sequential joins. Previously, the proper join path was not used when the fields are pulled from tables that were far apart unless fields from the intermediate tables were also used. Now, ThoughtSpot is able to handle multiple sequential joins.

- Resolved an issue with a chasm trap that used `unique count` on shared dimension. The chasm trap was generating an incorrect query. Now, `unique count` is applied correctly in the final query.

- Previously, a user user that created some row-level security (RLS) rules was associated with the rules such that deleting the user also deleted the rules. This is no longer the case. If a user creates a set of RLS rules and that user is subsequently deleted, the rules persist in the system.

- An issue was resolved where filters could only be edited in the search bar.

- Intermittent, ambiguous red bar errors related to chasm trap situations were resolved.

- The help for row-level security rules was complicated and hard to parse. This text was improved and moved into the Query Visualizer.