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

Mobile threat defense apps protect you against security threats by finding and alerting you to suspicious apps or third-party content on your device.  

Organizations often require employees and students to install a mobile threat defense app on their devices. If the app detects a threat on your device, it will block you from accessing school or work apps. It will provide you with immediate information to help you resolve the threat and regain access.  

There are a variety of mobile threat defense apps available to install; your organization will let you know which one to use. In this article, you will learn how to:

* Register your device with your organization, if you haven't done it already
* Install a mobile threat defense app 


## Information your organization can see   

Your organization can't see any data, such as texts, emails, and pictures, in your personal apps. The mobile threat defense app does report information about your apps, such as name and version, to the Mobile Threat Defense service that your company uses. The details shared depend on the service your company uses. Your organization might see:   

* App name  
* App ID: The unique name that identifies the app in the Play Store.  
* App version and short version number: The specific release numbers for an app.  
* App bundle and dynamic size: The amount of space an app uses on your device.    

LN notes: Ended here--editing resuming on 10/22 

## Install app    
 Before you begin the steps in this section, make sure you:  

* For iOS: Install Microsoft Authenticator app and sign in with your work or school. 
* For Android: Install the Company Portal app and sign in with your work or school account. 

These two steps are neccessary to confirm your school or work identity with your organization.  From Laura: Is this accurate?

### iOS setup  

1. When prompted to register your device, select **Register**. From Laura: If they already have the MS AUthenticator/CP set up, will they still see this prompt?  
2. Install the mobile threat defense app that's required by your organization. 
    a. Select **Download from App Store**.  
    b. A reminder appears. Read it and then select **OK**.
    c. The App Store opens the app details page. Install the app but don't open it yet.   
    d. Return to the app you were trying to access. 
3. Intune MAM Diagnostic App will ask you for permission to open the mobile threat defense app. Select **Open**. From Laura: Is it always going to be the app that they were trying to access that's asking for the permission? So if they were trying to access Outlook, would it say "Outlook wants to open this mobile threat defense app?"
4. The mobile threat defense app will ask you for permission to open Microsoft Authenticator. Select **Open**. 
5. Select your work account. The mobile threat defense app will use this account to sign you in.  From Laura: SHould users go back to the MAM diagnostic app as soon as the mtd app signs them in--or do they wait for the scan to complete (step 6)?
6. The mobile threat defense app will begin scanning your device for security threats. 
7.  Return to the school or work app that you were originally trying to access.  
8. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device. 
9. Return to the app. If you still don't have access:  
    * Select **Recheck,** if available in the school or work app.  
    * Check the mobile threat defense app for existing threats. Complete the recommended steps to resolve the threat and regain access.    

### Android setup 
1. When prompted to register your device, select **Register**. 
2. Install the mobile threat defense app that's required by your organization. 
    a. Select **Download** to open the Google Play store.  
    b. Install the app.  
3. The mobile threat defense app asks for permission to access your contacts and location. **Allow** the access to continue.  From Laura: Is this something that's required for both aspects--contacts and location? Can they continue if they select deny?
4. Select your work account. The mobile threat defense app will use this account to sign you in.
6. The mobile threat defense app will begin scanning your device for security threats.
9. Return to the school or work app that you were originally trying to access.
10. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device.  From Laura: Is this PIN specific to this app or is it for all of the school or work data/apps?
11. Return to the app. If you still don't have access:  
    * Select **Recheck,** if available in the school or work app.  
    * Check the mobile threat defense app for existing threats. Complete the recommended steps to resolve the threat and regain access.   

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

