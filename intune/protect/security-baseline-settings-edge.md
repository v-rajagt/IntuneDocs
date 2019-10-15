---
# required metadata

title: Intune security baselines settings for Microsoft Edge 
titleSuffix: Microsoft Intune
description: Security baseline settings supported by Intune for managing Microsoft Edge browser
author: brenduns
ms.author: brenduns
manager: dougeby
ms.date: 11/10/2019
ms.topic: reference
ms.service: microsoft-intune
ms.localizationpriority: medium
ms.technology:
ms.assetid:

# optional metadata

#ROBOTS:

#audience:
#ms.devlang:
ms.reviewer: shpate
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Microsoft Edge baseline settings for Intune

View the Microsoft Edge web browser baseline settings that are supported by Microsoft Intune. The Edge baseline defaults represent the recommended configuration for Edge browsers, and might not match baseline defaults for other security baselines.  

## Microsoft Edge

- **Prevent bypassing Microsoft Defender SmartScreen prompts for sites**  
  **Default**: Enabled  
  Edge CSP: [Browser/PreventSmartScreenPromptOverride](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)

  This policy setting lets you decide whether users can override the Microsoft Defender SmartScreen warnings about potentially malicious websites. If you enable this setting, users can't ignore Microsoft Defender SmartScreen warnings and they are blocked from continuing to the site. If you disable or don't configure this setting, users can ignore Microsoft Defender SmartScreen warnings and continue to the site.

- **Minimum SSL version enabled**  
  **Default**: Enabled  

  Sets the minimum supported version of SSL. If you don't configure this policy, Microsoft Edge uses a default minimum version, TLS 1.0. If you enable this policy, you can set the minimum version to one of the following values: "tls1", "tls1.1" or "tls1.2". When set, Microsoft Edge won't use any version of SSL/TLS lower than the specified version. Any unrecognized value is ignored. * "tls1" = TLS 1.0 * "tls1.1" = TLS 1.1 * "tls1.2" = TLS 1.2 Example value: tls1.  
  <br>
  - **Minimum SSL version enabled**  
    **Default**: TLS 1.2

- **Prevent bypassing of Microsoft Defender SmartScreen warnings about downloads**  
  **Default**: Enabled  
  Edge CSP: [Browser/PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)  

  This policy lets you determine whether users can override Microsoft Defender SmartScreen warnings about unverified downloads. If you enable this policy, users in your organization can't ignore Microsoft Defender SmartScreen warnings, and they're prevented from completing the unverified downloads. If you disable or don't configure this policy, users can ignore Microsoft Defender SmartScreen warnings and complete unverified downloads.

- **Allow users to proceed from the SSL warning page**  
  **Default**: Disabled  
  Edge CSP: [Browser/PreventCertErrorOverrides](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-preventcerterroroverrides)  

  Microsoft Edge shows a warning page when users visit sites that have SSL errors. If you enable or don't configured (default) this policy, users can click through these warning pages. If you disable this policy, users are blocked from clicking through any warning page. 

