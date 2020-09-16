---
author: rsameser
title: Getting Started with Windows 10 IoT Enterprise
ms.date: 09/04/2020
ms.topic: article
description: Learn about what Windows 10 IoT Enterprise is and what you can do with it.
keywords: IoT Enterprise, binary
---

# Getting Started with Windows 10 IoT Enterprise
This documentation set will cover the fundamental [technical breakdown](https://docs.microsoft.com/windows/iot-enterprise/Technical_Breakdown) of what's included when you choose to use Windows 10 IoT Enterprise. It will also go into detail about its [advanced lockdown features](https://docs.microsoft.com/windows/iot-enterprise/Advanced_Lockdown_Features), how to [brand](https://docs.microsoft.com/windows/iot-enterprise/Branding) your IoT devices, how OEM relationships and [licensing](https://docs.microsoft.com/windows/iot-enterprise/Licensing) works and includes [tutorials](https://docs.microsoft.com/windows-hardware/manufacture/desktop/iot-ent-overview) on how to set up your devices.

This article will give you an overview of the product and guide you through how to get started with Windows 10 IoT Enterprise.

## What is Windows 10 IoT Enterprise?
Windows 10 IoT Enterprise is a full version of Windows 10 that delivers enterprise manageability and security to IoT solutions. Windows 10 IoT Enterprise shares all the benefits of the world-wide Windows ecosystem. It is a binary equivalent to Windows 10 Enterprise, so you can use the same familiar development and management tools as client PCs and laptops.  However, when it comes to licensing and distribution, the desktop version and IoT versions differ. Note that Windows 10 IoT Enterprise offers both Long-term Servicing Channel (LTSC) and Semi-Annual Channel (SAC) options. OEMs can choose the version they require for their devices.

## Fixed purpose devices

> [!TIP]
> See your licensing agreement for complete guidance on all Windows 10 IoT Enterprise usage scenarios. If you do not have this licensing agreement, ask the OEM you work with for the commercial agreement.

Windows is well known as the operating systems on laptops and desktops used by consumers and businesses world-wide for decades.  Windows also powers many ATM machines, point-of-sale terminals, industrial automation systems, thin clients, medical Devices, digital signage, kiosks, and other fixed purpose devices.  Windows 10 IoT Enterprise allows you to build fixed purpose devices with specific allowances and restrictions in the license agreement.  

A fixed purpose device differs from a general purpose device in the following ways:  
* The device is locked down to a single application or fixed set of applications through the Assigned Access or Shell Launcher features.  
* The device experience is immediate when the customer powers-on. This is achieved by configuring the device image to skip the normal Windows out-of-box experiences.
* Keyboards, USB ports, and device policies are locked down to constrain the device to be used only in its fixed purpose.  
* The OEM licenses the device to the user with the software attached to the device as a complete product and passes through specific Windows terms in their own agreements.
* The OEM provides the customer support for their complete product, including the functions performed by the operating system.

## Long-term Servicing Channel (LTSC)

Specialized systems, such as PCs that control medical equipment, point-of-sale systems, and ATMs, often require a longer servicing option because of their purpose. These devices typically perform a single important task and don’t need feature updates as frequently as other devices in the organization. It’s more important that these devices be kept as stable and secure as possible than that they be up to date with UI changes. The LTSC servicing model prevents Windows 10 IoT Enterprise LTSC devices from receiving the usual feature updates and provides only quality updates to ensure that device security stays up to date. With this in mind, quality updates are still immediately available to Windows 10 IoT Enterprise LTSC clients, but customers can choose to defer them by using one of the servicing tools mentioned in the Servicing tools section.

* [Learn more about LTSC](https://docs.microsoft.com/windows/deployment/update/waas-overview#long-term-servicing-channel)

> [!NOTE]
> Due to the long life of the LTSC releases and the benefit of remaining on a specific release for 10 years, an upgrade fee will be charged for customers moving from one LTSC release to another.

## Long-Term Support Silicon Details

The Windows 10 IoT Enterprise 2019 release will be an LTSC release. See [here](https://docs.microsoft.com/en-us/windows/whats-new/ltsc) for a general description of Windows 10 LTSC and other channels available. You can find details on processor support for each edition and channel of Windows 10 [here](https://docs.microsoft.com/windows-hardware/design/minimum/windows-processor-requirements#windows-iot-enterprise--embedded-processor-table).
