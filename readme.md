# Windows Server Remote Desktop Access Management

This project builds on the **[win-server-AD](https://github.com/aaomio/win-server-AD)** repository.

With the infrastructure in place, this project focuses on **access control for Remote Desktop (RDP)** using Active Directory security groups and Group Policy.

---

## Objective

The goal of this lab is to centrally manage Remote Desktop access across domain-joined servers.

Instead of configuring RDP permissions manually on each machine, access is controlled through:

- Active Directory Security Groups
- Group Policy Objects (GPO)

This provides a scalable and role-based access model similar to enterprise environments.

---

## Lab Environment

**Domain**

```text
matrix.local
```

**Systems**

```text
DC-01      Domain Controller
CLIENT-01  Domain Client
```

## Workflow

1. Enable Remote Desktop on the target servers.
2. Configure Windows Defender Firewall to allow RDP traffic.
3. Create an Active Directory security group for Remote Desktop access and Add authorised users to the security group.
4. Configure Group Policy to grant the required Remote Desktop permissions.
5. Test Remote Desktop connectivity from CLIENT-01.

## Repository Structure

* [Enable Remote Desktop](enable-rdp.md)
* [Configure Windows Firewall](windows-firewall.md)
* [Create Active Directory Security Group](security-group.md)
* [Configure Group Policy](group-policy.md)
* [Remote Desktop Testing](rdp-testing.md)
