---
title: Windows 10 roaming settings reference | Microsoft Docs
description: A complete list of all the settings that will be roamed or backed up in Windows 10.
services: active-directory
keywords: enterprise state roaming, windows cloud
documentationcenter: ''
author: MarkusVi
manager: femila
editor: curtand

ms.assetid: 17cffc3e-2928-4235-91f7-a685bd6bdcbf
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 02/22/2017
ms.author: markvi

---
# Windows 10 roaming settings reference
The following is a complete list of all the settings that will be roamed or backed up in Windows 10. 

## Devices and endpoints
See the following table for a summary of the devices and account types that are supported by the sync, backup, and restore framework in Windows 10.

| Account type and operation | Desktop | Mobile |
| --- | --- | --- |
| Azure Active Directory: sync |Yes |No |
| Azure Active Directory: backup/restore |No |No |
| Microsoft account: sync |Yes |Yes |
| Microsoft account: backup/restore |No |Yes |

## What is backup?
Windows settings generally sync by default, but some settings are only backed up, such as the list of installed applications on a device. Backup is for mobile devices only and currently not available for Enterprise State Roaming users. Backup uses a Microsoft account and stores the settings and application data into OneDrive. If a user disables sync on the device using the Settings app, application data that normally syncs becomes backup only. Backup data can only be accessed through the restore operation during the first run experience of a new device. Backups can be disabled via the device settings, and can be managed and deleted through the user’s OneDrive account.

## Windows Settings overview
The following settings groups are available for end-users to enable/disable settings sync on Windows 10 devices.

