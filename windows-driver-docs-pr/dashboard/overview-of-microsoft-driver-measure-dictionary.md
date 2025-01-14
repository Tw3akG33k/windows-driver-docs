---
title: Microsoft driver measure
description: Publishers and authors use the descriptions of the Microsoft driver measures to better understand the criteria Microsoft uses in evaluating driver quality during driver flighting
ms.topic: article
ms.date: 05/20/2019
ms.author: paslote
author: parkeratmicrosoft
ms.localizationpriority: medium
---

# Overview of the Microsoft driver measures

Microsoft distributes thousands of drivers via the Windows Update service, servicing millions of machines and users each month. Safely delivering the right driver at scale requires evaluating driver quality through real-world verification during distribution.

This document is a reference to publishers and authors of Windows device drivers.  Publishers and authors can better understand the criteria Microsoft uses in evaluating driver quality during the [driver flighting process](https://docs.microsoft.com/windows-hardware/drivers/dashboard/driver-flighting). Becoming familiar with the driver quality criteria will help driver publishers understand how Microsoft reached a decision about releasing their driver.

Keywords in **bold** have corresponding definitions in the glossary.

This content contains three sections:

* Using measures: defines what measure are, the types of measures, and how measures evaluate quality.
* [Driver measure attributes](measure-attributes.md): defines the various attributes that each measure has.
* Driver measures dictionary: provides a definition for each driver measure, whether **systemic** or **device class**, with a description, attribute values, and calculation logic.

## Using measures

Microsoft defines a **measure** as a quantifiable metric to gauge the quality of products delivered by the company. Driver measures aggregate **telemetry** produced by customer machines, processing any events that are related to a driver. Each measure is scoped to a use case of the driver’s functions, ensuring that the end user can experience the component’s capabilities.

## Types of measures

To evaluate the quality of drivers, Microsoft has two distinct types of measures: **systemic measures** and **device-class measures**.

Systemic Measures ensure that a driver installs without error and the machine continues to be reliable; Microsoft applies these measures to every driver submitted. Device-Class measures monitor specific capabilities of the driver to ensure the hardware component behaves as intended; each Device-Class has a set of distinct measures applied or only uses Systemic Measures for evaluation.

All drivers submitted to Microsoft Approval undergo systemic quality evaluation. Systemic measures evaluate quality and the status of the machine without needing to understand the specific functionality of the driver. The current systemic measures monitor the success of the *driver installation and the reliability* of the machine. Driver installation measures monitor the success of installation within the audience and detect any post-installation errors.

When a partner submits a driver to Microsoft, the driver is associated with a device-class that indicates which component the driver is for. Each device-class has a distinct set of measures used to evaluate a driver’s behavior on the component or only use Systemic measures for evaluation.

## How measures assess driver quality

Each measure has its own calculation logic, which is an algorithm that parses telemetry for driver-related events and aggregates the results into a percent, ratio, or histogram of failures & successes. This result is the measure’s **current value**; the current value is evaluated against a minimum bar of quality, known as the measure’s **passing criteria**.

A measure is failing when its Current Value does not meet its Passing Criteria, triggering an investigation that may result in remediation, such as a flight rejection or an in-market expiration.

## Data sources for measures

To evaluate driver quality, measures incorporate data from machines running in two distinct customer groups: **Windows Insider Program (WIP)** and **Retail**.

WIP data is vital to flighting scenarios, as users have opted-in to providing Microsoft with increased levels of telemetry for use in real-world verification. Retail data is collected from the general Windows Ecosystem and allows Microsoft to monitor quality issues on released drivers.

## Count differences between measures

Microsoft constructs each measure differently, with a unique calculation logic, set of attributes, sampling percentages, and evaluation criteria. As a result, a set of measures applied to a distinct driver can have inconsistent **counts** reported; Microsoft expects these discrepancies.

## Related topics

[Audio measures](audio-measures.md)

[Bluetooth measures](bluetooth-measures.md)

[Camera measures](camera-measures.md)

[Firmware measures](firmware-measures.md)

[Graphics measures](graphics-measures.md)

[Wi-Fi measures](wi-fi-measures.md)

[Glossary](measures-glossary.md)
