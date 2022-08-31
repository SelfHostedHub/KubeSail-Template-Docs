---
title: Outline Wiki Azure Login
description:  Outline Wiki Azure Login Docs for KubeSail.com
---
# Microsoft / Azure
*If you do not know how to create all of the Keys Needed, Scroll down to the [Azure Application Guide](#azure-credentials-guide)*

# Kubesail Customization

#### New Install or Exisiting Install of Outine

**NOTICE:** If you are installing fresh, **Please Install** With Random Values in the Google String. Due to the Limit of the Kubesail Editor, It will be easier.

1. Make Sure you are in the namespace where you installed Outline.
2. Click on the ["All Resources"](https://kubesail.com/dashboard/all) button so you can Find your Secrets File.
3. Click on the Secret File labled `Secret/outline`
4. Make sure to Delete the `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` Secret if you do not want Google as a login Method
5. Add the Keys Listed Below. To add them, put the **Key First**, then hit Add. After its added, find it in the list ahd **then put the value of that key in.**
	
	- `AZURE_CLIENT_ID`
	- `AZURE_CLIENT_SECRET`
	- `AZURE_RESOURCE_APP_ID`

6. After the Keys are Entered, Hit Save.
7. After you save the Secret File, Go back to your [Outline Deployment](https://kubesail.com/dashboard/deployment/outline)
9. Once at the outline Deployment, go to the `Status Tab` And Restart the Pods!

If you need any help, ask arround in the [KubeSail Discord](https://discord.gg/aZ76CuYadx)

--- 

# Azure Credentials Guide

## Register an application

-   Go to [portal.azure.com](http://portal.azure.com/)  
    
-   Select “Azure Active Directory”, in the left sidebar select “App registrations”
    
-   Select “+ New registration”
    
-   Choose “Accounts in this organizational directory only”
    
-   For the Redirect Uri choose “Web” and enter the URL: `http://docs.mycompany.com/auth/azure.callback`
    
-   Save the new app
    
-   Make a note of the client id
    

## API permissions

-   Select “API permissions” in the sidebar
    
-   Click on “Add a permission” and add delegated `email` and `profile` permissions from the Microsoft Graph API
    

![Permissions UI in Azure](https://outline-production-attachments.s3-accelerate.amazonaws.com/uploads/292079f8-0319-4111-bb5b-315e8ae8f14e/a1aad607-e8ca-401a-af0d-967d5390c93a/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4EOUDTOVUICLPZ4P%2F20220831%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220831T222418Z&X-Amz-Expires=3600&X-Amz-Signature=1cebc59f45db29c11e65b475f9605e9c9faccfe1fcca0e4381720693a9a9df60&X-Amz-SignedHeaders=host&response-content-disposition=attachment)

Permissions UI in Azure

  

## Certificates and secrets

-   Select “Certificates and secrets” in the left sidebar
    
-   Select “+ New client secret”, name it something like “wiki” and **make a note of the resulting secret value**
    
-   Select “Manifest” in the left sidebar, find the `resourceAppId` and make a **make a note of the value**
    

![resourceAppId](https://outline-production-attachments.s3-accelerate.amazonaws.com/uploads/292079f8-0319-4111-bb5b-315e8ae8f14e/273272f0-1f9a-46b7-a8eb-bcf6ad2024f9/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4EOUDTOVUICLPZ4P%2F20220831%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220831T222418Z&X-Amz-Expires=3600&X-Amz-Signature=4ce9f56fdb7263ca157a912cbb365deb3fac2bd6b582a1fa284f039ff26914d2&X-Amz-SignedHeaders=host&response-content-disposition=attachment)

resourceAppId

Add the values noted from the above process in the following environment variables, once you restart the instance you’ll see a new option to sign-in with Microsoft.



