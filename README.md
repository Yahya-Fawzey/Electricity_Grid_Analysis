# Analysis of U.S. Electricity Grid Patterns & Performance 

## 🎯 Project Goal
The goal of this project was to analyze **hourly electricity data** for three major U.S. grid operators (**CISO, ERCO, and PJM**) to identify key **consumption patterns**, understand **inter-regional power dynamics**, and evaluate the accuracy of **demand forecasts**.

---

## 💾 Data Source
The data was sourced from the **U.S. Energy Information Administration (EIA) API**, covering the period from **January 1, 2025, to August 18, 2025**.

---

## 🔢 Key Steps
1. **Data Ingestion** – Fetched over **700,000 records** from the EIA API using a pagination loop to handle the API's 5,000-record limit.  
2. **Data Cleaning & Preparation** – Handled complex **time zone** issues by converting all UTC timestamps to the correct local time for each region.  
3. **Exploratory Data Analysis (EDA)** – Analyzed and visualized daily, weekly, and seasonal demand patterns.  
4. **Comparative Analysis** – Compared the demand profiles, seasonal peaks, and inter-regional power trading of the three grid operators.  
5. **Performance Evaluation** – Assessed the accuracy of the day-ahead demand forecasts by calculating the **Mean Absolute Percentage Error (MAPE)** for each region.  

---

## 🛠️ Project Challenges & Solutions
- **Challenge: API Pagination** – The initial API request was capped at 5,000 records.  
  **Solution:** Implemented a pagination loop using the `offset` parameter to fetch the complete dataset.  

- **Challenge: Time Zone Inaccuracy** – Initial plots showed a misleading late-night peak due to data being in UTC.  
  **Solution:** Converted timestamps to the correct **local time zone** for each region, which fixed the demand curves.  

---

## 💡 Key Insights
- **Peak Demand** – All regions show a clear **evening peak** between 4 PM and 7 PM local time.  
- **Seasonal Patterns** – ERCO (Texas) and CISO (California) are *summer-peaking* grids, with ERCO’s summer demand **20% higher** than its winter demand. PJM is a *dual-peaking* grid with nearly identical demand in both seasons.  
- **Grid Inter-dependency** – CISO is a major **net importer** of electricity, PJM is a major **net exporter**, and ERCO operates as a largely self-sufficient **“energy island.”**  
- **Forecast Accuracy** – ERCO had the most accurate forecast (**MAPE ~2.5%**), while CISO was the least accurate (**MAPE >8%**).  

---

## 💻 Tools & Libraries Used
- Python  
- Pandas  
- Matplotlib  
- Seaborn  
- Requests  
- python-dotenv  

---

📄 For a detailed walkthrough of the analysis, including all visualizations and insights, please see the **[Full Project Report (PDF)](link/to/your/report.pdf)**.
