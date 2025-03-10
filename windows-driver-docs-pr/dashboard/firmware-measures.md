---
title: Firmware measures
description: Firmware measures filter out benign initialization errors during firmware driver flighting
ms.topic: article
ms.date: 05/20/2019
ms.author: paslote
author: parkeratmicrosoft
ms.localizationpriority: medium
---

# Firmware Measures

Windows supports a platform for installing machines and device firmware updates through driver packages that are processed by using the UEFI Update Capsule function, as noted in the [Windows UEFI firmware update platform](https://docs.microsoft.com/windows-hardware/drivers/bringup/windows-uefi-firmware-update-platform). The UEFI platform supports both machine and device-level firmware updates, enabling external partners to safely update their customers’ machines. An erring firmware package can seriously harm the user’s machine and cause the machine to longer function whatsoever.
