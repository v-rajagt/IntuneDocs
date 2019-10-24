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

As part of their app security requirements, organizations often require employees and students to install a mobile threat defense app. This type of app detects and alerts you to threats on your device, such as suspicious apps, networks, or OS vulnerabilities.  

If you don't have the required app, your organization can limit your access to the school or work data in your apps. You'll receive a notification to install the app. This article describes [how to install the app](set-up-mobile-threat-defense.md#install-app) and get access.  

When a threat is detected, your organization can limit your access to the school or work data in your apps. Your organization could also erase this data from your apps. The mobile threat defense app provides information about the threat and how to resolve it to regain access. See [how to resolve a threat]() in this article for more information. 

There are a variety of mobile threat defense apps available to install; your organization will let you know which one to use. 


## Information your organization can see   

Your organization can't see any data, such as texts, emails, and pictures, in your personal apps. The mobile threat defense app does report information about your apps, such as name and version, to your organization. The actual reported information depends on the mobile threat defense service your company uses. Your organization might see:   

* App name  
* App ID: The unique name that identifies the app in the Play Store.  
* App version and short version number: The specific release numbers for an app.  
* App bundle and dynamic size: The amount of space an app uses on your device.    

## Install app    
 Before you begin the steps in this section, make sure you:  

* For iOS: Install Microsoft Authenticator app and sign in with your work or school. 
* For Android: Install the Company Portal app and sign in with your work or school account. 

These two steps are necessary to confirm your school or work identity with your organization.  **From Laura: Is this an accurate explanation**?  

### iOS setup  
After you're blocked from signing in to an app, you'll receive a prompt to register or protect your device. Complete these steps to regain access to the app.

1. Select **Register**. **From Laura: Will everyone get the "Register" prompt/button, whether they've registered or now. 
2. From the **Get access** screen, install the mobile threat defense app that's required by your organization. 
    1. Select **Download from App Store**.
    2. A reminder appears. Read it and then select **OK**.
    3. The App Store opens the app details page. Install the app but don't open it yet.   
    4. Return to the app you were trying to access. 
3. Intune MAM Diagnostic App will ask you for permission to open the mobile threat defense app. Select **Open**.  **From Laura: Is it always going to be the app that they were trying to access that's asking for the permission? So if they were trying to access Outlook, would it say "Outlook wants to open this mobile threat defense app?"**
4. The mobile threat defense app will ask you for permission to open Microsoft Authenticator. Select **Open**. 
5. Select your work account to sign you in.  **From Laura: SHould users go back to the MAM diagnostic app as soon as the mtd app signs them in--or do they wait for the scan to complete (step 6)?**
6. The mobile threat defense app will begin scanning your device for security threats. 
7.  Return to the school or work app that you were originally trying to access.  
8. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device. 
9. Return to the app. If you still don't have access:  
    * Select **Recheck,** if available in the school or work app.  
    * Check the mobile threat defense app for existing threats. Complete the recommended steps to resolve the threat and regain access.    

### Android setup 
After you're blocked from signing in to an app, you'll receive a prompt to register or protect your device. Complete these steps to regain access to the app.  

1. When prompted to register your device, select **Register**. **From Laura: Same question here about what users see to launch them into this flow--will it always be "Register?"**
2. From the **Get access** screen, install the mobile threat defense app that's required by your organization.  
    a. Select **Download** to open the Google Play store.  
    b. Install the app.  
3. The mobile threat defense app will ask for permission to access your contacts and location. In order for the app to work correctly, you must **Allow** access to contacts.  
4. Select your work account. The mobile threat defense app uses this account to sign you in.
5. The mobile threat defense app will begin scanning your device for security threats.
6. Return to the school or work app that you were originally trying to access.
7. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device.  **From Laura: Is this PIN specific to this app or is it for all of the school or work data/apps?**
8. Return to the app. If you still don't have access:  
    * Select **Recheck,** if available in the school or work app.  
    * Check the mobile threat defense app for existing threats. Complete the recommended steps to resolve the threat and regain access.   

### Installation failed 

If the installation fails, contact your IT support person. Go to the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980) to find your organization's contact information.  

You can also send your app logs to your IT support person to provide them with more context about the installation.  
* Android users: [Upload and email your logs](https://docs.microsoft.com/intune-user-help/send-logs-to-your-it-admin-by-email-android) from Company Portal.   

* iOS device users: [Retrieve and send your logs](https://docs.microsoft.com/intune/apps/manage-microsoft-edge#use-microsoft-edge-on-ios-to-access-managed-app-logs) from Microsoft Edge for iOS.  

## Resolve a threat  

Mobile Threat Defense apps detect and alert you to potential threats on your devices. Some organizations integrate a Mobile Threat Defense service with an Enterprise Mobility Management vendor (EMM), like Intune. When the connector is set up, the Mobile Threat Defense service reports the threats (such as suspicious apps, networks, and OS vulnerabilities) and notifies you within any [Intune protected app](https://docs.microsoft.com/en-us/intune/apps/apps-supported-intune-apps) that is targeted with your organization's policy. This threat notification may come as a block from corporate data access or as a selective wipe of corporate data, depending on IT admin intent. 

Threat notifications appear to you the within an Intune protected app, such as Microsoft Outlook, as a dialog indicating that your access is blocked. As long as these threats are present on your device, you may be unable to:  

* Access your corporate data via your corporate account in an Intune protected app
* Access other company apps 

You can find details about the threat(s) and remediation steps in the Mobile Threat Defense app to get access to corporate data again. You may have to hit a 'Recheck' button within the Intune protected app, to get a status update to confirm the threat on your device is indeed remediated. 

Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980) 

On Android, for information on how to send logs to someone who can help, check [Upload and email logs from Company Portal](https://docs.microsoft.com/en-us/intune-user-help/send-logs-to-your-it-admin-by-email-android). 

On iOS, for information on how to send logs to someone who can help, check [Use Microsoft Edge on iOS to access managed app logs](https://docs.microsoft.com/en-us/intune/apps/manage-microsoft-edge#use-microsoft-edge-on-ios-to-access-managed-app-logs). 


Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).

