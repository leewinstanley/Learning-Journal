# **REVISION NOTES: Storing and Querying Data**

## **1. Data Storage Options**
### **1.1 Filesystem (FS)**
- Hierarchical structure (folders, subfolders, and files).
- Stores **text data** (.txt, .csv) and **binary data** (images, executables).
- **Common commands** (PowerShell/Linux):
  - `ls` – List files in a directory.
  - `cd <directory>` – Change directory.
  - `mkdir <name>` – Create a folder.
  - `rm <filename>` – Delete a file.
  - `cp <source> <destination>` – Copy a file.
  - `mv <source> <destination>` – Move/rename a file.

![Filesystem Diagram](filesystem_diagram.png)

---

### **1.2 Relational Databases (RDBMS - SQL)**
- Stores **structured data** in **tables** with rows & columns.
- Examples: MySQL, PostgreSQL, SQL Server, Oracle DB.
- **Core elements**:
  - **Tables (Relations)** – Store structured data.
  - **Columns (Attributes)** – Define the data type.
  - **Rows (Tuples)** – Individual records.
  - **Keys** – Unique identifiers (e.g., `PRIMARY KEY`).

![SQL Table Example](sql_table.png)

**Advantages:** ✅ Structured, ✅ Query optimization, ✅ Data integrity.

**Limitations:** ❌ Not ideal for unstructured data, ❌ Scaling can be costly.

---

### **1.3 Non-Relational Databases (NoSQL)**
- Designed for **flexibility, scalability, and speed**.
- **Types of NoSQL Databases:**
  - **Key-Value Stores** (e.g., Redis, DynamoDB).
  - **Document Stores** (e.g., MongoDB, CouchDB).
  - **Column-Family Stores** (e.g., Cassandra, BigTable).
  - **Graph Databases** (e.g., Neo4j).

![SQL vs NoSQL](sql_vs_nosql.png)

---

## **2. From Files to Databases**
### **Why move from files to databases?**
1. **Scalability** – Handles large data efficiently.
2. **Querying** – SQL provides fast data retrieval.
3. **Security** – Encryption, authentication, access control.
4. **Data Integrity** – Constraints (`PRIMARY KEY`, `FOREIGN KEY`).

![Files vs Databases](files_vs_databases.png)

---

## **3. Cloud Storage & Databases**
### **Types of Cloud Storage**
| Storage Type | Features | Example Services |
|-------------|----------|-----------------|
| **Block Storage** | High-performance, like local disks | Amazon EBS |
| **File Storage** | Scalable, like a shared drive | Amazon EFS |
| **Object Storage** | Stores any data type, low-cost | Amazon S3 |

![Cloud Storage](cloud_storage.png)

---

## **4. Data Models**
### **4.1 Relational Model (SQL Databases)**
- **Structure:** Data stored in tables.
- **Operations:** Queries using SQL (`SELECT`, `UPDATE`, `DELETE`).
- **Constraints:** Define rules like **uniqueness** & **relationships**.

### **4.2 NoSQL Data Models**
- **Key-Value Model** – Simple key-value pairs (e.g., Redis).
- **Document Model** – JSON-like documents (e.g., MongoDB).
- **Graph Model** – Nodes & relationships (e.g., Neo4j).

![SQL vs NoSQL Models](sql_nosql_models.png)

---

## **5. SQL Basics**
### **5.1 Data Definition Language (DDL)**
```sql
CREATE TABLE Customers (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
```

```sql
ALTER TABLE Customers ADD email VARCHAR(100);
```

```sql
DROP TABLE Customers;
```

### **5.2 Data Manipulation Language (DML)**
```sql
INSERT INTO Customers (id, name, age) VALUES (1, 'John Doe', 30);
```

```sql
UPDATE Customers SET age = 31 WHERE id = 1;
```

```sql
DELETE FROM Customers WHERE id = 1;
```

![SQL Queries](sql_queries.png)

---

## **6. AWS Redshift (Cloud Data Warehousing)**
- **What is AWS Redshift?**
  - A cloud-based **data warehouse** for large-scale storage & analytics.
  - Handles **structured & unstructured** data.
  - Supports **SQL-based querying** on petabyte-scale datasets.

- **Why use Redshift?**
  ✅ Scales easily for big data analytics  
  ✅ Built-in encryption for security  
  ✅ Compatible with BI tools (e.g., Tableau, PowerBI)  

### **6.1 Redshift Workflow**
1️⃣ Store data in Amazon **S3**  
2️⃣ Load data into **Redshift**  
3️⃣ Query using **SQL**  
4️⃣ Visualize insights using BI tools  

![Redshift Architecture](redshift_architecture.png)

---

## **7. Choosing the Right Database**
### **Factors to Consider:**
- **Application workload** – OLTP (Transactional) vs. OLAP (Analytics).
- **Data shape** – Structured (SQL) vs. Unstructured (NoSQL).
- **Performance needs** – High-speed vs. batch processing.

![Choosing a Database](choosing_database.png)

---

# **✅ SUMMARY & KEY TAKEAWAYS**
🔹 Filesystems store basic text/binary data, while databases handle structured queries.  
🔹 RDBMS (SQL) is best for structured data, while NoSQL is flexible for semi/unstructured data.  
🔹 Cloud storage (S3, EBS, EFS) and Data Warehouses (Redshift) support scalability & analytics.  
🔹 SQL is the standard language for querying relational databases.  
🔹 Choosing the right database depends on workload, data type, and performance needs.  

![Summary Mind Map](summary_mind_map.png)


