# Bank-Application-
# Banking Application (GUI)  A desktop-based Banking Application built with Python and CustomTkinter, featuring account management, transactions, and customer verification.  
# Banking Application (GUI)

A desktop-based Banking Application built with Python and CustomTkinter, featuring account management, transactions, and customer verification.

## Banking Application Overview

![Banking App Flowchart](images/DALL%E2%80%A2E%202025-02-20%2018.51.43%20-%20A%20refined%20and%20professional%20flowchart%20illustrating%20the%20main%20tools%20and%20their%20usage%20in%20a%20bank%20application%20project.%20The%20flowchart%20includes___1.%20__Python%20.webp)


## Features

- User Registration (Sign Up)
- OTP-based Email Verification
- User Authentication (Sign In)
- Deposit & Withdraw Money
- Check Account Balance
- Transaction History (Download as Excel file)
- Admin Panel for Customer Management

## Prerequisites

Ensure you have the following installed:

- Python (>=3.7)
- pip (Python package manager)
- MySQL Server

## Installation and Setup

### 1. Setup MySQL Database

1. Open MySQL Workbench or CLI.
2. Create a new database:
   ```sql
   CREATE DATABASE new_bank;

   ### create table to store customer details
   CREATE TABLE customer_info (
       c_id INT AUTO_INCREMENT PRIMARY KEY,
       fname VARCHAR(50),
       mname VARCHAR(50),
       lname VARCHAR(50),
       gender VARCHAR(1),
       phoneno VARCHAR(15),
       email VARCHAR(255),
       aadharno VARCHAR(12),
       dob DATE,
       age INT,
       occupation VARCHAR(20),
       monthly_income VARCHAR(20),
       marital_status VARCHAR(20),
       education VARCHAR(20),
       date DATE,
       username VARCHAR(10),
       password VARCHAR(4),
       balance INT,
       target_balance VARCHAR(10)
   );
   ```
3. Create new table for storing customer details

   Update database credentials in `bank_app.py` inside `get_db_connection()` function.

### 2. Run the Application

The GUI application will launch.

## Usage

- **Sign Up**: Register a new user.
- **Sign In**: Log in using registered credentials.
- **Deposit/Withdraw**: Perform transactions.
- **Admin Panel**: Manage customer accounts.

## Deployment

You can convert the application into an executable using Auto-py-to-exe or Pyinstaller:

## 1. Auto-py-to-exe
```sh
pip install auto-py-to-exe
# run this command
auto-py-to-exe
```
## 2. Pyinstaller

# 🚀 PyInstaller Guide for Anaconda Prompt  

This guide helps package `bank_app_.py` into an executable using PyInstaller in **Anaconda Prompt**.

## 📌 Prerequisites  
Ensure PyInstaller is installed:  
```sh
pip install pyinstaller
```
If working with Excel files, reinstall `openpyxl`:  
```sh
pip uninstall openpyxl
pip install --no-cache-dir openpyxl
```

## 🔧 Build the Executable  
Run PyInstaller with submodule collection:  
```sh
pyinstaller --onefile --collect-submodules openpyxl bank_app_.py
```

## 🛠 Troubleshooting  
### Recursion Error  
Increase recursion limit:  
```python
import sys
sys.setrecursionlimit(5000)
```
###or else upgrade pyinstaller
```
pip install --upgrade pyinstaller
```

### Missing Modules  
Manually add them in `bank_app_.py`:  
```python
import openpyxl.cell._writer
```
Or use a `.spec` file:  
1. Generate a `.spec` file:  
   ```sh
   pyi-makespec bank_app_.py
   ```
2. Edit and add hidden imports:  
   ```python
   hiddenimports=['openpyxl', 'openpyxl.cell', 'openpyxl.cell._writer']
   ```
3. Build with:  
   ```sh
   pyinstaller bank_app_.spec
   ```

## 🎯 Running the Executable  
After packaging, navigate to the `dist` folder:  
```sh
dist\bank_app_.exe
```

---

🚀 Happy coding!



#####

### This will convert python (.py) file into executable file (.exe)

auto-py-to-exe will open a gui window which asks for file location and select window-based option and one file option and .exe file will be created.

pyinstaller will create a build folder and your exe application will be in dist folder.

