# Microsoft Sentinel – Brute Force Detection Project

## Overview
This project demonstrates an end-to-end brute force detection use case using Microsoft Sentinel.
A Windows machine was onboarded via Azure Arc and Azure Monitor Agent (AMA) to collect
Windows Security Events and generate security incidents.

## Architecture
- Windows VM (Oracle VirtualBox)
- Azure Arc
- Azure Monitor Agent (AMA)
- Data Collection Rule (DCR)
- Microsoft Sentinel

## Detection Use Case
Detect multiple failed Windows login attempts indicating a brute force attack.

## KQL Query
```kql
SecurityEvent
| where EventID == 4625
| where TimeGenerated > ago(15m)
| summarize FailedAttempts = count() by Computer
| where FailedAttempts >= 3

Category: Credential Access

Outcome

Successfully detected multiple failed login attempts and generated a Microsoft Sentinel incident, demonstrating hands-on SOC detection and incident response capability.
