# 🏎️ Web Scraping F1 Race Data (2011–2024)  

## 🚀 Stage 1: Data Collection & Preprocessing  

### 📌 Objective  
The goal of this project is to scrape **Formula 1 race data** from **StatsF1** for the seasons **2011 to 2024**. The dataset includes:  
✅ **Driver names**  
✅ **Points scored in each Grand Prix**  
✅ **Total points scored by each driver per season**  

---

### 📊 Dataset Structure  
- **Rows:** 274  
- **Columns:** 35  
- **Key Data Fields:**  
  - **Driver Name** 🏁  
  - **Season (Year)** 📅  
  - **Grand Prix Points (Australia, USA, etc.)** 🏆  
  - **Total Points per Season (Last Column)**  

⚠️ If a race did not occur in a specific season (e.g., **Turkey 2012**, **Russia 2011**), the corresponding cell is filled with **NaN** to maintain a consistent dataset structure.  

---

### 🔥 Challenges Faced  
🚧 **Data Availability Issues:** Could not scrape data for **2020 and 2021** due to website restrictions.  
🔄 **Inconsistent Race Order:** The order of Grand Prix races varies by season. Example:  
  - **2015 Malaysian GP was the second Grand prix but in 2016 Bahrain GP is the second grand prix, so there is no proper order in Grand prix.  
  - This required writing **season-specific scraping logic** for accurate alignment.  

---

### ⚙️ Approach  
### ✅ **Identifying Unique Race Locations**:  
Since the **Formula 1 calendar changes every year**, not all Grand Prix races happen in every season.  
For example:  
- **Turkey GP** happened in **2011, 2020, and 2021**, but not in other years.  
- **Russia GP** started in **2014** but didn’t exist in **2011–2013**.  

👉 **Solution**:  
To ensure consistency across all seasons, you first identified **all unique race locations** that appeared in any season from **2011 to 2024**. Then, you structured your dataset so that every season includes **all possible race columns**, even if that specific race didn’t occur that year (filled with `NaN`).  

---

### ✅ **Consistent Column Structure**:  
Since the number and order of races change every year, you needed a **fixed column format** to prevent issues when merging the data.  

👉 **Solution**:  
- I ensured that **every season’s dataset had the same set of columns** (even if a race wasn’t held, it still had a column).  
- This helped avoid **errors when merging** all the years together into a single dataset.  

Without this, merging different years would be chaotic because different seasons would have **different column names** based on the Grand Prix schedule of that year.  

---

### ✅ **Season-Specific Scraping Code**:  
Formula 1 does not have a fixed race schedule every year. The **order of races** changes annually.  

For example:  
- **2015 season**: The **2nd race** was in **Malaysia**.  
- **2016 season**: The **2nd race** was in **Bahrain**.  

👉 **Problem**:  
If you used the **same scraping code for all seasons**, the data would be misaligned because the **2nd column would represent different races in different years**.  

👉 **Solution**:  
To fix this, I wrote **custom scraping code for each season** to extract the races **in their correct order**.  
- This ensured that each race’s points were placed in the **correct Grand Prix column**, even though the order varied across years.  

---

### 🛠️ Tools & Libraries  
- **Python** 🐍  
- **Scrapy** 🕷️ (Web Scraping)  
- **Pandas** 📊 (Data Processing)  
- **OS Module** 🗂️ (File Handling)  
- **Jupyter Notebook** 📓  

---

### 🧹 Data Cleaning & Processing  
🔹 After scraping each season, data was converted to **CSV** format.  
🔹 Used the **OS library** to merge all individual season files.  
🔹 Performed **data cleaning**:  
   - **Blank values & hyphens** ➝ Replaced with `0` (Indicates no points scored).  
   - **NaN in Grand Prix columns** ➝ Converted to `pd.NA` for consistency.  
   - **Standardized Grand Prix columns to `Int32`** for numerical analysis.  

---

### 🎯 Outcome  
✔ **Successfully scraped** and structured F1 data for **2011–2024** (except 2020 & 2021).  
✔ Created a **unified dataset** with a structured format, ready for **analysis and further processing**.  

---

📌 **Next Steps:**
🚀 Moving to **Stage 2**, which will involve **data analysis and visualization!** 📊  

---