- **Default Adobe Flash setting**  
  **Default**: Enabled
  Edge CSP: [Browser/AllowFlash](https://docs.microsoft.coms/windows/client-management/mdm/policy-csp-browser#browser-allowflash), and [Browser/AllowFlashClickToRun](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)  

  Determines whether websites that aren't covered by 'PluginsAllowedForUrls' or 'PluginsBlockedForUrls' can automatically run the Adobe Flash plug-in. You can select 'BlockPlugins' (2) to block Adobe Flash on all sites, or you can select 'ClickToPlay' (3) to let Adobe Flash run but require the user to click the placeholder to start it. In any case, the 'PluginsAllowedForUrls' and 'PluginsBlockedForUrls' policies take precedence over 'DefaultPluginsSetting'. Automatic playback is only allowed for domains explicitly listed in the 'PluginsAllowedForUrls' policy. If you want to enable automatic playback for all sites, consider adding http://* and https://* to this list. If you don't configure this policy, the user can change this setting manually. * 2 = Block the Adobe Flash plug-in * 3 = Click to play The former '1' option set allow-all, but this functionality is now only handled by the 'PluginsAllowedForUrls' policy. Existing policies using '1' will operate in Click-to-play mode.  
  <br> 
  - **Default Adobe Flash setting**  
    **Default**: Block the Adobe Flash plugin

- **Enable site isolation for every site**  
  **Default**: Enabled  

  The 'SitePerProcess' policy can be used to prevent users from opting out of the default behavior of isolating all sites. Note that you can also use the IsolateOrigins policy to isolate additional, finer-grained origins. If you enable this policy, users can't opt out of the default behavior where each site runs in its own process. If you disable or don’t configure this policy, a user can opt out of site isolation. (For example, by using "Disable site isolation" entry in edge://flags.) Disabling the policy or not configuring the policy doesn't turn off Site Isolation.

- **Supported authentication schemes**  
  **Default**: Enabled  

  Specifies which HTTP authentication schemes are supported. You can configure the policy by using these values: 'basic', 'digest', 'ntlm', and 'negotiate'. Separate multiple values with commas. If you don't configure this policy, all four schemes are used. Example value: basic,digest,ntlm,negotiate.  
  <br>  

  - **Supported authentication schemes**  
    Select from the following options: 
    - Basic
    - Digest
    - NTLM *(Selected by default)*
    - Negotiate *(Selected by default)*

- **Enable saving passwords to the password manager**  
  **Default**: Disabled  
  Edge CSP: [Browser/AllowPasswordManager](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)  

  Enable Microsoft Edge to save user passwords. If you enable this policy, users can save their passwords in Microsoft Edge. The next time they visit the site, Microsoft Edge will enter the password automatically. If you disable this policy, users can't save new passwords, but they can still use previously saved passwords. If you enable or disable this policy, users can't change or override it in Microsoft Edge. If you don't configure it, users can save passwords, as well as turn this feature off.

- **Control which extensions cannot be installed**  
  **Default**: Enabled  
   
  List specific extensions that users can NOT install in Microsoft Edge. When you deploy this policy, any extensions on this list that were previously installed will be disabled, and the user won't be able to enable them. If you remove an item from the list of blocked extensions, that extension is automatically re-enabled anywhere it was previously installed. Use "*" to block all extensions that aren't explicitly listed in the allow list. If you don't configure this policy, users can install any extension in Microsoft Edge. Example value: extension_id1 extension_id2.  
  <br>
  - **Extension IDs the user should be prevented from installing (or * for all)**  
    Select **Add** and specify additional extensions. **\*** is selected by default.

- **Configure Microsoft Defender SmartScreen**  
  **Default**: Enabled  
  Edge CSP: [Browser/AllowSmartScreen](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)  
  
  This policy setting lets you configure whether to turn on Microsoft Defender SmartScreen. Microsoft Defender SmartScreen provides warning messages to help protect your users from potential phishing scams and malicious software. By default, Microsoft Defender SmartScreen is turned on. If you enable this setting, Microsoft Defender SmartScreen is turned on and users can't turn it off. If you disable this setting, Microsoft Defender SmartScreen is turned off and users can't turn it on. If you don't configure this setting, users can choose whether to use Microsoft Defender SmartScreen. This policy is available only on Windows instances that are joined to a Microsoft Active Director domain; or on Windows 10 Pro or Enterprise instances that are enrolled for device management.

- **Allow user-level native messaging hosts (installed without admin permissions)**  
  **Default**: Disabled  

  Enables user-level installation of native messaging hosts. If you disable this policy, Microsoft Edge will only use native messaging hosts installed on the system level. By default, if you don't configure this policy, Microsoft Edge will allow usage of user-level native messaging hosts.
 
