---
# required metadata

title: Configure Google Chrome for Android devices using Intune 
titleSuffix: Microsoft Intune
description: Use Intune configuration policies with Google Chrome for Android devices. 
keywords:
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 10/04/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: chrisbal
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: 
ms.collection: M365-identity-device-management
---

# Configure Google Chrome for Android devices using Intune 

You can use an Intune app configuration policy to configure Google Chrome for Android devices. The settings for the app can be automatically applied. For example, you can specifically set the bookmarks and the URLs that you would like to block or allow.

## Prerequisites

- Android Enterprise enrollment
- Google Chrome is added as Managed Google Play app

## Configuration steps

Intune admin needs to add Google Chrome into the Managed Google Play store first, below are the steps:

1. Go to the Intune portal > Client apps > Apps, add the **Managed Google Play** app.

   ![Add the Managed Google Play app](./media/manage-android-google-chrome/add-app.png)

1. Go to Managed Google Play, search with **Google Chrome** and approve.

   ![Search and approve Google Chrome](./media/manage-android-google-chrome/search.png)

1. Assign Google Chrome to a user group as the required type. Thus, Google Chrome will be deployed automatically when the device is enrolled into Intune.

Next, Intune admin can follow below steps to create the configuration policy.

1. Go to the **App configuration policies** blade and add the policy.
1. Enter the policy name, choose **Managed devices** under Device enrollment type and **Android** under Platform.

   ![Add Google Chrome Configuration policy](./media/manage-android-google-chrome/add-policy.png)

1. Click Associated app, and then select **Google Chrome**.

   ![Select Google Chrome under Associated app](./media/manage-android-google-chrome/associated-app.png)

1. Click Configuration settings, select **Use configuration designer**, and then click **Add** to select the configuration keys.

   ![Add Use configuration designer](./media/manage-android-google-chrome/configuration.png)

1. Below is the example of the common settings:

   ```asciidoc
   Block access to a list of URLs: ["*"]
   Allow access to a list of URLs: ["baidu.com", "yahoo.com", "chrome://*"]
   Managed Bookmarks: [{"toplevel_name": "My managed bookmarks folder"  },  {"url": "baidu.com",   "name": "Baidu"},  {"url": "youtube.com", "name": "Youtube"},  {"name": "Chrome links",  "children": [{"url": "chromium.org", "name": "Chromium"},    {"url": "dev.chromium.org", "name": "Chromium Developers"}]}]
   Incognito mode availability: Incognito mode disabled
   ```

   ![Common settings](./media/manage-android-google-chrome/common-settings.png)

   With the above setting, the bookmarks will be created, and all websites except baidu.com, yahoo.com and chrome:// will be blocked.

1. Click OK and Add.
1. Assign this configuration policy to a user group.

## User experience

1. Once the Android device is enrolled as Android Enterprise, the managed Google Chrome with the portfolio icon will be deployed automatically.

   ![Managed Google Chrome with the portfolio icon](./media/manage-android-google-chrome/chrome-icon.png)

1. Launch Google Chrome and you will find the settings applied.

   - Bookmarks:

     ![Bookmarks](./media/manage-android-google-chrome/bookmarks.png)

   - Blocked URL:

     ![Blocked URL](./media/manage-android-google-chrome/blocked-url.png)

   - Allow URL:

     ![Allow URL](./media/manage-android-google-chrome/allowed-url.png)

   - Incognito tab:

     ![Incognito tab](./media/manage-android-google-chrome/incognito-tab.png)

## Troubleshooting

1. Check the Intune portal to monitor the policy deployment status.

   ![Monitor the policy deployment status](./media/manage-android-google-chrome/monitor-status.png)

1. Launch Google Chrome and visit **chrome://policy**. We can confirm if the settings are applied successfully.

   ![Confirm settings are applied successfully](./media/manage-android-google-chrome/confirm.png)

## Reference

- [Add app configuration policies for managed Android Enterprise devices](https://docs.microsoft.com/intune/app-configuration-policies-use-android)
- [Chrome Enterprise policy list](https://cloud.google.com/docs/chrome-enterprise/policies/)

**Third-party disclaimer information**

The third-party products that this article discusses are manufactured by companies that are independent of Microsoft. Microsoft makes no warranty, implied or otherwise, about the performance or reliability of these products.

The information and the solution in this document represent the current view of Microsoft Corporation on these issues as of the date of publication. This solution is available through Microsoft or through a third-party provider. Microsoft does not specifically recommend any third-party provider or third-party solution that this article might describe. There might also be other third-party providers or third-party solutions that this article does not describe. Because Microsoft must respond to changing market conditions, this information should not be interpreted to be a commitment by Microsoft. Microsoft cannot guarantee or endorse the accuracy of any information or of any solution that is presented by Microsoft or by any mentioned third-party provider.

## Next steps

- For more information about Android Enterprise fully managed devices, see [Set up Intune enrollment of Android Enterprise fully manage devices](../enrollment/android-fully-managed-enroll.md).
