# 🔐 SecureMe – Platform to Secure Your Daily Life

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Security](https://img.shields.io/badge/Security-AES%20%7C%20PBKDF2-red.svg)

**A lightweight, offline-first personal security platform built with Python Flask**

[Features](#-core-features) • [Installation](#️-installation) • [Usage](#-usage-guide) • [Security](#️-security-architecture) • [Tech Stack](#-technology-stack)

</div>

---

## 📖 Overview

SecureMe is a comprehensive local security solution designed to protect your sensitive data without relying on cloud services. Everything stays on your machine, encrypted with industry-standard cryptography.

### Why SecureMe?

- ✅ **100% Offline** – No internet required, no data leaves your device
- ✅ **Military-Grade Encryption** – AES/Fernet encryption with PBKDF2 hashing
- ✅ **Zero Dependencies on Cloud** – Complete privacy and control
- ✅ **Lightweight & Fast** – Minimal resource usage
- ✅ **Open Source** – Transparent and auditable code

---

## 🎯 Core Features

### 🗂️ Folder Lock Module

Protect sensitive folders with system-level access restrictions and comprehensive activity logging.

**Key Capabilities:**

- Lock/unlock any folder on your device
- Real-time access control
- Detailed audit logs for every action
- Instant folder protection

### 🔑 Password Vault

A fully encrypted password manager that keeps all your credentials safe and organized.

**Features:**

- ➕ Add, edit, and delete password entries
- 📂 Category-based organization (Social, Finance, Work, etc.)
- 🔒 AES/Fernet encryption for all data
- 📊 Local encrypted Excel storage
- 🕒 Automatic metadata and timestamp logging
- 👁️ Secure password reveal/hide functionality

### 📝 Secure Notes

Create and store encrypted notes with military-grade protection.

**Highlights:**

- 📄 Each note saved as encrypted `.docx` file
- 🔐 Unique 6-character encryption key per note
- 📋 Metadata logging for all notes
- ✏️ In-app editing with automatic re-encryption
- 🔓 Simple unlock mechanism

### 🛡️ Master Passkey Authentication

Your first and last line of defense.

**Security Features:**

- PBKDF2 key derivation with SHA-256
- Random salt generation
- 200,000 iterations for maximum security
- Required for all system access

---

## 🛡️ Security Architecture

SecureMe implements multiple layers of security:

```
┌─────────────────────────────────────────┐
│         Master Passkey (PBKDF2)         │
├─────────────────────────────────────────┤
│      AES/Fernet Encryption Layer        │
├─────────────────────────────────────────┤
│        Local Storage (No Cloud)         │
├─────────────────────────────────────────┤
│    Unique Per-Note Encryption Keys      │
└─────────────────────────────────────────┘
```

**Security Standards:**

- 🔐 **AES-256 Encryption** – Industry-standard symmetric encryption
- 🔑 **PBKDF2** – Password-Based Key Derivation Function 2
- 🔒 **SHA-256 Hashing** – Cryptographic hash function
- 🎲 **Random Salt Generation** – Unique salt for each passkey
- 🔄 **200,000 Iterations** – Protection against brute-force attacks
- 💾 **Local Storage Only** – No external data transmission

---

## 🛠️ Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Quick Start

1. **Clone the Repository**

```bash
git clone https://github.com/yourusername/SecureMe.git
cd SecureMe
```

2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the Application**

```bash
python app.py
```

4. **Access in Browser**

```
http://127.0.0.1:5000
```

---

## 📌 Usage Guide

### 🚀 First Launch

On your first run, you'll be prompted to create a **Master Passkey**. This is your key to the entire system—choose wisely and remember it!

### 🗂️ Using Folder Lock

1. Navigate to the Folder Lock module
2. Enter the full path of the folder you want to protect
3. Click **Lock** to secure or **Unlock** to restore access
4. View complete lock/unlock history in the activity log

### 🔑 Managing Your Password Vault

1. Click **Add Password** to create a new entry
2. Fill in the details (title, username, password, category, URL)
3. Use filters to sort by category (Social, Finance, Work, etc.)
4. Click the eye icon to reveal/hide passwords
5. Edit or delete entries as needed

### 📝 Creating Secure Notes

1. Open the Secure Notes module
2. Click **New Note** and write your content
3. The system automatically generates a unique encryption key
4. Save the note—it's encrypted immediately
5. Use the encryption key to unlock and edit later

---

## 📚 Technology Stack

| Component            | Technology                     |
| -------------------- | ------------------------------ |
| **Backend**    | Python Flask                   |
| **Encryption** | AES/Fernet, PBKDF2, SHA-256    |
| **Frontend**   | HTML5 + CSS3 (Flask Templates) |
| **Storage**    | Encrypted Excel & Word Files   |
| **Security**   | Cryptography Library           |

---

## 📂 Project Structure

```
SecureMe/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── templates/             # HTML templates
│   ├── index.html
│   ├── vault.html
│   ├── notes.html
│   └── folder_lock.html
├── static/                # CSS and assets
│   └── styles.css
├── data/                  # Encrypted data storage
│   ├── passwords.xlsx
│   └── notes/
└── README.md
```

---

## 🔮 Future Enhancements

We're constantly working to improve SecureMe. Here's what's on the roadmap:

- [ ] 👆 **Biometric Authentication** – Fingerprint/face recognition
- [ ] 👥 **Multi-User Support** – Multiple accounts with separate vaults
- [ ] 🎭 **Role-Based Access** – Different permission levels
- [ ] 💾 **Encrypted Backup** – Optional secure backup functionality
- [ ] 📱 **Mobile Companion App** – Sync across devices (optional)
- [ ] 🌙 **Dark Mode** – Eye-friendly interface
- [ ] 🔔 **Security Alerts** – Breach notifications and warnings

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Disclaimer

SecureMe is designed for personal use and educational purposes. While we implement industry-standard security practices, no system is 100% secure. Always maintain backups of critical data and use strong, unique passphrases.

---

## ✨ Credits

**Developed by:**

👨‍💻 **Amritanshu Kumar**
👨‍💻 **Ritesh Singh Kushwaha**

**Master of Computer Applications (2024–2026)**
Lovely Professional University

---

## 📞 Contact & Support

Found a bug? Have a suggestion? We'd love to hear from you!

- 🐛 [Report Issues](https://github.com/yourusername/SecureMe/issues)
- 💡 [Request Features](https://github.com/yourusername/SecureMe/issues/new)
- ⭐ [Star this Repository](https://github.com/yourusername/SecureMe)

---

<div align="center">

**If you find SecureMe helpful, please consider giving it a ⭐!**

Made with ❤️ by security enthusiasts for security enthusiasts

</div>

---

## 📋 Raw Markdown Code

```markdown
Copy the entire artifact content above - it's already pure Markdown!
Just click the copy button in the top-right corner of the artifact.
```
