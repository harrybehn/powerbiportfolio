## 🎰 Gaming Performance Monthly & Yearly Monitoring

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

This Power BI dashboard is one of the projects that i created in my current job as a Data Analyst in an integrated resort but using fictional data. This dashboard provides insights into **gaming performance metrics** by analyzing **Unique Players, Theoritical Win, Actual Win and Coin In Statistics** across different nationalities ,gaming areas and game type in weekly , monthly and yearly basis.

---

## 📊 Dashboard Overview

### 🔹 Unique Players, Theo Win, Actual Win & Coin In Analysis
- Monitor unique players, Theo Win, Actual Win & Coin In by **nationality** (Philippines, USA, Others).
- Compares Unique player, Theo Win, Actual Win & Coin In against **previous weeks** (P1W, P2W, P3W).
- Shows **percentage change** vs. the same day last week.

See dashboard screenshot
![Image](https://github.com/user-attachments/assets/94c4ca2c-7500-4a40-9162-0abaaa112b41)

### 🔹 Gaming Types & Areas
- **Game Types**: Slot, Table
- **Gaming Areas**: Mass Gaming, VIP Areas 1-4

### 📈 Trends & Visualizations
- **Bar charts** compare **yearly trends (2016, 2017, 2018)**.
- Tracks **monthly Coin In performance** for **overall and by nationality**.
- Shows **growth or decline trends**.
  
![Image](https://github.com/user-attachments/assets/c4f8ed57-9e2e-412e-8b8b-99556c366c1a) 
---

## 🚀 Key Features
✅ **Comparative Performance Tracking** – View daily, weekly, and yearly changes.  
✅ **Nationality-Based Analysis** – Understand gaming trends by demographic.  
✅ **Visual Insights** – Intuitive graphs for quick trend assessment.  
✅ **Gaming Area & Type Segmentation** – Detailed breakdown for slot & table games.   

---

## 📌 Usage
1. **Open Power BI** and load the `.pbix` file.  
2. **Explore the dashboards** for insights.  

---

## Steps followed 

### Step 1 : 
- **Load data into Power BI Desktop**.
- I use excel files in this project but in my actual work I would extract data from sql server and I would usually use native query for optimization.
- I used three datasets for this project namely, PlayerGamingSession1, Player, Nationality and PlayerGamingSession2. 
- PlayerGamingSession1 contains the columns PlayerID, Win(Actual Win), TheoWin, GamingArea, GameType and Dateplayed.
- PlayerGamingSession2 contains the columns PlayerID, Win(Actual Win), TheoWin, GamingArea, GameType, Month and Year.
- Player contains columns PlayerID and NationalityCode. Nationality contains columns NationalityCode and description.

### Step 2 :
- **Merge Queries**.
-  Next step is to merge Nationality table to Player table using the nationalitycode column to get the nationality description.
- Then merge Player table to PlayerGamingSession1 and PlayerGamingSession2. Close and Apply.

### Step 3 : Weekly Monitoring
### Step 3.1
- **Create Calculated Columns**.
- Create NationalityGroup column to group the nationaties into Philippines, USA and others.
  ![Image](https://github.com/user-attachments/assets/155a747f-41e3-4a3c-8ed9-1860eee9389a)
- Create DateRange column to compare weekly performance. I used a fixed date in this project but in my work I use a dynamic date using this dax formula: Yesterday = today() - 1, P1W = today() - 8, ..etc.
  ![Image](https://github.com/user-attachments/assets/12bd71c2-94be-4fac-add3-4eb2a226fb23)

### Step 3.2 :
- **Create Measures**.
- Create measures for total Unique Players, total TheoWin, total Actual Win and total Coin In.
  ![Image](https://github.com/user-attachments/assets/f2538be6-c8eb-47d2-97e3-d0512b70df08)

### Step 3.3 :
- **Create Visualization for Weekly Gaming performance**.
- Use Matrix visual to visualize Unique Players by nationality and by DataRange.
 ![Image](https://github.com/user-attachments/assets/ac00bf95-5bec-41d7-8802-a538a14956c2)

### Step 3.4 :
- **Create Visualization for Weekly Percentage Change**.
- Create measures for Weekly Percentage Change for Unique Player Count
  ![Image](https://github.com/user-attachments/assets/472d0991-26f8-4e96-aa76-16f2181474a2)
- Do the same for TheoWin, Actual Win and Coin In
