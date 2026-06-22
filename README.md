# 🛒 SuperShop Management System

A Java desktop application for managing retail shop operations, built with Swing GUI and CSV-based persistence. Developed as a CSE 202 (Object Oriented Programming I Lab) project at **University of Asia Pacific**.

---

## 👥 Team — Mad Thinkers

| Name | ID | Section |
|---|---|---|
| Md. Zubaer | 24101106 | B2 |
| Nasim Mahmud | 24201104 | B2 |
| Dipraj Mitra Chandon | 24201091 | B2 |
| Yeasen Ahmed | 24201089 | B2 |

---

## 📌 Features

### 🔐 Authentication
- Role-based login for **Admin** and **Employee**
- Secure credential validation via `AuthController`
- Default admin account auto-created on first run

### 🧑‍💼 Admin Panel
- Add, update, and delete employee records
- View daily sales report
- Monitor inventory stock levels
- Restock low-stock items

### 🏪 Employee Panel
- Add, update, delete, and search inventory items
- Support for **Standard** and **Discounted** items
- Shopping cart with dynamic pricing
- Generate and print itemised customer invoices

### 💾 Data Persistence
- All data stored in CSV flat files (`employees.csv`, `items.csv`, `invoices.csv`)
- Data survives application restarts with no loss
- Bill numbering resumes correctly across sessions

---

## 🏗️ Project Structure

```
SuperShop/
├── Main.java
├── controllers/
│   ├── AuthController.java
│   ├── UserController.java
│   ├── InventoryController.java
│   └── BillingController.java
├── dao/
│   └── CSVHandler.java
├── models/
│   ├── User.java          (abstract)
│   ├── Admin.java
│   ├── Employee.java
│   ├── Item.java          (abstract)
│   ├── StandardItem.java
│   ├── DiscountItem.java
│   └── Bill.java
└── view/
    ├── LoginFrame.java
    ├── AdminDashboard.java
    ├── EmployeeDashboard.java
    ├── AddEmployeeDialog.java
    ├── UpdateEmployeeDialog.java
    ├── AddItemDialog.java
    ├── UpdateItemDialog.java
    ├── SearchItemDialog.java
    ├── BillingDialog.java
    └── SalesReportDialog.java
```

---

## 🧠 OOP Concepts Applied

| Concept | Implementation |
|---|---|
| **Abstraction** | `User` and `Item` are abstract classes defining contracts |
| **Inheritance** | `Admin`, `Employee` extend `User`; `StandardItem`, `DiscountItem` extend `Item` |
| **Encapsulation** | All fields are `private`/`protected`, accessed via getters/setters |
| **Polymorphism** | `calculatePrice()` overridden in `StandardItem` and `DiscountItem`; resolved at runtime |
| **MVC Pattern** | View, Controller, and Model layers are strictly separated |

---

## 🛠️ Tech Stack

| Category | Detail |
|---|---|
| Language | Java (JDK 17+) |
| GUI | Java Swing |
| Storage | CSV flat files |
| IDE | IntelliJ IDEA / Eclipse / NetBeans |
| OS | Windows 10/11 |

---

## 🚀 Getting Started

### Prerequisites
- JDK 17 or higher installed
- Any Java IDE or command-line tools

### Run the project

**Via IDE:**
1. Clone the repository
2. Open the project in IntelliJ IDEA, Eclipse, or NetBeans
3. Run `Main.java`

**Via command line:**
```bash
javac -d out $(find . -name "*.java")
java -cp out Main
```

### Default login credentials

| Role | ID | Password |
|---|---|---|
| Admin | `ADMIN001` | `admin123` |

> Employee credentials are created by the Admin through the dashboard.

---

## 📁 Data Files

Auto-generated in the `data/` directory on first run:

```
data/
├── employees.csv   # id, name, password, role, shift, phone
├── items.csv       # id, name, basePrice, discountPercent, stock, type
└── invoices.csv    # billId, employeeId, dateTime, grandTotal, itemCount
```

---

## 📸 Screenshots

| Login | Admin Dashboard | Employee Dashboard |
|---|---|---|
| Role-select login form | Employee CRUD + sales report | Inventory & billing |

*(See the project report for full UI screenshots.)*

---

## 🔗 Project Links

- **GitHub:** [github.com/jubayermd10/Mad-Thinkers](https://github.com/jubayermd10/Mad-Thinkers)
- **Google Drive:** [Source code & demo](https://drive.google.com/drive/u/0/folders/1avBxbe-Ivo1xImy5TOA6-bkPqAz5Q5lx)

---

## 📄 License

This project was developed for academic purposes at the University of Asia Pacific.  
© 2026 Mad Thinkers — CSE 202 Lab Project
