---
title: Outline Wiki GitLab Login
description:  Outline Wiki GitLab Login Docs for KubeSail.com
---
# GitLab

GitLab authentication can be used through Outline’s support for OIDC authentication providers. Self-hosting Outline only supports one team, so once you have authenticated with your GitLab organization additional teams will not be able to be created.

# Kubesail Customization

#### New Install or Exisiting Install of Outine

**NOTICE:** If you are installing fresh, **Please Install** With Random Values or Leave them Empty in the Google Strings. Due to the Limit of the Kubesail Editor, It will be easier to change out later.

1. Make Sure you are in the namespace where you installed Outline.
2. Click on the ["All Resources"](https://kubesail.com/dashboard/all) button so you can Find your Secrets File.
3. Click on the Secret File labled `Secret/outline`
4. Make sure to Delete the `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` Secret if you do not want Google as a login Method. Google is the Defualt Login Method When Installed
5. Add the Keys Listed Below. To add them, put the **Key First**, then hit Add. After its added, find it in the list ahd **then put the value of that key in.** (`gitlab.example.com` should be replaced with either the cloud hosted or self hosted installation url.)

|Key| Example Value |
|--|--|
|OIDC_AUTH_URI  | https://gitlab.example.com/oauth/authorize |
|OIDC_TOKEN_URI  |https://gitlab.example.com/oauth/token  |
|OIDC_USERINFO_URI | https://gitlab.example.com/oauth/userinfo |
|OIDC_USERNAME_CLAIM | username |
| OIDC_DISPLAY_NAME |GitLab|
| OIDC_SCOPES | openid, email |

6. After the Keys are Entered, Hit Save.
7. After you save the Secret File, Go back to your [Outline Deployment](https://kubesail.com/dashboard/deployment/outline)
8. Once at the outline Deployment, go to the `Status Tab` And Restart the Pods!
9. Once the App Is started, Follow the [Security Section Below](#security)

If you need any help, ask arround in the [KubeSail Discord](https://discord.gg/aZ76CuYadx)


## Security

Once signed into Outline you should make sure to add authorized domain names under **Settings** → **Security** to restrict access to your installation.