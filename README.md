# Convert Unstructured Data into Structured Data
# 🚀 Convert Unstructured Data into Structured Data using Azure Data Factory

## 🧑‍💻 Internship Project

This project shows how we can change unstructured data (like a CSV file) into proper structured data (rows and columns) using **Azure Data Factory (ADF)**.

---

## 🎯 Project Goal

We had a CSV file with data (like student data), stored in Azure Blob Storage.  
Our goal was to send this data to an **Azure SQL Database**, where it can be stored in table format (structured form).

We used **Azure Data Factory** to do this work step-by-step.

---

## 🔧 Tools Used

- Azure Storage Account  
- Azure Blob Storage  
- Azure SQL Database  
- Azure Data Factory (ADF)

---

## ✅ Step-by-Step Process

### 📁 Step 1: Upload CSV File to Blob Storage

- First, we created a **Storage Account** in Azure.
- Then we created a **Container** inside Blob Storage.
- After that, we uploaded our **CSV file** (example: `StudentData.csv`) into the container.

🖼️ _Screenshot: Upload CSV to Blob Storage_

---

### 🔗 Step 2: Create Linked Service for Blob Storage

- In Azure Data Factory, we created a new **Linked Service**.
- This Linked Service connects ADF with our Blob Storage.
- We selected the storage account and provided connection details.

🖼️ _Screenshot: Linked Service for Blob Storage_

---

### 🗃️ Step 3: Create Dataset for CSV File (Source)

- We created a **Dataset** in ADF which represents our CSV file.
- We selected the correct container and file path.
- We also set the file format (comma-separated).

🖼️ _Screenshot: Dataset for CSV File_

---

### 🧩 Step 4: Create Linked Service for Azure SQL Database

- Now we created another **Linked Service**, this time for Azure SQL.
- We selected our Azure SQL Database and added login details.
- This will allow ADF to push data into the SQL table.

🖼️ _Screenshot: Linked Service for Azure SQL_

---

### 🧾 Step 5: Create Dataset for SQL Table (Sink)

- Here, we created a **Dataset** for the destination (SQL table).
- We selected the correct table where we want to store our CSV data.

🖼️ _Screenshot: Dataset for SQL Table_

---

### 📦 Step 6: Create Pipeline with Copy Activity

- In ADF, we created a new **Pipeline**.
- Inside the pipeline, we added a **Copy Activity**.
- In Copy Activity:
  - **Source**: CSV file dataset  
  - **Sink**: Azure SQL table dataset

🖼️ _Screenshot: Copy Activity in Pipeline_

---

### ▶️ Step 7: Run the Pipeline (Trigger)

- We manually ran the pipeline to check if the data is going from Blob to SQL properly.
- The run was successful.

🖼️ _Screenshot: Pipeline run successful_

---

### 📅 Step 8: Create Trigger for Scheduling (Optional)

- If we want the pipeline to run daily or on a schedule, we can create a **Trigger**.
- We selected the time and connected it with our pipeline.

🖼️ _Screenshot: Trigger Created_

---

### 📊 Step 9: Verify Data in Azure SQL Table

- Finally, we checked the Azure SQL table.
- Our CSV data was successfully inserted as rows in the table.

🖼️ _Screenshot: Azure SQL Table Output_

---

## 📌 Conclusion

This project helped me understand how to:
- Use Azure Data Factory
- Move data between services
- Work with Linked Services, Datasets, and Pipelines
- Schedule tasks using triggers

This was a good learning experience and is useful in real-world data handling projects.

---

## 📎 Project Submitted By:

**Your Name:** _Pradeep Gurjar_  
**Internship Role:** _Cybersecurity / Cloud Intern_  
**Company:** _[Your Company Name]_  
**Date:** 23rd July 2025

---
