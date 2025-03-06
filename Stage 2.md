## 🚀 **Stage 2: Data Cleaning, Normalization & Visualization**  

### 🏎️ **Data Preparation & Structuring**  

After merging and cleaning all the scraped data, I created a final dataset: `f1_clean.csv`. This involved:  
✅ **Normalization**: Standardizing data for consistency.  
✅ **Manual Data Collection**: Compiling driver-team associations for each season.  

To enhance data organization, I created three structured datasets:  
1️⃣ **`drivers_info`**: Contains `driver_name` and a unique `driver_id`.  
2️⃣ **`team_info`**: Contains `team_name` and a unique `team_id`.  
3️⃣ **`F1_master_file`**: The final dataset linking all details, including:  
   - `driver_id`, `team_id`, `year`  
   - Race-wise Grand Prix points  
   - **Total season points**  

---

### 🛠 **Database Integration & Visualization**  

📌 **Tech Stack Used:** `sqlite3`, `pandas`, `lets-plot`  

🔗 **SQL Joins**: Merged the structured data with `F1_master_file` using `sqlite3`, then converted it into a DataFrame for analysis.  

📊 **Visualization - 2024 Season Analysis**  
- **Top 10 Drivers Performance**:  
  - 📈 *Max Verstappen* showcased dominance, consistently averaging **18 points per Grand Prix**.  
  - 📉 *Lando Norris* gained momentum from the **China Grand Prix**, averaging **15 points per race**.  
  - 🏆 **2024 World Champion**: *Max Verstappen* clinched his **4th title**.  

- **Team Performance Over 2024 Season**:  
  - 🏎️ *Red Bull* led the standings until the **Netherlands Grand Prix**.  
  - 🔥 *McLaren* surged ahead in **Azerbaijan**, overtaking Red Bull.  
  - 🏁 *Ferrari* took the lead in **Mexico**, securing a dramatic finish.  
  - 🏆 **Constructors' Champion**: *McLaren*  
  - 🥈 **Runner-Up**: *Ferrari*  

---  
