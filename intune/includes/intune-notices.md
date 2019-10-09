---
title: include file
description: include file
author: ErikjeMS  
ms.service: microsoft-intune
ms.topic: include
ms.date: 03/28/2019
ms.author: erikje
ms.custom: include file
---

These notices provide important information that can help you prepare for future Intune changes and features. 

### Decreasing support for Android device administrator 
Android device administrator, sometimes referred to as *legacy Android management* and released with Android 2.2, is a way to manage Android devices. Improved management functionality is now available with [Android Enterprise](../enrollment/connect-intune-android-enterprise.md) (released with Android 5.0). To move to modern, richer, and more secure device management, Google is decreasing device administrator support in new Android releases.

#### How this change affects you
Google's changes will affect Intune users in the following ways: 
- Intune will support devices that are managed by device administrator and that run Android 10 and later (also known as Android Q) only through June or July of 2020, when the next major Android version is expected.  
- Devices that are managed by device administrator and that run Android 10 or later after June or July of 2020 will no longer be entirely managed.    
- Android devices that are managed by device administrator and that remain on versions earlier than Android 10 won't be affected and can continue to be entirely managed by device administrator.  
- For all devices that run Android 10 and later, Google restricts device administrator management agents like Company Portal from accessing device identifier information. After a device updates to Android 10 or later, this restriction affects Intune users in the following ways: 
    - Network access control for VPNs no longer works.  
    - Devices that use their IMEI or serial number to identify their corporate ownership aren't automatically recognized. 
    - The IMEI and serial number are no longer visible to IT admins in Intune. 
        > [!NOTE]
        > These effects apply only to devices that are managed by device administrator on Android 10 and later. They don't apply to devices that are managed through Android Enterprise. 

#### How to prepare for this change
To avoid reduced functionality in June or July of 2020, we recommend the following precautions:
- Don't onboard new devices into device administrator management.
- If a device is expected to receive an update to Android 10, migrate it from device administrator management to Android Enterprise management or APP or both.

#### Additional information
- See Google's [guidance for migration from device administrator to Android Enterprise](http://static.googleusercontent.com/media/android.com/en/enterprise/static/2016/pdfs/enterprise/Android-Enterprise-Migration-Bluebook_2019.pdf).
- See Google's [documentation on the plan to deprecate the device administrator API](https://developers.google.com/android/work/device-admin-deprecation).

### Updating your Android Company Portal app to the latest version <!--4536963-->
Intune periodically releases updates to the Android Company Portal app. In November 2018, we released a Company Portal update that included a backend switch to prepare for Google's change from their existing notification platform to Firebase Cloud Messaging (FCM). When Google moves to FCM, end users will need to update their Company Portal app to at least the November 2018 release to continue communicating with the Google Play Store.

#### How this change affects you
Our telemetry indicates that you have devices whose Company Portal version is earlier than 5.0.4269.0. If you don't have version 5.0.4269.0 or later, IT-pro device actions like wipe, reset password, available and required app installs, and certificate enrollment might not work as expected. If your devices are enrolled in mobile device management (MDM) in Intune, you can see the Company Portal versions and users by going to **Client apps – Discovered apps**. By selecting earlier versions of the Company Portal app, you can see which end users have an outdated Company Portal app.

#### How to prepare for this change
For Android devices aren't updated, ask the end users to update the Company Portal app through Google Play. Notify your help desk in case a user hasn't been automatically updating the Company Portal app. 

#### Additional information
For more information about Google's FCM platform and change, see [this Google article](https://firebase.google.com/docs/cloud-messaging/).


### New full-screen experience <!--4593669-->
We're rolling out updated create and edit UI experiences to Intune in the Azure portal. These new experiences simplify existing workflows by using a wizard-style format on one blade. This update eliminates "blade sprawl" or any create-and-edit flows that require deep blade journeys. The create workflows will also be updated to include assignments (except for app assignment).

#### How this change affects you
The full-screen experience will be rolled out to Intune at both portal.azure.com and devicemanagement.microsoft.com over the next few months. This update to the UI won't affect the functionality of your existing policies and profiles, but you'll see a slightly modified workflow. When you create new policies, for example, you can set some assignments as part of this flow instead of setting assignments after you create the policy. 

#### How to prepare for this change
You don't need to take any action to prepare for this change. But you can consider updating your IT-pro guidance. We'll update our documentation as this experience rolls out to various blades on Intune in the Azure portal.

