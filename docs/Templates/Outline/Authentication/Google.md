---
title: Outline Wiki Google Login
description:  Outline Wiki Google Login Docs for KubeSail.com
---
# Google
***Using Google as an OAuth provider is only supported if you are using Google Workspace***

---

# KubeSail Customization

*If you do not know how to create all of the Keys Needed, Scroll down to the [Google Credentials Guide](#google-credentials-guide)*
#### New Install or Exisiting Install of Outine
1. Edit The App Values, and add the Variables noted above to `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`


---
# Google Credentials Guide

In this guide `docs.mycompany.com` will be used to represent the location you are hosting Outline, it should be replaced with the correct value.
## Create a project

-   Go to [https://console.cloud.google.com](https://console.cloud.google.com/)  
    
-   Create a project or use an existing one
    

## API's & Services

-   Go to [APIs & Services](https://console.cloud.google.com/apis/dashboard)  
    
-   Click “Enable APIs and Services”
    
-   Enable the [Google+ API](https://console.cloud.google.com/apis/library/plus.googleapis.com)  
    

## OAuth consent screen

-   Go to [OAuth consent screen](https://console.cloud.google.com/apis/credentials/consent)  
    
-   Select `Internal` for the user type and click “Create” – If you are not a Google Workspace user you will not be able to select this option. It is advisable to use a different method of auth.
    
-   Choose an “App name”
    
-   Make sure that “Authorized domains” includes the domain you are using for Outline
    

## Credentials

-   Go to [Credentials](https://console.cloud.google.com/apis/credentials)  
    
-   Click on “Create credentials” and select “OAuth client ID”
    
-   Choose `Web application` as the application type
    
-   Under “Authorized JavaScript origins” enter your domain name again
    
-   Under “Authorized redirect URIs” enter the URL (replacing the domain name): `http://docs.mycompany.com/auth/google.callback`
    
-   Click “Save”
    
-   Make a note of the Client ID and Secret values



