## Create Active Directory Security Group

This section explains how to create a dedicated Active Directory security group to manage Remote Desktop (RDP) access in a centralized way.

---

## 1. Open Active Directory Users and Computers

Run:
dsa.msc

Navigate to:
Users container or a dedicated OU for administrative groups.

---

## 2. Create New Group

Right-click → New\Group

Set the following:

Group Name:
Remote-RDP-Users

Group Scope:
Global

Group Type:
Security

---

## 3. Add Members to Group

Open the group → Members tab → Add users.

Example:
User1
User2

Only include users who require Remote Desktop access.
## 2. Create New Group

Right-click then select New Group

Set the following:

Group Name:
Remote-RDP-Users

Group Scope:
Global

Group Type:
Security

---

## 3. Add Members to Group

Open the group and go to the Members tab, then add users.

Example:
User1  
User2  

Only include users who require Remote Desktop access.

---

## 4. Verify Group Membership

On a domain-joined machine, run:
whoami /groups

Confirm that Remote-RDP-Users appears in the list.

