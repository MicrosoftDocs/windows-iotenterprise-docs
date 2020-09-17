---
author: riames
title: Advanced Lockdown Features
ms.date: 09/17/2020
ms.topic: article
description: Learn about the Advanced Lockdown Features of Windows 10 IoT Enterprise.
keywords: Lockdown, AppLocker, Assigned Access, Edge Swipe Policy, Filtering and Controlling, USB Access, Keyboard Filter, Kiosk Mode, Shell Launcher, Unified Write Filter, HORM
---

# Advanced Lockdown Features
IoT Enterprise provides customers with the ability to create a locked down experience on any device running Windows 10. The following features describe how that experience can be customized to meet your needs.

## AppLocker
AppLocker advances the app control features and functionality of Software Restriction Policies. AppLocker contains new capabilities and extensions that allow you to create rules to allow or deny apps from running based on unique identities of files and to specify which users or groups can run those apps. AppLocker is ideal for organizations that currently use Group Policy to manage their PCs. To learn more about if AppLocker can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/applocker-overview).

Since AppLocker rules specify which apps are allowed to run on the device, you can leverage AppLocker to create a [Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) that runs multiple apps.

## Assigned Access
If you are trying to build a kiosk computer or want to restrict users to just interact with a single application, assigned access is the feature for you.
Assigned access is a feature on Windows 10 IoT Enterprise that allows you to create a locked down environment where users can only interact with a singular application when they sign into a specified account. With assigned access users will not be able to navigate away from the application.
Here's a [quick guide](https://docs.microsoft.com/windows-hardware/drivers/partnerapps/create-a-kiosk-app-for-assigned-access) on how to set up kiosk apps with assigned access on your Windows 10 device.  

## Edge Swipe Policy
If your Windows 10 device has a touchscreen, you have the option to swipe from the edge of a screen to invoke a UI. Depending on the direction of the swipe, the action center, tablet mode or taskbar can appear. To lockdown our kiosk experience the following documentation will guide you on [how to enable to disable](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe) the edge swipe policy to meet your needs.

## Filtering and Controlling (USB Access)
One of the most important safeguards that can be implemented against device tampering, whether that be malware infections or data loss, is restricting USB drives and other peripherals from gaining access to your device. Windows 10 IoT Enterprise gives you the power to set policies to [restrict or allow removable devices](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#allow-or-block-removable-devices), [prevent threats from removable storage](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#prevent-threats-from-removable-storage), create [customized alerts](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#create-customized-alerts-and-response-actions) and response actions to monitor usage of removable devices and even [respond to threats](https://docs.microsoft.com/windows/security/threat-protection/device-control/control-usb-devices-using-intune#respond-to-threats) in real-time.

## Hibernate Once/Resume Many (HORM)
You can use the [Hibernate Once/Resume Many (HORM)](https://docs.microsoft.com/windows-hardware/customize/enterprise/hibernate-once-resume-many-horm-) feature with [Unified Write Filter (UWF)](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#unifiedwritefilter) to start your device in a preconfigured state. When HORM is enabled, your system always resumes and restarts from the last saved hibernation file. A device with HORM enabled can quickly be turned off or shut down, and then restarted into the preconfigured state, even in the event of a sudden power loss. To configure the UMF with HORM, check out this [guide](https://docs.microsoft.com/en-us/windows-hardware/customize/enterprise/hibernate-once-resume-many-horm-#configure-horm).

## Keyboard Filter
If your devices is being use for a dedicated purpose, it may make sense to ensure that key combinations like 'Ctrl+Alt+Delete' do not alter the operation of the device by locking the screen or using Task Manager to close a running application. Windows 10 IoT Enterprise provides a feature called [Keyboard Filter](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter#:~:text=Keyboard%20Filter.%20You%20can%20use%20Keyboard%20Filter%20to,using%20Task%20Manager%20to%20close%20a%20running%20application.) that allows you to suppress undesirable key presses or key combinations. This [guide](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter#turn-on-keyboard-filter) will be able to walk you through how to configure, enable or disable the feature to meet your needs.

## Kiosk Mode  
Kiosk configurations are based on [Assigned Access](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#assignedaccess), a feature in Windows 10 that allows an administrator to manage the user's experience by limiting the application entry points exposed to the user. Windows 10 IoT Enterprise offers two different types of locked-down experiences for public or specialized use.

**Question: How does this fit in Edge, Chromium Browsers?

### Single-App Kiosk
A single-app kiosk runs a single Universal Windows Platform (UWP) app in full-screen above the lock screen. People using the kiosk can see only that app. A single-app kiosk is ideal for public use. Here's a [guide](https://docs.microsoft.com/windows/configuration/kiosk-single-app) on how to set up a single-app kiosk.

### Multi-App Kiosk
A multi-app kiosk runs one or more apps from the desktop. People using the kiosk see a customized Start that shows only the tiles for the apps that are allowed. With this approach, you can configure a locked-down experience for different account types. A multi-app kiosk is appropriate for devices that are shared by multiple people. Here's a [guide](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on how to set up a multi-app kiosk.

## Shell Launcher
Using [Shell Launcher](https://docs.microsoft.com/windows/configuration/kiosk-shelllauncher), you can configure a kiosk device that runs a Windows desktop application as the user interface. The application that you specify replaces the default shell (explorer.exe) that usually runs when a user logs on. This type of single-app kiosk does not run above the lock screen. Methods of controlling access to other desktop applications and system components can be used in addition to using the Shell Launcher such as, [group policy](https://www.microsoft.com/download/details.aspx?id=25250), [AppLocker](https://docs.microsoft.com/windows/iot-enterprise/advanced_lockdown_features#applocker) and [mobile device management](https://docs.microsoft.com/windows/client-management/mdm/)

## Unified Write Filter
The [Unified Write Filter (UWF)](https://docs.microsoft.com/windows-hardware/customize/enterprise/unified-write-filter#turn-on-and-configure-uwf) is a Windows 10 IoT Enterprise feature that helps to protect your drives by intercepting and redirecting any writes to the drive (app installations, settings changes, saved data) to a virtual overlay. The virtual overlay is a temporary location that is usually cleared during a reboot or when a guest user logs off. This is a great feature because it provides a clean experience for thin clients and workspaces that have frequent guests, like school, library or hotel computers. This way, guests can work, change settings, and install software, and after the device reboots, the next guest receives a clean experience. This also increases security and reliability for kiosks, IoT-embedded devices, or other devices where new apps are not expected to be frequently added. Learn how to [enable the unified write filter](https://docs.microsoft.com/windows-hardware/customize/enterprise/uwf-turnonuwf) to enhance your kiosk experience.  
