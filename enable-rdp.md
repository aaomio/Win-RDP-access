## Enable Remote Desktop

This section enables Remote Desktop Services on a Windows Server within an Active Directory environment.

## 1. Open System Configuration
Use: Win + R
Run: sysdm.cpl

Navigate to the Remote tab.

## 2. Enable Remote Desktop
Select: Allow remote connections to this computer.

Enable: Allow connections only from computers running Network Level Authentication (NLA).

## 3. Verify RDP Service
Open services.msc.

Ensure Remote Desktop Services is running.

## 4. Verify Listening Port
Run: netstat -an | find "3389"

Confirm state is LISTENING.
