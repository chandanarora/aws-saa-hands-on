# Task 01 – IAM User and Group Setup

This task sets up the foundational IAM structure to securely manage AWS access.

---

## ✅ Objectives

- Create an IAM Group with PowerUserAccess
- Create an IAM User and attach to the group
- Enable MFA for the user
- Sign in with IAM credentials (not root)

---

## 🛠️ Steps Performed

1. Created IAM Group `SAA_admins`
2. Attached AWS managed policy: `PowerUserAccess`
3. Created IAM user `saa-user` with:
   - Console + programmatic access
   - Group assignment: `SAA_admins`
4. Enabled MFA (Virtual Authenticator App)
5. Downloaded `.csv` with access keys
6. Logged in successfully with MFA

---

## 📸 Screenshots

| Action                     | Screenshot                                  |
|---------------------------|---------------------------------------------|
| Group with PowerUserAccess| ![Group](./screenshots/group.png)           |
| MFA enabled for user      | ![MFA](./screenshots/user_mfa.png)          |

---

## 🔒 Security Notes

- Root account never used beyond setup
- MFA enforced
- Access keys saved securely (not hardcoded)

---

## ⏭️ Next Task

[Task 02 – EC2 Launch & Security Group Setup](../task-02-ec2-launch/)
