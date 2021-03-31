The latest release of ThoughtSpot Cloud contains several new and enhanced features.

<ul>
<li><a href="{{ site.baseurl }}#mar-cloud-analyst">For the Analyst</a></li>
<li><a href="{{ site.baseurl }}#mar-cloud-business-user">For the Business User</a></li>
<li><a href="{{ site.baseurl }}#mar-cloud-it-ops-engineer">For the IT Ops Engineer</a></li>
<li><a href="{{ site.baseurl }}#mar-cloud-developer">For the Developer</a></li>
</ul>

<h3><a id="mar-cloud-analyst"></a>For the Analyst</h3>

<dl>

<dlentry id="scriptability">
<dt>Scriptability</dt>
<dd><ul><li><p><strong>Add tables and columns to an Embrace connection:</strong> ThoughtSpot now allows you to use TML to edit tables created through <a href="{{ site.baseurl }}/admin/ts-cloud/embrace.html">Embrace</a>, and add columns and tables that already exist in the external database to the connection. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/tml.html#syntax-tables">ThoughtSpot Modeling Language</a> and specify the <code>connection</code> information when adding tables or table columns to an Embrace connection.</p> <p>This feature is in <strong>Beta</strong>; to add columns and tables to an Embrace connection through Scriptability, contact <a href="{{ site.baseurl }}/admin/misc/contact.html">ThoughtSpot Support</a>.</p></li>
<li><p><strong>Improvements to generic join functionality:</strong> The expanded functionality for generic joins in TML files allows the following elements:
<ul><li>Constants: int, double, bool, date, and string</li>
<li>Comparison operators: <code>=</code>, <code>!=</code>, <code>&lt;</code>, <code>&gt;</code>, <code>&lt;=</code>, and <code>&gt;=</code></li>
<li>Columns</li>
<li>Boolean operators: <code>AND</code>, <code>OR</code>, and <code>NOT</code></li></ul> This feature is in <strong>Beta</strong>; to add columns and tables to an Embrace connection through Scriptability, contact <a href="{{ site.baseurl }}/admin/misc/contact.html">ThoughtSpot Support</a>.</p>
</li>
</ul></dd></dlentry>

</dl>

<h3><a id="mar-cloud-business-user"></a>For the Business User</h3>

<dl>

<dlentry id="ts-one-ga">
<dt>ThoughtSpot One GA</dt>
<dd>ThoughtSpot One is now available for all customers. It is on by default. See <a href="{{ site.baseurl }}/end-user/search/search-answers.html">Search Answers</a> and <a href="{{ site.baseurl }}/end-user/thoughtspot-one/thoughtspot-one-homepage.html">ThoughtSpot One home page</a> for more information.</dd>
</dlentry>

<dlentry id="bulk-share">
<dt>Bulk share objects from the ThoughtSpot One home page</dt>
<dd>You can now share multiple objects at a time from the ThoughtSpot One home page. Refer to <a href="{{ site.baseurl }}/end-user/thoughtspot-one/thoughtspot-one-homepage.html#bulk-share">ThoughtSpot One home page</a>.</dd>
</dlentry>


<dlentry id="details-panel">
<dt>Frequent metrics and attributes in the <strong>Details</strong> panel</dt>
<dd>The <strong>Details</strong> panel that appears when you click on a Pinboard visualization while searching across your existing Answers and Pinboards now lists frequent metrics and attributes for that Pinboard. You can determine if a Pinboard search result is useful for you based on the metrics and attributes used most often in that Pinboard.</dd>
</dlentry>

</dl>

<h3><a id="mar-cloud-it-ops-engineer"></a>For the IT Ops Engineer</h3>

<dl>

<dlentry id="search-spotiq">
<dt>Manage advanced search and SpotIQ settings</dt>
<dd>You can now manage advanced search and SpotIQ settings from the Admin Console. You can configure column indexing and enable or disable SpotIQ Analyze and column summaries. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/search-spotiq-settings.html">Manage search and SpotIQ settings</a>.</dd></dlentry>

<dlentry id="email-onboarding">
<dt>Manage email and onboarding settings</dt>
<dd>You can manage certain advanced settings for your organization from the Admin Console. You can customize welcome emails, scheduled emails, and the workflow that allows users to sign up for ThoughtSpot from the login page. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/onboarding-email-settings.html">Manage email and onboarding settings</a>.</dd></dlentry>

<dlentry id="performance-tracking">
<dt>Performance Tracking Pinboard</dt>
<dd>The <a href="{{ site.baseurl }}/admin/ts-cloud/performance-tracking.html">Performance Tracking Pinboard</a> is now accessible from the Admin Console. To view this Pinboard, navigate to the Admin Console by selecting <strong>Admin</strong> from the top navigation bar. Select <strong>App performance</strong> from the side navigation bar in the Admin Console.</dd></dlentry>

</dl>

<h3><a id="mar-cloud-developer"></a>For the Developer</h3>

<dl>

<dlentry id="thoughtspot-embed">
<dt>ThoughtSpot Embed</dt>
<dd>ThoughtSpot cloud now supports embedding ThoughtSpot content in third-party applications. In this release, ThoughtSpot introduces the Visual Embed SDK package <span class="label label-beta">Beta</span> to help developers embed the ThoughtSpot search functionality, pinboards, visualizations, or the full application in their web page, portal, or business solution.</dd>
<dd>For more information on embedding ThoughtSpot, see <a href="{{ site.baseurl }}/admin/ts-cloud/intro-embed.html">ThoughtSpot embedding solution</a>.</dd></dlentry>

<dlentry id="spotdev-portal">
<dt>SpotDev portal</dt>
<dd>ThoughtSpot cloud now includes the <strong>SpotDev</strong> portal <span class="label label-beta">Beta</span> to allow developer users to explore the ThoughtSpot SDK APIs and build sample applications. The <strong>SpotDev</strong> tab in the ThoughtSpot application is available for the users with administrator and developer privileges.</dd>
<dd>The <strong>SpotDev</strong> portal provides a playground for developers and product owners to evaluate the Visual Embed APIs and preview the results. The portal also allows authorized users to rebrand the embedded content, <a href="{{ site.baseurl }}/admin/ts-cloud/customize-style-spotdev.html">customize styles</a>, and <a href="{{ site.baseurl }}/admin/ts-cloud/customize-actions-spotdev.html">add custom menu actions</a> to the embedded instance.</dd><dd>For more information, see <a href="{{ site.baseurl }}/admin/ts-cloud/spotdev-portal.html">SpotDev Portal</a>.</dd></dlentry>

</dl>