* Theme: desktop background, user tile, taskbar position, etc. 
* Internet Explorer Settings: browsing history, typed URLs, favorites, etc. 
* Passwords: [Windows credential locker](https://technet.microsoft.com/library/jj554668.aspx), including Wi-Fi profiles 
* Language Preferences: spelling dictionary, system language settings 
* Ease of Access: narrator, on-screen keyboard, magnifier 
* Other Windows Settings: see Windows Settings details

![](./media/active-directory-enterprise-state-roaming/active-directory-enterprise-state-roaming-individual-sync-settings.png)

Edge browser setting group (favorites, reading list) syncing can be enabled or disabled by end users through Edge browser Settings menu option.

![](./media/active-directory-enterprise-state-roaming/active-directory-enterprise-state-roaming-sync-content.png)

## Windows Settings details
In the following table, Other entries in the Settings Group column refers to settings that can be disabled by going to Settings > Accounts > Sync your settings > Other Windows settings. 

Internal entries in the Settings Group column refer to settings and apps that can only be disabled from syncing within the app itself or by disabling sync for the entire device using mobile device management (MDM) or Group Policy settings.
Settings that don't roam or sync will not belong to a group.

| Settings | Desktop | Mobile | Group |
| --- | --- | --- | --- |
| **Accounts**: account picture |sync |X |Theme |
| **Accounts**: other account settings |X |X | |
| **Advanced mobile broadband**: Internet connection sharing network name (enables auto-discovery of mobile Wi-Fi hotspots via Bluetooth) |X |X |Passwords |
| **App data**: individual apps can sync data |sync backup |sync backup |internal |
| **App list**: list of installed apps |X |backup |Other |
| **Bluetooth**: all Bluetooth settings |X |X | |
| **Command prompt**: Command prompt "Defaults" settings |sync |X | |
| **Credentials**: Credential Locker |sync |sync |password |
| **Date, Time, and Region**: automatic time (Internet time sync) |sync |sync |language |
| **Date, Time, and Region**: 24-hour clock |sync |X |language |
| **Date, Time, and Region**: date and time |sync |X |language |
| **Date, Time, and Region**: time zone | |X |language |
| **Date, Time, and Region**: daylight savings time |sync |X |language |
| **Date, Time, and Region**: country/region |sync |X |language |
| **Date, Time, and Region**: first day of week |sync |X |language |
| **Date, Time, and Region**: region format (locale) |sync |X |language |
| **Date, Time, and Region**: short date |sync |X |language |
| **Date, Time, and Region**: long date |sync |X |language |
| **Date, Time, and Region**: short time |sync |X |language |
| **Date, Time, and Region**: long time |sync |X |language |
| **Desktop personalization**: desktop Theme (background, system color, default system sounds, screen saver) |sync |X |Theme |
| **Desktop personalization**: slideshow wallpaper |sync |X |Theme |
| **Desktop personalization**: taskbar settings (position, auto-hide, etc.) |sync |X |Theme |
| **Desktop personalization**: start screen layout |X |backup | |
| **Devices**: shared printers you've connected to |X |X |other |
| **Edge browser**: reading list |sync |sync |internal |
| **Edge browser**: favorites |sync |sync |internal |
| **Edge browser**: all other Edge settings |X |X | |
| **High Contrast**: On or Off |sync |X |ease of access |
| **High contrast**: Theme settings |sync |X |ease of access |
| **Internet Explorer**: open tabs (URL and title) |sync |sync |Internet Explorer |
| **Internet Explorer**: reading list |sync |sync |Internet Explorer |
| **Internet Explorer**: typed URLs |sync |sync |Internet Explorer |
| **Internet Explorer**: browsing history |sync |sync |Internet Explorer |
| **Internet Explorer**: favorites |sync |sync |Internet Explorer |
| **Internet Explorer**: excluded URLs |sync |sync |Internet Explorer |
| **Internet Explorer**: home pages |sync |sync |Internet Explorer |
| **Internet Explorer**: domain suggestions |sync |sync |Internet Explorer |
| **Keyboard**: users can turn on/off on-screen keyboard |sync |X |ease of access |
| **Keyboard**: turn on sticky yes (off by default) |sync |X |ease of access |
| **Keyboard**: turn on filter keys (off by default) |sync |X |ease of access |
| **Keyboard**: turn on toggle keys (off by default) |sync |X |ease of access |
| **Internet Explorer**: domain Language: Chinese (CHS) QWERTY - enable self-learning |sync |X |Language |
| **Language**: CHS QWERTY - enable dynamic candidate ranking |sync |X |Language |
| **Language**: CHS QWERTY - char-set Simplified Chinese |sync |X |Language |
| **Language**: CHS QWERTY - char-set Traditional Chinese |sync |X |Language |
| **Language**: CHS QWERTY - fuzzy pinyin |sync |backup |Language |
| **Language**: CHS QWERTY - fuzzy pairs |sync |backup |Language |
| **Language**: CHS QWERTY - full pinyin |sync |X |Language |
| **Language**: CHS QWERTY - double pinyin |sync |X |Language |
| **Language**: CHS QWERTY - reading auto correction |sync |X |Language |
| **Language**: CHS QWERTY - C/E switch key, shift |sync |X |Language |
| **Language**: CHS QWERTY - C/E switch key, Ctrl |sync |X |Language |
| **Language**: CHS WUBI - single character input mode |sync |X |Language |
| **Language**: CHS WUBI - show the remaining coding of the candidate |sync |X |Language |
| **Language**: CHS WUBI - beep when 4-coding is invalid |sync |X |Language |
| **Language**: CHT Bopomofo - include CJK Ext-A |sync |X |Language |
| **Language**: Japanese IME - predictive typing and custom words |sync |sync |Language |
| **Language**: Korean (KOR) IME |X |X |Language |
| **Language**: handwriting recognition |X |X |Language |
| **Language**: language profile |sync |backup |Language |
| **Language**: spellcheck - autocorrect and highlight misspellings |sync |backup |Language |
| **Language**: list of keyboards |sync |backup |Language |
| **Lock Screen**: all lock screen settings |X |X | |
| **Magnifier**: on or off (master toggle) |X |X |Ease of access |
| **Magnifier**: turn inversion color on or off (off by default) |sync |X |Ease of access |
| **Magnifier**: tracking - follow the keyboard focus |sync |X |Ease of access |
| **Magnifier**: tracking - follow the mouse cursor |sync |X |Ease of access |
| **Magnifier**: start when users sign in (off by default) |sync |X |Ease of access |
| **Mouse**: change the size of mouse cursor |sync |X |other |
| **Mouse**: change the color of mouse cursor |sync |X |other |
| **Mouse**: all other settings |X |X | |
| **Narrator**: quick launch |sync |X |Ease of access |
| **Narrator**: users can change Narrator speaking pitch |sync |X |Ease of access |
| **Narrator**: users can turn on or off Narrator reading hints for common items (on by default) |sync |X |Ease of access |
| **Narrator**: users can turn on or off whether they can hear typed characters (on by default) |sync |X |Ease of access |
| **Narrator**: users can turn on or off whether they can hear typed words (on by default) |sync |X |Ease of access |
| **Narrator**: have insert cursor following Narrator (on by default) |sync |X |Ease of access |
| **Narrator**: enable visual highlighting of Narrator cursor (on by default) |sync |X |Ease of access |
| **Narrator**: play audio cues (on by default) |sync |X |Ease of access |
| **Narrator**: activate keys on the touch keyboard when you lift your finger (off by default) |sync |X |Ease of access |
| **Ease of access**: set the thickness of the blinking cursor |sync |X |Ease of access |
| **Ease of access**: remove background images (off by default) |sync |X |Ease of access |
| **Power and Sleep**: all settings |X |X | |
| **Start screen personalization**: accent color (phone only) |X |sync |Theme |
| **Typing**: spelling dictionary |sync |backup |Language |
| **Typing**: autocorrect misspelled word |sync |backup |Language |
| **Typing**: highlight misspelled words |sync |backup |Language |
| **Typing**: show text suggestions as I type |sync |backup |Language |
| **Typing**: add a space after I choose a text suggestion |sync |backup |Language |
| **Typing**: add a period after I double-tap the spacebar |sync |backup |Language |
| **Typing**: capitalize the first letter of each sentence |sync |backup |Language |
| **Typing**: use all uppercase letters when I double-tap shift key |sync |backup |Language |
| **Typing**: play key sounds as I type |sync |backup |Language |
| **Typing**: personalization data for touch keyboard |sync |backup |Language |
| **Wi-Fi**: Wi-Fi profiles (only WPA) |sync |sync |Passwords |

## Related topics
* [Enterprise state roaming overview](active-directory-windows-enterprise-state-roaming-overview.md)
* [Enable enterprise state roaming in Azure Active Directory](active-directory-windows-enterprise-state-roaming-enable.md)
* [Settings and data roaming FAQ](active-directory-windows-enterprise-state-roaming-faqs.md)
* [Group policy and MDM settings for settings sync](active-directory-windows-enterprise-state-roaming-group-policy-settings.md)
* [Troubleshooting](active-directory-windows-enterprise-state-roaming-troubleshooting.md)
