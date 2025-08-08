# task-4-aggregate-functions-on-numeric-columns-GROUP-BY-and-HAVING




## **Step-by-Step Process**

### **1. Open MySQL**

* You can use **MySQL Workbench** (GUI) or the **MySQL CLI** (terminal).
* Make sure your database (`details_sales`) and table (`details_salesofe_corcess`) are already created and data is inserted.

---

### **2. Show all databases**

```sql
SHOW DATABASES;
```

* Lists all databases present in your MySQL server.
* This is just to check if `details_sales` exists.

---

### **3. Select the database**

```sql
USE details_sales;
```

* Tells MySQL that you want to work inside the **details\_sales** database.
* All further queries will be executed in this database.

---

### **4. See table structure**

```sql
DESCRIBE details_salesofe_corcess;
```

* Shows the columns, their data types, and constraints for the table.
* Good for confirming that your table structure is correct.

---

### **5. List all tables in the database**

```sql
SHOW TABLES;
```

* Displays the names of all tables in `details_sales`.
* You should see `details_salesofe_corcess` here.

---

### **6. View all data in the table**

```sql
SELECT * FROM details_salesofe_corcess;
```

* Shows every row and column from the table.
* Good for quickly checking if your data loaded properly.

---

### **7. Count total number of rows**

```sql
SELECT COUNT(*) FROM details_salesofe_corcess;
```

* Returns how many rows (orders) exist in the table.

---

### **8. Find total quantity sold**

```sql
SELECT SUM(Quantity) FROM details_salesofe_corcess;
```

* Adds up all values in the `Quantity` column.
* Tells you the **total number of items sold**.

---

### **9. Count quantity grouped by Amount**

```sql
SELECT COUNT(Quantity)
FROM details_salesofe_corcess
GROUP BY Amount
ORDER BY COUNT(Amount) DESC;
```

* Groups rows based on the **Amount** value.
* Counts how many rows have the same Amount.
* Orders results by the count in **descending order**.

---

### **10. Count orders grouped by Amount where quantity count > 5**

```sql
SELECT COUNT(Order_ID)
FROM details_salesofe_corcess
GROUP BY Amount
HAVING COUNT(Quantity) > 5;
```

* Groups rows by Amount.
* Counts how many orders exist in each Amount group.
* **HAVING** is used to filter groups where the **count of Quantity** is more than 5.

---

✅ **In simple words**:

1. First, you connect to MySQL and choose your database.
2. Then, you check the table structure and data.
3. Finally, you run queries to **count rows**, **sum sales quantities**, and **group data** for analysis.

---



Do you want me to make that?
