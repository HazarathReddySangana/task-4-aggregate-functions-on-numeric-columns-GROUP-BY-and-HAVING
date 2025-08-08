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

<img width="681" height="374" alt="Image" src="https://github.com/user-attachments/assets/6306752d-af7d-4620-8bb5-a54937df41d0" />
<img width="676" height="318" alt="Image" src="https://github.com/user-attachments/assets/358982bc-be16-40db-9b3a-b50b2cace3ab" />
<img width="452" height="584" alt="Image" src="https://github.com/user-attachments/assets/e8271e58-5ed1-42be-a17e-402928e62258" />
<img width="499" height="598" alt="Image" src="https://github.com/user-attachments/assets/871623dd-02af-42ba-b270-d3d557732d27" />
<img width="1235" height="532" alt="Image" src="https://github.com/user-attachments/assets/06b64d6f-3485-4dc3-a35e-7113b8c115ba" />
