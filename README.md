# 🌐 BLUE GALAXY - Audit File Management System

![Version](https://img.shields.io/badge/Version-2.0.0-blue)
![License](https://img.shields.io/badge/License-Proprietary-red)
![Python](https://img.shields.io/badge/Python-3.8+-green)
![Platform](https://img.shields.io/badge/Platform-Windows-blue)
![Year](https://img.shields.io/badge/Year-2026-brightgreen)

---

## 📌 Quick Info

**Company:** LABH PARIWAR  
**Owner:** Shubham Kumar LABH  
**Product Name:** Blue Galaxy  
**Application Type:** Desktop File Management System  
**Platform:** Windows 10/11 (Local Desktop Application)
**Year:** © 2026 LABH PARIWAR

---

## 🎯 What is BLUE GALAXY?

Blue Galaxy is a **professional Audit File Management System** designed specifically for audit firms and accounting professionals. It helps organize client files, documents, and audit records in a secure, local desktop application.

### Key Features:
✅ **Client Management** - Create and manage client profiles  
✅ **Document Storage** - Upload, organize, and retrieve documents  
✅ **Audit Logging** - Track all activities for compliance  
✅ **User Management** - Admin and Staff roles  
✅ **Local Storage** - No internet required, complete data privacy  
✅ **Windows Compatible** - Runs on Windows 10/11  

---

## 📦 Installation

### Quick Start (Recommended):

1. **Download** `blue_galaxy.exe` from `dist/` folder
2. **Double-click** to run (no installation needed!)
3. **Login** with:
   - Username: `admin`
   - Password: `admin123`

### From Source (For Developers):

```bash
# 1. Install Python 3.8+
# 2. Clone/Extract repository

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run application
python main.py
```

### Build Your Own Executable:

```bash
# Windows:
build.bat

# Or manually:
pip install pyinstaller==6.1.0
pyinstaller --onefile --windowed main.py
```

---

## 📂 Project Structure

```
blue_galaxy/
├── main.py                  # Main application (911 lines)
├── requirements.txt         # Python dependencies
├── build.bat               # Automated build script
│
├── INSTALLATION.md         # 📖 Setup & Installation Guide
├── USER_GUIDE.md          # 📖 User Manual
├── DEVELOPER_GUIDE.md     # 📖 Developer Documentation
├── README.md              # This file
│
├── data/                  # Auto-created on first run
│   ├── audit_system.db   # SQLite database
│   └── storage/          # Client document folders
│
└── dist/
    └── blue_galaxy.exe   # Compiled executable
```

---

## 🚀 Features

### 1. **Login System**
- Admin and Staff roles
- Password hashing (SHA256)
- Activity logging

### 2. **Client Management**
- Add/Edit/Delete clients
- Store: Name, Phone, Email, Address
- Track creator for accountability

### 3. **Document Management**
- Upload: PDF, JPG, PNG, DOCX, XLSX, DOC, XLS, BMP, GIF
- Storage limit: 500 MB per client
- View/Delete documents
- File tracking

### 4. **Activity Logs**
- Automatic logging of all actions
- Admin: View all logs
- Staff: View personal logs
- Timestamp tracking

### 5. **User Management** (Admin only)
- Create new users
- Assign roles (Admin/Staff)
- User list with creation date

---

## 👥 User Roles

### Admin
- Full system access
- Manage all clients and documents
- Create/manage users
- View all activity logs

### Staff
- Manage own clients
- Upload documents
- View own activity
- Cannot access other users' data

---

## 💾 Database Schema

### users
- user_id, username, password, role, created_at

### clients
- client_id, client_name, phone, email, address, created_by, created_at

### documents
- doc_id, client_id, file_name, file_path, file_size, uploaded_by, upload_date

### activity_logs
- log_id, user_id, action, client_id, details, timestamp

---

## 🎨 Color Scheme

| Name | Hex Code | Usage |
|------|----------|-------|
| Blue Galaxy | #003893 | Primary (Headers, Buttons) |
| Crimson | #DC143C | Accent (Delete, Warning) |
| Full White | #FFFFFF | Background |
| Light Gray | #F5F5F5 | Sections |
| Dark Gray | #333333 | Text |

---

## 🔐 Security

- **Password Hashing:** SHA256 encryption
- **Database:** Local SQLite (no server)
- **Data Privacy:** Each user sees only their data
- **Audit Trail:** Complete activity logging
- **No Internet:** Secure offline operation

---

## 📊 System Requirements

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| OS | Windows 10 | Windows 11 |
| RAM | 2 GB | 4 GB |
| Disk | 500 MB | 1 GB |
| Python | 3.8 | 3.11+ |

---

## 📖 Documentation

### For Users:
📚 **[USER_GUIDE.md](USER_GUIDE.md)** - How to use the application

### For Installation:
📚 **[INSTALLATION.md](INSTALLATION.md)** - Setup instructions

### For Developers:
📚 **[DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md)** - Code structure & modification

---

## 🔧 Development

### Tech Stack:
- **Language:** Python 3.8+
- **GUI:** Tkinter (built-in with Python)
- **Database:** SQLite
- **Build Tool:** PyInstaller

### Architecture:
```
User Interface (Tkinter)
        ↓
Database Layer (SQLite)
        ↓
File Storage (Local Folders)
```

### Modification Examples:

**Add new field to client:**
1. Update database schema
2. Add UI element
3. Update insert/update query
4. Refresh display

**Change color theme:**
1. Edit COLORS dictionary in main.py
2. Rebuild executable

**Add new file type:**
1. Update filetypes list in upload_document()
2. Restart application

See [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md) for detailed examples.

---

## 🐛 Troubleshooting

### Application won't start:
```bash
# Check Python version
python --version

# Check Tkinter
python -m tkinter

# Delete database and restart
rm data/audit_system.db
```

### Database issues:
```bash
# Database locked error → Close all instances
# Fresh start → Delete data/audit_system.db
```

### Build issues:
```bash
# Run build.bat in Command Prompt (not PowerShell)
# Make sure Python is in PATH
# Install PyInstaller: pip install pyinstaller
```

See [INSTALLATION.md](INSTALLATION.md) for complete troubleshooting.

---

## 🚀 Building Executable

### Automated (Recommended):
```bash
double-click build.bat
```

### Manual:
```bash
pip install pyinstaller==6.1.0
pyinstaller --onefile --windowed main.py
# Output: dist/blue_galaxy.exe
```

---

## 📋 Checklist

- [x] Database schema designed
- [x] Login system implemented
- [x] Client management complete
- [x] Document upload/download working
- [x] Activity logging functional
- [x] User management (Admin)
- [x] Role-based access control
- [x] Color theme (Blue Galaxy)
- [x] Documentation complete
- [x] Windows compatibility verified

---

## 🔄 Version History

### v1.0.0 (March 18, 2024)
- Initial release
- All core features implemented
- Complete documentation
- Ready for production use

---

## 📞 Contact & Support

**Company:** LABH PARIWAR  
**Owner:** Shubham Kumar LABH  
**Email:** support@labhpariwar.com  
**Phone:** [Contact Info]

---

## 📝 License

**Proprietary Software**  
Copyright © 2024 LABH PARIWAR  
All Rights Reserved

---

## 🎓 Getting Started

### First Time Users:
1. Extract/Download application
2. Run `blue_galaxy.exe`
3. Login with `admin` / `admin123`
4. Read [USER_GUIDE.md](USER_GUIDE.md)

### Administrators:
1. Create user accounts
2. Set up client profiles
3. Train staff users
4. Monitor activity logs
5. Perform regular backups

### Developers:
1. Read [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md)
2. Review main.py code structure
3. Set up development environment
4. Make modifications as needed
5. Build new executable with build.bat

---

## ✨ Features Coming Soon (v2.0)

- 🔄 Password change feature
- 📊 Report generation (PDF/Excel)
- 🔍 Advanced search and filters
- 💾 Automated backup system
- 📧 Email notifications
- 🌐 Network database sharing
- 📱 Mobile app support

---

## 🙏 Thank You!

Thank you for choosing **BLUE GALAXY** for your audit file management needs.

For support, feature requests, or bug reports, please contact the development team.

---

**Happy File Managing! 🎉**

*BLUE GALAXY - Making Audit Management Simple & Secure*

---

**Last Updated:** March 18, 2024  
**Maintained By:** Development Team, LABH PARIWAR
