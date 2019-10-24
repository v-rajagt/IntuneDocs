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

As part of your organization's security requirements, you might be required to install a Mobile Threat Defense (MTD) vendor app. This type of app detects and alerts you to threats on your device, such as suspicious apps, networks, or OS vulnerabilities.  

If you don't have the required MTD app, you'll be blocked from signing in to protected apps with your work or school account. This article describes [how to install an MTD app](set-up-mobile-threat-defense.md#install-app) and get access to your school or work data.  

There are a variety of MTD vendor apps available to install; your organization will let you know which one to use. 


## Information your organization can see   

Your organization can't see any data, such as texts, emails, and pictures, in your personal apps. The MTD app does report information about your apps, such as name and version, to your organization. The actual information reported depends on the MTD vendor your company uses. Your organization might see:   

* App name  
* App ID: The unique name that identifies the app in Google Play.  
* App version and short version number: The specific release numbers for an app.  
* App bundle and dynamic size: The amount of space an app uses on your device. 


## Install app    
 Before you install the app, make sure you:  

* For iOS: Install Microsoft Authenticator app and sign in with your work or school account. 
* For Android: Install the Company Portal app and sign in with your work or school account. 

These two steps are necessary to confirm your school or work identity with your organization.  **From Laura: Is this an accurate explanation**?  

### iOS setup  
After you're blocked from signing in to an app, you are prompted to register or protect your device with an MTD app. Complete these steps to regain access to the app.  

1. Select **Register**. **From Laura: Will everyone get the "Register" prompt/button, whether they've registered or not?**
2. From the **Get access** screen, install the MTD app that's required by your organization. 
    1. Select **Download from App Store**.
    2. A reminder appears. Read it and then select **OK**.
    3. The App Store opens the app details page. Install the app but don't open it yet.   
3. On the **Get access** screen, select **Open**.  
4. The MTD app asks for permission to open Microsoft Authenticator. Select **Open**. 
5. Select your work account to sign in.  **From Laura: SHould users go back to the MAM diagnostic app as soon as the mtd app signs them in--or do they wait for the scan to complete (step 6)?**
6. Wait while the MTD app scans your device for security threats. 
7. Return to the school or work app that you were originally trying to access.  
8. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device. 
9. Return to the app. If you still don't have access:  
    * On the **Get access** screen, select **Recheck**.    
    * Check the MTD app for existing threats. Complete the recommended steps to resolve the threat and regain access.    

### Android setup 
After you're blocked from signing in to an app, you are prompted to register or protect your device. Complete these steps to regain access to the app.  

1. Select **Register**. **From Laura: Same question here about what users see to launch them into this flow--will it always be "Register?"**
2. From the **Get access** screen, install the MTD app that's required by your organization.  
    a. Select **Download** to open the Google Play store.  
    b. Install the app.  
3. The MTD app asks for permission to access your contacts and location. In order for the app to work correctly, you must **Allow** access to contacts.  
4. Select your work account to sign in. 
5. Wait while the MTD app scans your device for security threats.  
6. Return to the school or work app that you were originally trying to access.
7. When prompted to, create a PIN that's easy for you to remember. You'll use this PIN to authenticate yourself when accessing school or work data from your device.  **From Laura: Is this PIN specific to this app or is it for all of the school or work data/apps?**
8. Return to the app. If you still don't have access:  
    * On the **Get access** screen, select **Recheck**.  
    * Check the MTD app for existing threats. Complete the recommended steps to resolve the threat and regain access.   

### Installation failed 

If the installation fails, contact your IT support person. Go to the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980) to find your organization's contact information.  

You can also send your app logs to your IT support person to provide them with more context about the installation.  
* Android users: [Upload and email your logs](https://docs.microsoft.com/intune-user-help/send-logs-to-your-it-admin-by-email-android) from Company Portal.   

* iOS device users: [Retrieve and send your logs](https://docs.microsoft.com/intune/apps/manage-microsoft-edge#use-microsoft-edge-on-ios-to-access-managed-app-logs) from Microsoft Edge for iOS.  

## Resolve a threat  
If a threat exceeds your organization's defined threat level, your organization will either:  
   
* Block access: Blocks you from using your organization's protected apps while signed in to your work or school account.  
* Wipe data: Deletes your work or school data from one or more of your organization's protected apps.    

To resolve a threat and regain access, open the MTD app on your device. Read through the provided information to learn how the threat could affect your device and how to resolve it. After you follow the steps to resolve the threat, go back to the MTD app and initiate a new scan. It might take a few minutes to regain access to your organization.  

## Next steps  

Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).

