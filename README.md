# Bank Management System

## 📋 Project Overview

**Bank Management System** is a console-based application developed in **C++** that simulates basic banking operations. It allows users to create and manage two types of bank accounts (Savings and Current) with essential features like account creation, deposit, withdrawal, and balance inquiry.

This is a beginner-friendly project that demonstrates object-oriented programming (OOP) concepts in C++, including classes, static members, and member functions.

---

## ✨ Features

### Account Types

1. **Savings Account**
   - Minimum opening balance: **₹500**
   - Suitable for individual savers
   - Standard savings account features

2. **Current Account**
   - Minimum opening balance: **₹1000**
   - Designed for business transactions
   - Similar operations as Savings account

### Core Operations

- **Account Opening**: Create a new account with customer details
- **Deposit**: Add funds to an existing account
- **Withdrawal**: Withdraw money (with balance validation)
- **Balance Inquiry**: Check current account balance
- **Account Management**: View account details and transaction history

### Customer Information Stored

- Customer Name
- Address
- Phone Number
- Account Type (Savings/Current)
- Account Number (auto-generated)
- Current Balance

---

## 🏗️ Project Architecture

### Class Structure

```bash
class bank
├── Private Members
│   ├── static int acctno (Savings account counter)
│   ├── static int acttno (Current account counter)
│   ├── char name[20]
│   ├── char add[20]
│   └── char ph_no[10]
│
└── Public Methods
    ├── static void increment() - Increment savings account number
    ├── static void display() - Display account number
    ├── static void increse() - Increment current account number
    ├── static void show() - Display current account number
    ├── void saving() - Handle savings account operations
    └── void curr() - Handle current account operations
```

### Flow Diagram

```bash
Main Menu (Savings/Current/Exit)
    ↓
┌─────────────────────────────────────────┐
│                                         │
├→ Savings Account Menu             ├→ Current Account Menu
│  1. Account Opening                  1. Account Opening
│  2. Deposit                          2. Deposit
│  3. Withdrawal                       3. Withdrawal
│  4. Balance Check                    4. Balance Check
│  5. Back to Main                     5. Back to Main
│                                      │
└─────────────────────────────────────────┘
```

---

## 🔧 Technical Details

### Built With

- **Language**: C++
- **Platform**: Turbo C++ (DOS-based)
- **Compilation Target**: Windows (legacy DOS mode)

### Dependencies

- `iostream.h` - Standard I/O operations
- `conio.h` - Console I/O (Turbo C++ specific)
- `stdlib.h` - Standard library functions
- `dos.h` - DOS-specific functions (delay, etc.)

---

## 📝 How to Use

### Running the Program

**On Turbo C++:**

1. Open Turbo C++
2. File → New → Edit the file
3. Copy the code from `BANK.CPP`
4. Press Alt+F9 to compile
5. Press Ctrl+F9 to run

**On Modern Compilers (with modifications):**

```bash
# Using g++ (requires refactoring)
g++ -o bank BANK.CPP
./bank
```

### Using the Application

1. **Start the Program**: The welcome screen appears
2. **Select Account Type**:
   - Option 1: Access Savings Account menu
   - Option 2: Access Current Account menu
   - Option 3: Exit the application

3. **Perform Transactions**:
   - Create an account with minimum balance
   - Deposit money
   - Withdraw money (up to available balance)
   - Check balance and account details

4. **Exit**: Select option 3 from main menu to exit

### Sample Transactions

```bash
1. Create Savings Account (₹500 minimum)
   - Name: John Doe
   - Address: 123 Main St
   - Phone: 9876543210
   - Initial Deposit: ₹5000

2. Deposit ₹2000
   - New Balance: ₹7000

3. Withdraw ₹3000
   - New Balance: ₹4000

4. Check Balance
   - Account Balance: ₹4000
```

---

## ⚠️ Limitations & Known Issues

1. **No Persistent Storage**: All data is lost when the program exits
2. **Single Account Per Session**: Only one account can be stored in memory at a time (per account type)
3. **Limited Validation**: Basic input validation only
4. **Legacy Code**: Uses deprecated headers (Turbo C++ style)
5. **No Interest Calculation**: No automated interest application
6. **No Transaction Log**: Individual transactions are not recorded
7. **Static Account Numbers**: Account numbers reset when program restarts
8. **No Security**: No password or authentication system

---

## 🚀 Future Enhancements

Suggested improvements for modernization and functionality:

1. **Database Integration**: Use SQLite or MySQL to persist data
2. **File-Based Storage**: Save account details to files
3. **Multi-Account Management**: Handle multiple accounts simultaneously
4. **Interest Calculation**: Implement interest accrual for savings accounts
5. **Transaction History**: Maintain detailed transaction logs
6. **PIN Protection**: Add security with PIN/password authentication
7. **Modern C++**: Refactor to use modern C++ standards (C++14/17/20)
8. **Cross-Platform**: Use standard libraries for broader compatibility
9. **GUI Interface**: Develop a graphical user interface
10. **Overdraft Facility**: Allow current accounts to have overdraft limits
11. **Cheque Management**: Add cheque book functionality
12. **Transfer Between Accounts**: Enable account-to-account transfers

---

## 📊 Code Statistics

- **Total Lines**: ~400+ lines
- **Classes**: 1 (bank)
- **Public Methods**: 6
- **Member Functions**: 2
- **Main Function**: 1 entry point

---

## 🎓 Learning Outcomes

This project demonstrates:

✅ **Object-Oriented Programming**

- Class definition and implementation
- Public and private access specifiers
- Static members and methods

✅ **Control Flow**

- Switch-case statements
- Do-while loops
- Conditional statements

✅ **User Interface**

- Console-based menu design
- Input/output operations
- Screen clearing and formatting

✅ **Data Management**

- Variable declaration and initialization
- Array usage for strings
- Data validation

---

## 💡 Algorithm Explanation

### Account Opening Process

```bash
1. Auto-generate account number (increment static counter)
2. Display generated account number
3. Take user input (name, address, phone, initial amount)
4. Validate minimum balance requirement
5. Store details in class member variables
6. Set initial balance
7. Display confirmation
```

### Withdrawal Process

```bash
1. Request account number from user
2. Validate account number
3. Display current balance
4. Request withdrawal amount
5. Validate amount ≤ balance
6. Deduct from balance
7. Display new balance
8. Show confirmation or error
```

---

## 🔐 Security Notes

**This is an educational project.** For production use, implement:

- Encryption for sensitive data
- User authentication
- Transaction logging
- Audit trails
- Data backup systems

---

## 📄 License

This is an open-source educational project. Feel free to use, modify, and distribute.

---

## 👨‍💻 Note

Created as a learning project to understand C++ fundamentals and banking system logic.

---

## 🎯 Conclusion

The Bank Management System is a fundamental project that introduces banking concepts through programming. While it has limitations, it serves as an excellent learning resource for understanding OOP principles, user interface design, and business logic implementation in C++.

**Ideal for:** Students, beginners in C++, anyone learning about system design and banking operations.

---
