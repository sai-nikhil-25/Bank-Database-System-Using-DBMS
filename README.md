# **📊 Bank Management System - README**

---

## **📌 Project Overview**  
The **Bank Management System** is a robust database project designed to manage various banking operations, including **customer accounts, branches, employee records, services, and transactions**. It ensures smooth and secure handling of bank processes using a well-structured and normalized relational database.

---

## **✨ Key Features**

- **👥 Customer Management:**  
  Manage customer details, including names, contact numbers, and identification numbers.

- **💼 Account Management:**  
  Track different types of bank accounts, their balances, statuses, and associated customers.

- **🏢 Branch Information:**  
  Store branch details, such as branch type, contact information, and operating hours.

- **🔁 Service Records:**  
  Maintain records of services like deposits, withdrawals, loans, and transfers linked to feedback and transactions.

- **👩‍💼 Employee Management:**  
  Store employee details, including their designations, salaries, and assigned branches.

- **📝 Feedback and Transactions:**  
  Record customer feedback and service details for better performance tracking.

---

## **💻 Technologies Used**
- **Oracle SQL:** Database design, table creation, and query execution.  
- **SQL Queries:** Data retrieval, updates, and deletions.  
- **Normalization:** Up to **BCNF** to reduce redundancy and improve efficiency.

---

## **📚 Database Design Components**

### **1. Entities and Attributes**  
- **👥 Customer:** Store customer names, contact details, and IDs.  
- **💼 Account:** Track account types, balances, and opening dates.  
- **🏢 Branch:** Store branch locations, operating hours, and contact information.  
- **👩‍💼 Employees:** Store employee data, including job titles and salaries.  
- **🔁 Services:** Maintain records of services and transactions.  
- **📝 Feedback:** Collect and store customer feedback.

### **2. Normalization Steps**  
- **1NF:** Atomic values, no repeating groups.  
- **2NF:** No partial dependencies.  
- **3NF:** No transitive dependencies.  
- **BCNF:** Satisfy all functional dependencies.

### **3. Entity-Relationship Diagram**  
Defines relationships such as:  
- One-to-many between customers and accounts.  
- Many-to-one between branches and employees.  
- Many-to-many between services and accounts.

---

## **🔄 Project Workflow**

1. **🛠️ Schema Design:**  
   Created tables with primary and foreign key constraints to maintain relationships.

2. **📥 Data Insertion:**  
   Populated tables with sample data using SQL `INSERT` statements.

3. **🔍 Data Queries:**  
   Performed data retrieval, updates, and deletions through structured queries.

---

## **📑 Key SQL Queries**

1. **List of Customers:**  
   ```sql
   SELECT CustomerID, FirstName, LastName, PhoneNumber FROM Customer;
   ```

2. **Customers with Savings Balance > $2000:**  
   ```sql
   SELECT Customer.FirstName, Customer.LastName
   FROM Customer
   JOIN Accounts ON Customer.CustomerID = Accounts.CustomerID
   WHERE Accounts.Account_Type = 'Savings' AND Accounts.Balance > 2000;
   ```

3. **Branch with Highest Active Accounts:**  
   ```sql
   SELECT BranchName, COUNT(Account_Number) AS ActiveAccounts
   FROM Branch
   JOIN Accounts ON Branch.BranchID = Accounts.BranchID
   WHERE Accounts.Account_Status = 'Active'
   GROUP BY BranchName
   ORDER BY ActiveAccounts DESC;
   ```

---

## **🚀 How to Run the Project**

1. **Install Oracle SQL:**  
   Set up and configure Oracle SQL on your system.

2. **Run SQL Scripts:**  
   Execute the provided scripts to create the database tables and populate them with sample data.

3. **Test the System:**  
   Run SQL queries to retrieve and manipulate data.

---

## **💡 Project Challenges and Learnings**
- **Challenge:** Managing transitive dependencies and ensuring efficient normalization.  
- **Learning:** Gained hands-on experience with BCNF and optimized SQL queries.  
- **Outcome:** Successfully designed a scalable and normalized database system.

---

## **👥 Contributors**
- **Kunduri Sai Nikhil Reddy**  
- **Kakanuru Harshitha**  
- **Ganne Eswar Chandra Vidya Sagar**  
- **Garikapati Chandanika**  
- **Muniganti Venu**

---

## **📈 Conclusion**  
This project provided practical experience in database management by applying theoretical concepts like normalization and complex SQL queries. It emphasized the importance of scalability and optimization in real-world database development.
