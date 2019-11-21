---
# required metadata

title: Add preference file settings to macOS devices in Microsoft Intune - Azure | Microsoft Docs
titleSuffix:
description: Add an xml or plist file that includes key information about your app bundle
keywords:
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 11/20/2019
ms.topic: reference
ms.service: microsoft-intune
ms.subservice: configuration
ms.localizationpriority: medium
ms.technology:

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Use 

Using Microsoft Intune, you can add a property list file (.plist) for your macOS devices.

Property list files typically include user settings, or information about bundles and applications. For more information on property lists, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (opens Apple's website).

This article lists and describes the different settings you can control on macOS devices. As part of your mobile device management (MDM) solution, use these settings to add the app bundle ID, and add a .plist file.

These settings are added to a device configuration profile in Intune, and then assigned or deployed to your macOS devices.

## Before you begin

[Create the profile](device-profile-create.md).

## What you need to know

- These settings aren't validated. Be sure to test your changes before assigning the profile to your devices.
- If you’re not sure how to enter an app key, change the setting within the app. Then, review the app's preference file using [Xcode](https://developer.apple.com/xcode/) to see how the setting is configured. Apple recommends removing non-manageable settings using Xcode before importing the file.
- Only some apps work with managed preferences, and might not allow you to manage all settings.

## Preference file

- **Preference domain name**: Property list files are typically used for custom apps. When you create a custom app, a bundle ID is automatically created. Enter the bundle ID of your app. For example, enter `com.Microsoft.Edge`.

- **Property list file**: Select the property list file associated with your app. Be sure it's a `.plist` or `.xml` file. For example, upload a `YourApp-Manifest.plist` file.
- **File contents**: 

Select **OK** > **Create** to save your changes. The profile is created and shown in the profiles list.

## Next steps

The profile is created, but it's not doing anything yet. Next, [assign the profile](device-profile-assign.md) and [monitor its status](device-profile-monitor.md).
