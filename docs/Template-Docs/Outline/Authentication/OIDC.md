---
title: Outline Wiki ODIC Login
description:  Outline Wiki ODIC Login Docs for KubeSail.com
---
# ODIC
Outline supports all OIDC-compatible authentication providers out of the box. Currently the OIDC configuration must be provided manually as environment variables; the following values are supported:

-   `OIDC_CLIENT_ID` – OAuth client ID
    
-   `OIDC_CLIENT_SECRET` – OAuth client secret
    
-   `OIDC_AUTH_URI`
    
-   `OIDC_TOKEN_URI`
    
-   `OIDC_USERINFO_URI`
    
-   `OIDC_USERNAME_CLAIM` – Supports any valid JSON path with the JWT payload (“preferred\_username” by default)
    
-   `OIDC_DISPLAY_NAME` – The text that should be displayed on the login button (OpenID by default)
    
-   `OIDC_SCOPES` – Default is “openid profile email”

See [Examples Below](#examples)

# Kubesail Customization

#### New Install or Exisiting Install of Outine

**NOTICE:** If you are installing fresh, **Please Install** With Random Values or Leave them Empty in the Google Strings. Due to the Limit of the Kubesail Editor, It will be easier to change out later.

1. Make Sure you are in the namespace where you installed Outline.
2. Click on the ["All Resources"](https://kubesail.com/dashboard/all) button so you can Find your Secrets File.
3. Click on the Secret File labled `Secret/outline`
4. Make sure to Delete the `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` Secret if you do not want Google as a login Method. Google is the Defualt Login Method When Installed
5. Add the Keys that can be used are listed below (Only Used what is Required for your ODIC Installation). To add them, put the **Key First**, then hit Add. After its added, find it in the list ahd **then put the value of that key in.**

-   `OIDC_CLIENT_ID` – OAuth client ID
    
-   `OIDC_CLIENT_SECRET` – OAuth client secret
    
-   `OIDC_AUTH_URI`
    
-   `OIDC_TOKEN_URI`
    
-   `OIDC_USERINFO_URI`
    
-   `OIDC_USERNAME_CLAIM` – Supports any valid JSON path with the JWT payload (“preferred\_username” by default)
    
-   `OIDC_DISPLAY_NAME` – The text that should be displayed on the login button (OpenID by default)
    
-   `OIDC_SCOPES` – Default is “openid profile email”
  
1. After the Keys are Entered, Hit Save.
2. After you save the Secret File, Go back to your [Outline Deployment](https://kubesail.com/dashboard/deployment/outline)
3. Once at the outline Deployment, go to the `Status Tab` And Restart the Pods!



### Examples

OIDC providers will often publish the correct values for these at the “.well-known” url, some examples that could be used to sign-in to Outline using this method include:

-   **GitLab**: [https://gitlab.com/.well-known/openid-configuration](https://gitlab.com/.well-known/openid-configuration)  
    
-   **Apple**: [https://appleid.apple.com/.well-known/openid-configuration](https://appleid.apple.com/.well-known/openid-configuration)  
    
-   **Twitch:** [https://id.twitch.tv/oauth2/.well-known/openid-configuration](https://id.twitch.tv/oauth2/.well-known/openid-configuration)  
    
-   **Facebook:** [https://www.facebook.com/.well-known/openid-configuration](https://www.facebook.com/.well-known/openid-configuration)  
    
-   **Keycloak:** [https://www.keycloak.org/](https://www.keycloak.org/) (self-hosted)
    
-   **Mattermost:** [https://developers.mattermost.com/integrate/admin-guide/admin-oauth2/#oauth-endpoints](https://developers.mattermost.com/integrate/admin-guide/admin-oauth2/#oauth-endpoints) (self-hosted and cloud)
    
-   **Authelia:** [https://www.authelia.com/configuration/identity-providers/open-id-connect/](https://www.authelia.com/configuration/identity-providers/open-id-connect/) (self-hosted)