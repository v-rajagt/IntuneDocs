---
# required metadata

title: Install Mobile Threat Defense on your mobile device
description: Learn how to install Mobile Threat Defense on your mobile device.
keywords:
author: lenewsad
ms.author: lanewsad  
manager: dougeby
ms.date: 10/22/2019
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.subservice: end-user
ms.technology:
ms.assetid: 
searchScope:
 - User help

# optional metadata

ROBOTS:  
#audience:
#ms.devlang:
#ms.reviewer: aanavath  
#ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-enduser
ms.collection: M365-identity-device-management
---  

# Install Mobile Threat Defense   

Install Mobile Threat Defense to sign in to your work account from your device, and protect yourself against security threats. Mobile Threat Defense finds and alerts you to suspicious apps or third-party contacts on your device. It also helps your resolve them. 

Organizations often require you to install a Mobile Threat Defense app before you can sign in to apps with your work or school account.  

---LN note: going to move this to a diff. section---You might see different prompts on your device, depending on which Mobile Threat Defense service your IT admin set it up.

## Information your organization can see   

Your organization can't see any data, such as texts, emails, and pictures, in your personal apps. Mobile Threat Defense does report information about your apps, such as name and version, to the Mobile Threat Defense service that your company uses. The details shared depend on the service your company uses. Your organization might see:   

* App name  
* App ID: The unique name that identifies the app in the Play Store.  
* App version and short version number: The specific release numbers for an app.  
* App bundle and dynamic size: The amount of space an app uses on your device.    

LN notes: Ended here--editing resuming on 10/22 

## Set up threat protection on your device  
Setting up threat protection requires you to:

* Register your device  
* Install the Mobile Threat Defense app that's required by your organization  

### Device registration
Register your device to confirm your identity with your organization. This step is required to access your organization's resources on your device.   

 To register your device:

* iOS: Install Microsoft Authenticator app and sign in with your work or school. 
* Android: Install the Company Portal app and sign in with your work or school account. 

Follow the onscreen prompts to complete registration. If you're not sure if your device is registered, the Mobile Defense App that you install will let you know, and provide next-step instructions.    

### App installation  
Your organization will make the app available to you through one of the following ways:  

* Your organization might install the app on your device so that it's ready to use when you turn the device on. This applies to corporate-owned devices only. 

*  

* 

1. Install the Mobile Threat Defense app.
2. Sign in with your work or school account.
3. Follow the prompts within the app to complete setup. 


Next, in order for the Mobile Threat Defense service to do a scan of a particular device, it needs to have the corresponding Mobile Threat Defense client app installed. Again, Intune helps you with that process with guided setup instructions within your Intune protected app. 

Make sure you have signed in with your corporate account into the Mobile Threat Defense client app. 




After setup is complete, you should have access to your organization's email, Wi-Fi, and apps.  



Lastly, once you have installed and signed in to all the required apps on your device, you may have to hit 'Recheck' within your Intune protected app, such as Microsoft Outlook. This is to get a status update to confirm the connection between services is working correctly. 

Now, you should be able to use your Intune protected apps as normal unless your device ever does not meet the threat level set by your IT admin. 

## What permissions does an end user need to accept? 

On Android, 'Allow contacts' needs to be an accepted permission for a proper connection to the Mobile Threat Defense connector to be correctly set up.

## If the installation doesn't work

Sometimes installations can fail due to technical issues beyond your control. If this happens, contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).

On Android, for information on how to send logs to someone who can help, check [Upload and email logs from Company Portal](https://docs.microsoft.com/en-us/intune-user-help/send-logs-to-your-it-admin-by-email-android). 

On iOS, for information on how to send logs to someone who can help, check [Use Microsoft Edge on iOS to access managed app logs](https://docs.microsoft.com/en-us/intune/apps/manage-microsoft-edge#use-microsoft-edge-on-ios-to-access-managed-app-logs). 

## Resolve a threat found by a Mobile Threat Defense app

Mobile Threat Defense apps detect and alert you to potential threats on your devices. Some organizations integrate a Mobile Threat Defense service with an Enterprise Mobility Management vendor (EMM), like Intune. When the connector is set up, the Mobile Threat Defense service reports the threats (such as suspicious apps, networks, and OS vulnerabilities) and notifies you within any [Intune protected app](https://docs.microsoft.com/en-us/intune/apps/apps-supported-intune-apps) that is targeted with your organization's policy. This threat notification may come as a block from corporate data access or as a selective wipe of corporate data, depending on IT admin intent. 

Threat notifications appear to you the within an Intune protected app, such as Microsoft Outlook, as a dialog indicating that your access is blocked. As long as these threats are present on your device, you may be unable to:  

* Access your corporate data via your corporate account in an Intune protected app
* Access other company apps 

You can find details about the threat(s) and remediation steps in the Mobile Threat Defense app to get access to corporate data again. You may have to hit a 'Recheck' button within the Intune protected app, to get a status update to confirm the threat on your device is indeed remediated. 

Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980) 

On Android, for information on how to send logs to someone who can help, check [Upload and email logs from Company Portal](https://docs.microsoft.com/en-us/intune-user-help/send-logs-to-your-it-admin-by-email-android). 

On iOS, for information on how to send logs to someone who can help, check [Use Microsoft Edge on iOS to access managed app logs](https://docs.microsoft.com/en-us/intune/apps/manage-microsoft-edge#use-microsoft-edge-on-ios-to-access-managed-app-logs). 


Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).

