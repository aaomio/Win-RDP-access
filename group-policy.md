## Group Policy Configuration for RDP Access

This section configures Group Policy to control which users are allowed to use Remote Desktop (RDP) across domain-joined servers.

The policy applies centrally to both the Domain Controller and File Server.

---

## 1. Open Group Policy Management

Use: 
Win + R

Run: 
gpmc.msc

---

## 2. Create New GPO

Right-click the domain or target OU and create:

GPO Name:
RDP-Access-Control

---

## 3. Edit GPO Settings

Navigate to:

Computer Configuration\Policies\Windows Settings\Security Settings\Local Policies\User Rights Assignment

---

## 4. Configure Remote Desktop Access

Open:
Allow log on through Remote Desktop Services

Add:
Remote-RDP-Users

Ensure default entries such as Administrators remain.

---

## 5. Link GPO to Target OU

Link the GPO to:
- Domain Controllers OU



