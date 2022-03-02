# Keycloak, Oauth, OpenID connect, SAML



Keycloak is an authentication framework provided Redhat.



**OAuth 2.0:** If you’ve ever signed up to a new application and agreed to let it automatically source new contacts via Facebook or your phone contacts, then you’ve likely used OAuth 2.0. This standard provides secure delegated access. That means an application can take actions or access resources from a server on behalf of the user, without them having to share their credentials. It does this by allowing the [identity provider (IdP)](https://www.okta.com/identity-101/why-your-company-needs-an-identity-provider/) to issue tokens to third-party applications with the user’s approval.

**OpenID Connect:** If you’ve used your Google to sign in to applications like YouTube, or Facebook to log into an online shopping cart, then you’re familiar with this authentication option. OpenID Connect is an open standard that organizations use to authenticate users. IdPs use this so that users can sign in to the IdP, and then access other websites and apps without having to log in or share their sign-in information.&#x20;

**SAML:** You’ve more likely experienced SAML authentication in action in the work environment. For example, it enables you to log into your corporate intranet or IdP and then access numerous additional services, such as Salesforce, Box, or Workday, without having to re-enter your credentials. SAML is an XML-based standard for exchanging authentication and authorization data between IdPs and service providers to verify the user’s identity and permissions, then grant or deny their access to services.



Group in Keycloak is not part of authentication protocol provided by openid



Scopes - space seperated list of identifiers used to specify what privileges are requestion

Claims - information of user

Response type - Authorization, implicit, explicit



{% embed url="https://www.okta.com/identity-101/whats-the-difference-between-oauth-openid-connect-and-saml" %}

{% embed url="https://developer.okta.com/blog/2017/07/25/oidc-primer-part-1" %}
