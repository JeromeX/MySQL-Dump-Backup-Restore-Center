# 🛡️ MySQL Backup, Restore & DB-Admin Center

![Version](https://img.shields.io/badge/version-27.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows_x64-lightgrey.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Built With](https://img.shields.io/badge/Built_with-.NET_8-purple.svg)

A modern, lightweight **WPF tool** for easy management of MySQL databases. It allows you to create backups (dumps), restore databases, and create or delete databases via a user-friendly graphical interface.

---

## ✨ Features

* **🚀 One-Click Backup:** Creates SQL dumps and automatically compresses them into `.zip` files.
* **♻️ Easy Restore:** Restores databases directly from `.sql` or `.zip` files.
* **🛠️ Database Admin:**
    * `[NEW DB]` Create new databases (automatically sets charset to `utf8mb4_general_ci`).
    * `[DELETE DB]` Delete databases (includes a double security confirmation prompt).
* **🌍 Multi-Language:** The entire interface can be switched between **English** and **German** on the fly.
* **📜 Logging:** Detailed log system (SQLite-based) with a built-in log viewer.
* **🔒 Security:** Passwords are stored encrypted using Windows DPAPI.
* **🎨 Modern UI:** Clean Dark Mode design with neon accents.

---

## 📥 Installation & Usage

### Prerequisites
1.  **Windows 10/11** (64-Bit).
2.  **.NET Desktop Runtime 8.0** (usually installed via Windows Update, otherwise [download here](https://dotnet.microsoft.com/download/dotnet/8.0)).
3.  **mysqldump.exe:** This file must be present on your PC (it is part of installation).

### Getting Started
1.  Use installer.
2.  Run the application.

---

## 📖 Quick Start Guide

### 1. Configuration (Important!)
On the first launch, you must configure the connection:
1.  Enter **Host** (e.g., `127.0.0.1`), **Port**, **User**, and **Password**.
2.  Select the path to `mysqldump.exe` and your desired Backup Directory.
3.  **IMPORTANT:** Click on **[ Save & Test ]**.
4.  Only *after* saving successfully can you select your database from the dropdown menu.

### 2. Create Backup
* Select the desired database.
* Click on **[ BACKUP ]** (or **[ CREATE BACKUP ]**).
* The tool generates a ZIP file in your target folder (Format: `backup_DBNAME_YYYY-MM-DD_HH-mm.zip`).

### 3. Manage Databases
* **Create:** Click the green **[ NEW DB ]** button. Enter a name, and the database will be created immediately with `utf8mb4` encoding.
* **Delete:** Click the red **[ DELETE DB ]** button to drop the currently selected database (irreversible!).

---

## 🧩 Technology Stack

* **Language:** C# (WPF)
* **Framework:** .NET 8.0 (Windows)
* **Database (Internal):** SQLite (via `Microsoft.Data.Sqlite`)
* **Design:** Custom Dark Theme (XAML)

---

## ⚖️ License & Copyright

This project is Open Source.

© 2025 by Malte Speck
