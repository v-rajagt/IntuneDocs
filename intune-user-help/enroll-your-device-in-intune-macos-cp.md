---
# required metadata

title: Enroll your Mac with Intune Company Portal | Microsoft Docs
description: Learn how to enroll your Mac in Intune with the Company Portal app.
keywords: Mac OS X, macOS, OS X
author: lenewsad
ms.author: lanewsad
manager: dougeby
ms.date: 11/14/2019
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.subservice: end-user
ms.technology:
ms.assetid: 3bb659cc-9b57-4d19-8631-2c26749fa71c
searchScope:
 - User help

# optional metadata

ROBOTS:  
#audience:
#ms.devlang:
ms.reviewer: elocholi
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-enduser
ms.collection: M365-identity-device-management
---

# Enroll your macOS device using the Company Portal app  

Enroll your macOS device with the Intune Company Portal app to gain secure access to your work or school email, files, and apps.

Organizations typically require you to enroll your device before you can access proprietary data. After your device is enrolled, it becomes *managed*. Your organization can assign policies and apps to the device through a mobile device management (MDM) provider, such as Intune. To get continuous access to work or school information on your device, you must configure your device to match your organization’s policy settings.  

This article describes how to use the Company Portal app for macOS to enroll, configure, and maintain your device so that you meet your organization's requirements.  


## What to expect from the Company Portal app

During initial setup, the Company Portal app requires you to sign in and authenticate yourself with your organization. Company Portal then informs you of any device settings you need to configure to meet your organization's requirements. For example, organizations often set minimum or maximum character password requirements that you'll be required to meet.    

After you enroll your device, Company Portal will always make sure that your device is protected according to your organization's requirements. For example, if you install an app from an untrusted source, Company Portal will alert you and might restrict access to your organization's resources. App protection policies like this one are common. To regain access, you'll likely need to to uninstall the untrusted app. 

If after enrollment your organization enforces a new security requirement, such as multi-factor authentication, Company Portal will notify you. You'll have the chance to adjust your settings so that you can continue to work from your device.  

To learn more about enrollment, see [What happens when I install the Company Portal app and enroll my device?](what-happens-if-you-install-the-Company-Portal-app-and-enroll-your-device-in-intune-macos.md).  

## Get your macOS device managed  
Use the following steps to enroll your macOS device with your organization. Your device must be running macOS 10.12 or later.   

> [!NOTE]
> Throughout this process, you might be prompted to allow Company Portal to use confidential information that's stored in your keychain. These prompts are part of Apple security, and are present on devices running macOS Catalina 10.15 and later. When you get the prompt, type in your password and select **Always Allow**. If you press enter or return on your keyboard, the prompt will instead select **Allow**, which may result in additional prompts.  **Katelynn, is my rewrite accurate? Also when I googled these prompts, I see that these occurred as far back as 2016. Was Catalina around back then? If not, thinking we should just remove that part and just have that they are a part of Apple security. Also, do device users need to enter their device password or keychain password? Or are they one in the same?**

### Install Company Portal app  
1. Visit aka.ms/EnrollMyMac.  
2. The CompanyPortal_2.0.190901-Installer.pkg will download. Launch the installer and continue through the steps. 
3. Agree to the software license agreement. 
4. Authenticate to install the software.   **Katelynn what action do the users take to "authenticate" here? DO they just sign in to something or are we being generic because there are multiple ways for them to authenticate in this step?**
5. Open Company Portal. If you can’t find the app, search for it in Spotlight.  


### Enroll your Mac  


1. Sign in to Company Portal with your work or school account.  
2. Select **Begin**.  

    ![Example screenshot of Company Portal screen., highlighting "Begin" button.](./media/company-portal-mac-begin-1911.PNG)  
3. Review [what your organization can and can't see](what-info-can-your-company-see-when-you-enroll-your-device-in-intune.md) on your enrolled device. Then select **Continue**.  
4. Follow the instructions on the **Install management profile** screen.  

    ![Example screenshot of Company Portal, Install management profile screen, highlighting 3 steps.](./media/install-mgmt-profile-mac-1911.PNG)  
5. After you've installed the management profile, return to Company Portal.   
6. Your organization might require you to update your device settings. When you're done updating settings, tap **Check settings**.    **Katelynn, where does the *How to resolve this* link take users? If it's a specific doc, can you let me know which one?**  

    ![Example screenshot of Company Portal, Update device settings screen, highlighting "Check settings" button.](./media/update-settings-mac-1911.PNG)  
7. When setup is complete, tap **DONE**.  

   ![Example screenshot of Company Portal, "You're all set!" screen, highlighting "Done" button.](./media/setup-done-mac-1911.PNG)  


 ## Troubleshooting and feedback   

If you run into issues during enrollment, you can send Microsoft information about what went wrong. **Katelynn, why do they want to do this--is it purely just to report an app issue? Or will they get some kind of personal resolution from it?**  Go to **Help** > **Send Diagnostic Report**.     **Katelynn, doublechecking... is "Send Diagnostic Report" really all caps as its written here?**

You will receive an incident ID, and you can email the details of the issue to your IT support person.  **Katelynn, do they need to type the details of the issue themselves, as they experienced it, or will they actually have a diagnostic report that they can just attach to the email? Do they include the incident ID in the email or is that just for them to write down for their records?** Look for their contact information on the **Contact** page in the Company Portal app, or check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).  **Katelynn, here is another article we might want to update. Can you review to make sure it's still accurate?: https://docs.microsoft.com/en-us/intune-user-help/send-errors-macos**  
 

Additionally, the Microsoft Intune Company Portal team would love to hear your feedback. Go to **Help** > **Send Feedback** to share your thoughts and ideas.  

## Unverified profiles  
When you view the installed mobile device management (MDM) profiles in **System Preferences** > **Profiles**, some profiles might show an unverified status. As long as the management profile shows a verified status, you don’t need to be concerned.  

The management profile is what defines the MDM channel connection. As long as the management profile is verified, any other profiles delivered to the machine via that channel inherit the security traits of the management profile.  

Also, because those other profiles don’t require individual verifications or manual installation, they're generated and delivered to devices quicker.   **Katelynn, do you think this last sentence is useful to the typical device user? I'm a macOS user and I don't understand this part at all, nor do I care. Haha! But if you think the majority will find it useful, it's fine to keep in.** 

## Updating the Company Portal app

Updating the Company Portal app is done the same way as any other Office app, through Microsoft AutoUpdate for macOS. Find out more about [updating Microsoft apps for macOS](https://support.office.com/article/Check-for-Office-for-Mac-updates-automatically-bfd1e497-c24d-4754-92ab-910a4074d7c1).  

## Next Steps  
Still need help? Contact your company support. For contact information, check the [Company Portal website](https://go.microsoft.com/fwlink/?linkid=2010980).   


