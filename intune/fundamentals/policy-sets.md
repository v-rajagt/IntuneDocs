---
# required metadata

title: Policy sets 
titleSuffix: Microsoft Intune
description: Use policy sets to group collections of management objects in Microsoft Intune.
keywords:
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 10/14/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.localizationpriority: high
ms.technology:
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: craigma
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Use policy sets to group collections of management objects

Policy sets allow you to create a bundle of references to already existing management entities that need to be identified, targeted, and monitored as a single conceptual unit. A policy set is an assignable collection of apps, policies, and other management objects you've created. Creating a policy set enables you to select many different objects at once, and assign them from a single place. As your organization changes, you can revisit a policy set to add or remove its objects and assignments. You can use a policy set to associate and assign existing objects, such as apps, policies, and VPNs in a single package. 

Policy sets do not replace existing concepts or objects. You can continue to assign individual objects and you can also reference individual objects as part of a policy set. Therefore, any changes to those individual objects will be reflected in the policy set.​ 

You can use policy sets to:

- Group objects that need to be assigned together
- Assign your organization’s minimum configuration requirements on all managed devices
- Assign commonly used or relevant apps to all users

You can include the following management objects in a policy set:
- Apps
- App configuration policies
- App protection policies
- Device configuration profiles
- Device compliance policies
- Device type restrictions
- Windows autopilot deployment profiles
- Enrollment status page

When you create a policy set, you create a single unit of assignment, and manage associations between different objects. A policy set will be a reference to objects external to it. Any changes in the included objects will affect the policy set as well. After you create a policy set, you can repeatedly view and edit its objects and assignments. 

> [!NOTE]
> Policy sets support Windows, Android, macOS, and iOS settings, and can be assigned cross-platform.

## How to create a policy set

1. Sign in to [Intune](https://go.microsoft.com/fwlink/?linkid=2090973).
2. On the **Intune** blade, choose **Policy Sets** > **Policy sets** > **Create**.
3. On the **Basics** page, add the following values:
    - **Policy set name** - Provide a name for this policy set.
    - **Description** - Optionally, provide a description for the policy set.
   <p>
   <img alt="Create policy set - Basics" src="~/fundamentals/media/policy-sets/policy-sets-01.png">

4. Click **Next: Application management**.<br>
   On the **Application management** page you can optionally [add apps](~/apps/apps-add.md), [app configuration policies](~/apps/app-configuration-policies-overview.md), and [app protection policies](~/apps/apps/app-protection-policy.md) to your policy set. For information about app management, see [What is Microsoft Intune app management?](~/apps/app-management.md). 
5. Click **Next: Device management**.<br>
   The **Device management** page allows you to add device management objects to your policy set, such as [device configuration profiles](~/configuration/device-profiles.md) and [device compliance policies](~/protect/device-compliance-get-started.md). Be sure to include all associated objects, such as other policies, certificates, and security baseline profiles.
6. Click **Next: Device enrollment**.<br>
   The **Device enrollment** page allows you to add device enrollment objects to your policy set, such as [device type restrictions](~/enrollment/enrollment-restrictions-set.md), [Windows Autopilot deployment profiles](~/enrollment/enrollment-autopilot.md), and [enrollment status page profiles](~/enrollment/windows-enrollment-status.md).
7. Click **Next: Assignments**.<br>
   The **Assignments** page allows you can assign the policy set to users and devices. It is important to note that you can assign a policy set to a device whether or not the device is managed by Intune.
8. Click **Next: Review + create** to review the values you entered for the profile.
9. When you are done, click **Create** to create the policy set in Intune. 

## Next steps

- [Enroll devices in Microsoft Intune](~/enrollment/index.md).