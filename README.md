# **SecureMe – Platform to Secure Your Daily Life**

**SecureMe** is an offline, lightweight security platform designed to safeguard a user’s sensitive information.
It consolidates three major modules into a single local-system application:

* **Folder Lock**
* **Password Vault**
* **Secure Notes**

  ![Home](https://github.com/Amritanshu-404/SecureMe/blob/main/data/notes/Home.png)
  ![Dashboard](https://github.com/Amritanshu-404/SecureMe/blob/main/data/notes/Dashboard.png)

The platform is built using Python (Flask) and utilizes AES & Fernet encryption.
No data is uploaded or synced to any cloud service—everything stays on the local machine.

---

## **🔐 1. User Login**

SecureMe uses a **Master Passkey** authentication system to control access to all modules.

* Passkey is hashed using **PBKDF2-HMAC-SHA256**
* Stored with salt & iterations
* Prevents unauthorized access
* Locked interface until authenticated
---

## **🗂️ 2. Folder Lock**

This module allows users to lock/unlock local folders using OS-level ACL manipulation.

### **Key Behaviors**

* Deny or remove user read/execute permissions
* Log every operation in **LockedFolders.xlsx**
* One-click Lock/Unlock from web UI

![Folder Locker UI](https://github.com/Amritanshu-404/SecureMe/blob/main/data/notes/Folder%20Lock.png) 

---

## **🔑 3. Password Vault**

Stores encrypted credentials inside an offline Excel file.

### **Features**

* AES/Fernet-encrypted password entries
* Add, view, filter, and edit credentials
* Secure vault key stored locally
* Metadata stored in OPass.xlsx

![Password Vault Module](https://github.com/Amritanshu-404/SecureMe/blob/main/data/notes/PassVault.png) 

---

## **📝 4. Secure Notes**

Allows users to create encrypted .docx notes.

### **Highlights**

* Notes saved as Word files
* Immediately encrypted using a user-generated 6-character key
* Editable only after decryption
* Metadata logged in ONotes.xlsx

![Notes Module](https://github.com/Amritanshu-404/SecureMe/blob/main/data/notes/Notes.png) 

---

## **⚙️ Technology Stack**

* **Python Flask** – Web interface
* **Cryptography (Fernet, AES)** – Encryption
* **OpenPyXL** – Encrypted Excel storage
* **python-docx** – Notes handling
* **OS ACL Commands** – Folder locking
* **Excel Metadata** – Operation logs

---
## **👥 Contributor**

Ritesh Singh Kushwaha
GitHub: @your-github-username


