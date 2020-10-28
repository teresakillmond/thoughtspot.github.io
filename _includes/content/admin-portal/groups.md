Before people can log in and use ThoughtSpot, you need to create a username, a
password, and a membership in one or more groups for them. Use the Admin Console to easily create and manage your user groups.

Refer to [Understand groups and privileges]({{ site.baseurl }}/admin/users-groups/about-users-groups.html) to learn about the privileges you can assign to a user or group.

To manage groups, navigate to the Admin Console by clicking on the **Admin** tab from the top navigation bar. Select **Groups** from the side navigation bar that appears.

![Admin Console - Groups]({{ site.baseurl }}/images/admin-portal-groups.png "Admin Console - Groups")

You can use the Admin Console to accomplish the following tasks:
* **Create a group** by clicking on the **+ add group** button
* **Manage an existing group** by clicking on the group you would like to edit: change the group or display name, update the sharing visibility, add a description, edit the group's privileges, change the group's default Pinboard, add an existing group to the group, add a user to the group, or resend or test the welcome email
* **Delete a group** by hovering over a group name, clicking the checkbox that appears, and selecting the **Delete** button

{% include note.html content="ThoughtSpot adds external users, or users that authenticate through SAML or Active Directory, to the <strong>all</strong> group by default. This group has no privileges. You must manually assign users to ThoughtSpot groups to give them privileges, such as <strong>can upload user data</strong>, or <strong>can manage data</strong>." %}

## Related information

Refer to [Create, edit, or delete a group]({{ site.baseurl }}/admin/users-groups/add-group.html) for more detail on how to create and manage groups.