---
title: Outline Wiki Slack Login
description:  Outline Wiki Slack Login Docs for KubeSail.com
---
# Slack
*If you do not know how to create all of the Keys Needed, Scroll down to the [Slack Credentials Guide](#slack-credentials-guide)*

# Kubesail Customization

#### New Install or Exisiting Install of Outine

**NOTICE:** If you are installing fresh, **Please Install** With Random Values or Leave them Empty in the Google Strings. Due to the Limit of the Kubesail Editor, It will be easier to change out later.

1. Make Sure you are in the namespace where you installed Outline.
2. Click on the ["All Resources"](https://kubesail.com/dashboard/all) button so you can Find your Secrets File.
3. Click on the Secret File labled `Secret/outline`
4. Make sure to Delete the `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` Secret if you do not want Google as a login Method. Google is the Defualt Login Method When Installed
5. Add the Keys Listed Below. To add them, put the **Key First**, then hit Add. After its added, find it in the list ahd **then put the value of that key in.**
	- `SLACK_KEY` (This is called "Client ID" in Slack)
	- `SLACK_SECRET` (This is called "Client Secret" in Slack)

6. After the Keys are Entered, Hit Save.
7. After you save the Secret File, Go back to your [Outline Deployment](https://kubesail.com/dashboard/deployment/outline)
8. Once at the outline Deployment, go to the `Status Tab` And Restart the Pods!

If you need any help, ask arround in the [KubeSail Discord](https://discord.gg/aZ76CuYadx)

--- 

# Slack Credentials Guide
In this guide `docs.mycompany.com` will be used to represent the location you’re hosting Outline, it should be replaced with the correct value. This guide only covers setting up Slack for authentication – if you are looking to setup Slack commands / posting see the [integrations page](https://app.getoutline.com/doc/slack-G2mc8DOJHk).

## Register an application

-   Go to [https://api.slack.com/apps](https://api.slack.com/apps)  
    
-   Click the “Create New App” button
    
-   Give your app a recognizable name, icon, description etc.
    
-   Save the new app
    

## OAuth & Permissions

-   Go to “OAuth & Permissions” in the left sidebar
    
-   For the Redirect URL add the following: `https://docs.mycompany.com/auth/slack.callback` – Note that Slack requires this url is HTTPS. If you are locally developing the software a valid certificate can be generated easily with [mkcert](https://mkcert.dev/).
    
-   Under “Scopes” the following are required:
    
    -   `identity.avatar`
        
    -   `identity.basic`
        
    -   `identity.email`
        
    -   `identity.team`
        

## Configuration

In your Outline environment set the following variables, the values can be found under “Basic information” in the Slack interface.

	- `SLACK_KEY` (This is called "Client ID" in Slack)
	- `SLACK_SECRET` (This is called "Client Secret" in Slack)