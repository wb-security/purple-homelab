# Sysmon Deployment Guide (Domain + Local Install)

## Overview
This document explains how Sysmon is deployed in the purple-homelab environment using:
- A local installation on DC-1
- A Group Policy Object (GPO) to deploy Sysmon to all domain-joined machines

---

## Step 1 — Download Sysmon and Sysmon Config
Location: `C:\Tools\Sysmon\`

Downloaded files:
- Sysmon64.exe
- sysmonconfig.xml (SwiftOnSecurity version)

---

## Step 2 — Install Sysmon (Local)
Run in elevated PowerShell:

cd C:\Tools\Sysmon
.\Sysmon64.exe -accepteula -i sysmonconfig.xml
---

## Step 3 — Copy Files to NETLOGON
The following files were copied to SYSVOL:

Sysmon64.exe
sysmonconfig.xml
---

## Step 4 — Create GPO: "Sysmon Deployment"
Path in GPMC:
Computer Configuration → Policies → Windows Settings → Scripts → Startup

Startup script used:
`install-sysmon.ps1`

---

## Step 5 — Script Contents

$sysmonInstaller = "\DC-1\NETLOGON\Sysmon64.exe"
$config = "\DC-1\NETLOGON\sysmonconfig.xml"

Start-Process $sysmonInstaller -ArgumentList "-accepteula -i $config" -Wait
---

## Step 6 — Verification
Sysmon logs successfully appear in:

Applications and Services Logs →
    Microsoft →
        Windows →
            Sysmon →
                Operational
