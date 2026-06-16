## Windows Firewall Configuration for RDP

This section configures Windows Defender Firewall to allow Remote Desktop (RDP) traffic within an Active Directory domain environment.

## 1. Open Firewall Management
Use: Win + R
Run: wf.msc

---

## 2. Enable RDP Inbound Rules
Navigate to:
Inbound Rules

Enable the following rule:
Remote Desktop - User Mode (TCP-In)

Also ensure:
Remote Desktop - User Mode (UDP-In)

---

## 3. Verify Rule Scope
Open properties of the RDP rule and confirm:

## General
- Enabled = Yes

## Advanced
- Profile: Domain (and Private if required)

## Protocols and Ports
- TCP 3389
- UDP 3389

---

## 4. Verify via Command Line (optional)
Run:
netsh advfirewall firewall show rule name="Remote Desktop"

