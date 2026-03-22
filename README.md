# 🎵 Music Store Database Analytics

## 📌 Project Overview
This project focuses on analyzing a music store database using SQL to extract meaningful business insights related to customer behavior, revenue trends, and music preferences.

The analysis simulates real-world business decision-making by converting raw relational data into actionable insights.

---

## 🛠️ Tools & Technologies
- PostgreSQL  
- SQL (Joins, Aggregations, Subqueries, CTEs)  
- PgAdmin4  
- Relational Database Design  

---

## 🗂️ Database Schema
The database consists of multiple interconnected tables:

- Customer, Invoice, Invoice Line  
- Track, Album, Artist  
- Genre, Media Type  
- Playlist  

📷 Schema Diagram:

![Schema](schema.png)

---

## 📊 Key Business Questions Solved

### 🔹 Customer Analysis
- Who are the top customers based on spending?  
- Which customers contribute most to revenue?  

### 🔹 Revenue Insights
- Which countries generate the highest revenue?  
- Which cities have the best customers?  

### 🔹 Music Trends
- Most popular genres across countries  
- Best-selling artists and tracks  

### 🔹 Advanced Analysis
- Customer spending on specific artists  
- Genre popularity per country using window functions  

---

## 🧠 Sample SQL Query

```sql
SELECT C.CUSTOMER_ID, C.FIRST_NAME, C.LAST_NAME, SUM(I.TOTAL) AS total
FROM CUSTOMER C 
JOIN INVOICE I ON C.CUSTOMER_ID = I.CUSTOMER_ID
GROUP BY C.CUSTOMER_ID
ORDER BY TOTAL DESC
LIMIT 1;
```

---

## 📈 Key Insights
- High-revenue cities identified for business expansion  
- Top customers contribute significantly to overall revenue  
- Rock genre shows high popularity across multiple regions  
- Certain artists dominate sales in specific countries  

---

## 📁 Project Structure

```
music-store-database-analytics/
│
├── README.md
├── schema.png
├── music_database_analysis.sql
│
├── datasets/
│   ├── album.csv
│   ├── artist.csv
│   ├── customer.csv
│   ├── employee.csv
│   ├── genre.csv
│   ├── invoice.csv
│   ├── invoice_line.csv
│   ├── media_type.csv
│   ├── playlist.csv
│   ├── playlist_track.csv
│   ├── track.csv
```

---

## ▶️ How to Run This Project

1. Create a PostgreSQL database  
2. Import all CSV files into respective tables  
3. Run `music_database_analysis.sql`  
4. Analyze query outputs  

---

## 🚀 Conclusion
This project demonstrates how SQL can be used to transform structured data into meaningful business insights and support data-driven decision-making.

---

