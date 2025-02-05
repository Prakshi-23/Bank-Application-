# Bank-Application-
# Banking Application (GUI)  A desktop-based Banking Application built with Python and CustomTkinter, featuring account management, transactions, and customer verification.  
# Banking Application (GUI)

A desktop-based Banking Application built with Python and CustomTkinter, featuring account management, transactions, and customer verification.

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

You can convert the application into an executable using Auto-py-to-exe:

```sh
pip install auto-py-to-exe
# run this command
auto-py-to-exe
```

#####

### This will convert python (.py) file into executable file (.exe)

auto-py-to-exe will open a gui window which asks for file location and select window-based option and one file option and .exe file will be created.

