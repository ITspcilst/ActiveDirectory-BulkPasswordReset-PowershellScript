## 📁 Active Directory Bulk Password Reset — PowerShell Automation

This project automates the **resetting of passwords** for multiple Active Directory (AD) users using a **CSV file**.
It is designed for IT administrators who need a **fast, consistent, and secure** way to reset many user passwords at once.

The script **generates unique random passwords** for each user, **updates them in AD**, enforces **password reset at next logon**, and stores the newly generated passwords inside a **CSV file** for administrative reference.

This project demonstrates practical skills in **AD automation**, **bulk operations**, **PowerShell scripting**, **secure credential handling**, and **file output management**.

---

### 🚀 Features

* **🔹 Bulk Password Reset**
    Reads a list of users from a CSV file and resets each user’s AD password automatically.

* **🔹 Random Secure Password Generation**
    Each user receives a **strong 12-character password** containing special characters for improved security.

* **🔹 Forced Password Change**
    After the reset, each account is configured to **require changing the password at next logon**, ensuring security.

* **🔹 Automatic CSV Output of New Passwords**
    The script saves each user’s new credentials into:
    ```text 
    Passwords\passwords.csv
    ```
   
    This file contains:
    
* **SamAccountName**
* **Newly generated password**

* **🔹 Automatic Folder Creation**
    If the `Passwords` folder does not exist, the script creates it.

* **🔹 Error Handling**
    If a password fails to reset, the script logs the failure in the console without stopping the entire batch process.

---

## 📂 Folder Structure
```text
Bulk AD user PowerShell Project
│
├── Script
│   ├── BulkADUser.ps1            # Project 1: AD User Creation
│   ├── ResetPasswords.ps1        # Project 2: This script
│   │
│   ├── Input
│   │   └── users.csv             # Contains SamAccountName list for resets
│   │
│   ├── Logs
│   │   └── creation-log.txt      # Logs for Project 1
│   │
│   └── Passwords
│       └── passwords.csv         # Output file created by this script
│
└── README.md
```
The script will reset passwords only for the users listed inside the users.csv

---

## ▶️ How to Run the Script

1. Open **PowerShell as Administrator**
2. Navigate to your Script folder:
```powershell
cd "C:\Path\To\Bulk AD user PowerShell Project\Script"
```
3. Execute the script
```powershell
.\ResetPasswords.ps1
```
4. When finished, open: 
```text
Script\Passwords\passwords.csv
```
You will see each user’s **new randomly generated password**.
## 🛡 Security Notice

* The generated passwords are **not stored in plaintext** anywhere except the CSV.
* **Delete or secure `passwords.csv`** after distributing passwords to users.
* Always store sensitive files in a **safe location**.

---

## 📸 Screenshots
* [**Runing the script**](Screenshots/IMG_2919.png)
* [**Password.csv file has successfully created**](Screenshots/IMG_2920.png)

--- 

## 🎯 What This Project Demonstrates

* Handling **bulk Active Directory operations**
* **Secure credential generation & storage**
* **Real-world IT administration tasks**
* **PowerShell automation design**
* **Safe error handling**
* **File & folder management** in scripts

---

## 📜 License

This project is released under the **MIT License**.
Feel free to modify and use it in your environment or portfolio.

---

## 🙌 Credits

Created by **ITspcilst**, with a goal to automate multiple user accounts password reset process and demonstrate practical PowerShell & AD administration skills.
