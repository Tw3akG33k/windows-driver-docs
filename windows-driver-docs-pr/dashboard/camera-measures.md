---
title: Camera measures
description: Camera measures filter out benign initialization errors during Bluetooth driver flighting
ms.topic: article
ms.date: 05/20/2019
ms.author: paslote
author: parkeratmicrosoft
ms.localizationpriority: medium
---

# Camera measures

## Description

In Windows 10, Microsoft provides a [Universal Camera Driver Design Guide](https://docs.microsoft.com/windows-hardware/drivers/stream/windows-10-technical-preview-camera-drivers-design-guide), that discusses how the camera driver interface can support all camera-related devices. The model includes new DDIs, like Digital Video Stabilization, Variable Frame Rate, Face Detection, and many other features. The universal camera driver is an AVStream minidriver built on the Windows Driver Model; AVStream is a Microsoft-provided multimedia class driver that supports video-only streaming and integrated video and audio streaming. You can find details about AVStream in the [AVStream Minidrivers Design Guide](https://docs.microsoft.com/windows-hardware/drivers/stream/avstream-minidrivers-design-guide) .