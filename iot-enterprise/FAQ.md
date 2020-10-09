---
title: Frequently Asked Questions (FAQ)
author: rsameser
ms.author: riameser
ms.date: 10/09/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Frequently asked questions about Windows 10 IoT Enterprise.
keywords: IoT Enterprise, FAQ
---

# Frequently Asked Questions (FAQ)
This document outlines the Frequently Asked Questions by customers and partners.
If you require additional assistance please reach out to your OEM distributor.

## What Windows IoT Solutions are available today?
There are presently three versions of Windows IoT available: [IoT Core](https://docs.microsoft.com/windows/iot-core/windows-iot-core), [IoT Enterprise](https://docs.microsoft.com/windows/iot-core/windows-iot-enterprise), and [IoT Server](https://docs.microsoft.com/windows/iot-core/windows-server).

## What is the difference between Windows 10 IoT Enterprise and IoT Core?
IoT Enterprise is binary-equivalent to standard Windows Enterprise. We have incorporated all IoT features into both versions, but the IoT edition includes a few minor config differences at activation and has dramatically different pricing and licensing terms. Windows 10 IoT Core is the smallest version of the Windows 10 editions that leverages the Windows 10 common core architecture. These editions enable building low-cost devices with fewer resources. Development for Windows 10 IoT Core leverages the Universal Windows Platform.

## How do people typically manage their IoT Solutions?
Listed below are the four most-commonly used management methods for IoT solutions.

### Traditional
Microsoft [System Center Configuration (SCCM)](https://docs.microsoft.com/system-center/), a solution typically used by IT departments, works with IoT Enterprise under current support terms. There is an exception process if your customer requires SCCM on IoT Core – please contact us with that request.

### Mobile Device Management (MDM)
You can use [Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) (and other Non-Microsoft MDMs like: VMWare AirWatch, MobileIron, etc) with both IoT Enterprise and IoT Core, again this is a solution typically administered by IT departments.

### Azure IoT
You can also build your own device management using [Azure IoT Device Twin and the Azure Device Agent](https://github.com/ms-iot/azure-client-tools/blob/master/docs/device-agent/device-agent.md) for IoT Core/IoT Enterprise. This method is mostly used by IoT Solution Operators.

### Device Update Center
[Device Update Center (DUC)](https://docs.microsoft.com/windows-hardware/service/iot/using-device-update-center) is available for IoT Core today. DUC is not really device management. It is update control which exists before device management in the control chain. Which means you (or your customers) can still use device management if you choose DUC. This method is mostly used by appliance device builders.
