# Meritshot
# 🚀 Amazon Redshift – Quick Guide for Data Engineers

Amazon Redshift is AWS’s fully managed data warehouse, designed for analyzing large volumes of data using SQL and cloud-native architecture. This guide helps you get started fast.

---

## 📌 What You’ll Learn

- What Redshift is and how it works
- How to set it up quickly on AWS
- How to run basic SQL commands
- Real-world use cases
- Best practices for performance

---

## 🧠 Core Concepts

- **Leader Node**: Manages queries and coordinates compute nodes.
- **Compute Nodes**: Store and process data in parallel.
- **Columnar Storage**: Speeds up analytics over large datasets.
- **DISTKEY / SORTKEY**: Optimize data distribution and query performance.
- **Redshift Spectrum**: Query data in S3 directly using SQL.

---

## ⚙️ Setup in 4 Steps

1. Go to AWS Console → Redshift → “Create Cluster”
2. Choose a node type (e.g., `dc2.large`)
3. Configure networking and IAM role (grant S3 access if needed)
4. Connect via SQL client (e.g., DBeaver, pgAdmin)

---

## 🧪 Basic SQL Commands

### Create a Table
```sql
CREATE TABLE users (
  user_id INT,
  name VARCHAR(50),
  email VARCHAR(100)
)
DISTKEY(user_id)
SORTKEY(name);