#### Additional information 
For more information and for screenshots of the new experience in the console, see [New full-screen experience coming to Intune](https://aka.ms/intune_fullscreen).

### Plan for change: New Windows updates settings in Intune <!-- 4464404 -->
Starting with the August release to the Intune service or 1908, we're adding new **Deadline** settings. You can configure these settings instead of the **Allow user to restart (engaged restart)** settings. We plan to disable the engaged-restart settings in the UI in 1909 or the September update. Then we'll completely remove them from the console near the end of October.

#### How this change affects you
If you manage Windows 10 devices in your environment:

- With the August Intune update or 1908, in the console you'll see both new deadline settings and old engaged-restart settings.
- When both old and new settings are configured, the deadline settings values will override the engaged-restart setting values.
- Deadline settings will replace the **Allow user to restart (engaged restart)** option in the console in the 1910 update.

#### How to prepare for this change
Start using the deadline settings in 1908 by configuring them with the values you want. After you've configured the deadline settings, you can set the engaged-restart setting to **Not configured** to prepare for the removal of the settings in October.

Update your documentation and any automation scripts if you need to.

We'll keep you updated and post a reminder to the message center before we remove the engaged-restart settings.

### Intune App SDK and app protection policies for Android moving to support Android 5.0 and later in October <!--4911065 -->
Intune will support Android 5.x (Lollipop) and later in October. Update any wrapped apps with the latest Intune App SDK, and update your devices.

#### How this change affects you
If you're not using or plan to use either the SDK or APP for Android, this change won't affect you. If you are using the Intune App SDK, be sure to update it to the latest version. Also update your devices to Android 5.x or later. If you don't update, apps won't receive updates, and the experience quality will diminish over time.

Below is a list of common devices that are enrolled in Intune and run Android version 4.x. If you have one of the devices, take steps to make sure that the device will support Android version 5.0 or later. Or make sure it will be replaced with a device that supports Android version 5.0 or later. 

- Samsung SM-T561  
- Samsung SM-T365
- Samsung GT-I9195
- Samsung SM-G800F
- Samsung SM-G357FZ
- Motorola XT1080
- Samsung GT-I9305
- Samsung SM-T231
 
This list isn't exhaustive. You might need to evaluate additional devices.

#### How to prepare for this change
Wrap your apps with the latest Intune App SDK. You might also want to set the **Require minimum OS version (Warning only)** conditional launch setting to notify end users to upgrade their personal devices.

### Nearing the end of support for Windows 7 <!-- 3042987 -->
As we wrote in MC148476 in September 2018 and again in MC176794 in March 2019, Windows 7 reaches the end of extended support on January 14, 2020. At that time, Intune will retire support for devices that run Windows 7 so we can focus on newer technologies and provide great new end-user experiences. After that date, Intune will no longer provide technical assistance and automatic updates that help protect your Windows 7 PCs. Microsoft strongly recommends that you move to Windows 10 before January 2020 to avoid a scenario where you need service or support that's no longer available. 

For more information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

#### How this change affects you
You're receiving this message because you currently manage Windows 7 PCs that use the legacy Intune PC software agent. Because less than a year remains before the end of Windows 7 extended support, we strongly encourage your organization to begin upgrading to Windows 10 as soon as possible. 

PC management capabilities are built directly into the Windows 10 operating system. You no longer need to install a client agent such as the Intune software client for Windows 7. Starting with Windows 8.1, Microsoft uses MDM architecture to provision, configure, update, and manage Windows PCs. After you set up Intune, you can simplify Windows enrollment by [enrolling Windows 10 PCs in Intune](..\windows-enroll.md) through the MDM channel. We recommend that you use this "agentless" MDM solution to manage your Windows 10 PCs.

#### How to prepare for this change
We encourage your organization to immediately consider this action plan:

- Plan to upgrade the Windows 7 fleet to Windows 10 before January 14, 2020.
- Explore [Windows 10 deployment support](https://docs.microsoft.com/windows/deployment/) to learn more about how to upgrade your existing Windows 7 PCs to Windows 10.
- Review the [Desktop App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure?rtc=1) offer through FastTrack, which will help fulfill the Microsoft application compatibility promise.
- Transition devices that are managed by the legacy Intune software client to the Microsoft-recommended solution. Manage Windows 10 through MDM. Enroll all new Windows 10 PCs by using MDM for Intune in the Azure portal.

For more information, see [Intune plan for change: Nearing end of support for Windows 7](https://aka.ms/Windows7_Intune).
