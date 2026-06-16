## Remote Desktop Testing

This section verifies that Remote Desktop (RDP) access is correctly restricted to authorised Active Directory users using Security Groups and Group Policy.

---

## 1. Verify User Group Membership

On the client machine or server, run:
```cmd
whoami /groups
```

Confirm:
Remote-RDP-Users is listed

---

## 2. Test DNS Resolution

From CLIENT-01, test name resolution:
```cmd
ping DC-01
```

Or:
```cmd
nslookup DC-01
```

Ensure resolution to correct IP address.

---

## 3. Start Remote Desktop Client

Use: Win + R
Run: mstsc

Enter target server:
DC-01


---

## 4. Authentication Test

Log in using a domain account:
DOMAIN\username

Expected result:
- Remote Desktop session opens successfully for authorised users
- Access denied for users not in Remote-RDP-Users group

---

## 5. Verify Active Session (Server Side)

To verify an active Remote Desktop session on the server:

Use:
Win + R

Run:
taskmgr

Go to the Users tab and check for active logged-in users.

