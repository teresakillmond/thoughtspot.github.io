---
title: [Integration guidelines]
last_updated: 4/3/2021
summary: "Before embedding, analyze your integration requirements, choose an embedding approach, and explore the APIs."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

ThoughtSpot recommends that you browse through the following guidelines before you begin embedding.
## Define application workflows

The ThoughtSpot Visual Embed SDK includes a Javascript library to programmatically embed search, pinboards, visualizations, and the full ThoughtSpot experience.

In addition to the Visual Embed SDK, ThoughtSpot provides REST APIs to query data from the ThoughtSpot application. For example, you can construct a search answer using the data APIs and use this link to embed search answers with your application.

Irrespective of the method you use for embedding, make sure you define your application workflows and authentication criteria to enable seamless navigation between the host and embedded interfaces.

## Define user roles and privileges
The ThoughtSpot application integration involves several workflows that require users to have specific privileges:

**ThoughtSpot admin**  
ThoughtSpot administrators who define the authentication workflow and create user groups.  
Access control in ThoughtSpot is managed through the users and groups that are stored locally on ThoughtSpot, even if the users are authenticated using SSO or Trusted Authentication. This means that to provide access to content or system privileges, admin users must create users and groups in ThoughtSpot.                           
For more information, see [Managing Users]({{ site.baseurl }}/admin/ts-cloud/users.html) and [Managing groups]({{ site.baseurl }}/admin/ts-cloud/groups.html).

**Developer**  
Application developers with privileges to use the Developer portal and embed ThoughtSpot components in their host application.  
Developer users can also customize the look and feel of the UI, add custom actions to an embedded visualization or pinboard, and modify security settings such as CORS and CSP.                   
For more information, see [User configuration]({{ site.baseurl }}/admin/ts-cloud/user-role-dev.html).

**Host application admin**
Admin privileges to modify the interfaces of your host application. For example, to embed ThoughtSpot components in a business application or web page, you may require edit access to the host application.

## Define an authentication method
For initial development and testing purposes, you can use the [session APIs]({{ site.baseurl }}/reference/api/session-api.html) to manage ThoughtSpot user logins and sessions. However, ThoughtSpot does not recommend using the session REST API to manage user sessions in production environments. Instead, you can use the SAML SSO or trusted authentication service to authenticate users.

**SAML SSO**  
To provide a seamless login experience for your application users, you can configure SSO and enable SAML authentication, so that the federated users are automatically authenticated to ThoughtSpot.
With SSO, you can use your host application, or an external service as the identity provider, and allow authenticated users to access the ThoughtSpot service.
ThoughtSpot administrators can set up SAML SSO either using the **Admin** console in the ThoughtSpot application.

To use SSO authentication, you must add the identity provider domain as a SAML redirect domain in the **Security Settings** page of the Developer portal.                                                               
For more information, see [Configure SAML]({{ site.baseurl }}/admin/ts-cloud/configure-saml-spotdev.html).

**Trusted Authentication**  
Trusted authentication is a token-based authentication service that uses a central authentication service to authenticate ThoughtSpot users. In a trusted authentication workflow, ThoughtSpot provides the authentication service with a token for a given ThoughtSpot user. This token is used for obtaining trust from the client applications before granting access to ThoughtSpot content.

ThoughtSpot users with administrator privileges can generate a trusted authentication token in the **Security Settings** page of the Developer portal.                                                         
For more information, see [Configure trusted authentication]({{ site.baseurl }}/admin/ts-cloud/trusted-authentication.html).

## Define security settings
Before embedding, you must enable several security settings in the Devloper portal to prevent security vulnerabilities in ThoughtSpot.

**Cross-Origin Resource Sharing**
Cross-Origin Resource Sharing (CORS) domains are the origins from which ThoughtSpot APIs can be called. When you add your host domain for CORS in the Developer portal, ThoughtSpot adds the `access-control-allow-origin` header in its API responses.

**Content Security Policy**
To use the Visual Embed SDK, configure the following content security policy (CSP).

-   **CSP visual embed hosts**                                            
    To allow your host domain to set the **frame-ancestors** CSP policy header and embed a ThoughtSpot object within your application frame, you must add your host domain as a CSP visual embed host.

-   **CSP connect-src**                      
    If you plan to configure custom actions to invoke external URLs, you must add these URLs to the **CSP connect-src** domain list in the Developer portal.

For more information, see [Configure security settings]({{ site.baseurl }}/admin/ts-cloud/security-settings.html).

## Try it out

The ThoughtSpot Developer portal provides a playground for developers to explore the Visual Embed SDK components. The **Playground** offers an interactive coding experience for developers to evaluate the APIs and embed ThoughtSpot search, visualizations, pinboards, or the full ThoughtSpot experience within their host application.                    
For more information, see [ThoughtSpot Developer portal]({{ site.baseurl }}/admin/ts-cloud/spotdev-portal.html).