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

Here’s your updated version with placeholders for the HTML chart links:  

---

📊 **Visualization - 2024 Season Analysis**  

### **Overall Driver Performance - 2024 Season**  
📌 **[View Chart](https://rawcdn.githack.com/Evans-01/F1_Project/ff73a67da6ff8889b1dc6f69a8393afda5abac49/lets-plot-images/F1%202024%20Driver%20Points.html)** 
- *Jack Doohan* raced only **one** Grand Prix but scored **0 points**.  
- *Logan Sargeant* participated in only **half the season** and also scored **0 points**.  
- *Valtteri Bottas* raced the **full season** but failed to score any points.  

### **Top 10 Drivers Performance**  
📌 **[View Chart](https://rawcdn.githack.com/Evans-01/F1_Project/ff73a67da6ff8889b1dc6f69a8393afda5abac49/lets-plot-images/Top%2010%20Drivers%20of%202024.html)**  
- 📈 *Max Verstappen* showcased dominance, consistently averaging **18 points per Grand Prix**.  
- 📉 *Lando Norris* gained momentum from the **China Grand Prix**, averaging **15 points per race**.  
- 🏆 **2024 World Champion**: *Max Verstappen* clinched his **4th title**.  

### **Team Performance Over 2024 Season**  
📌 **[View Chart](https://rawcdn.githack.com/Evans-01/F1_Project/ff73a67da6ff8889b1dc6f69a8393afda5abac49/lets-plot-images/F1%202024%20Team%20Progression.html)**   
- 🏎️ *Red Bull* led the standings until the **Netherlands Grand Prix**.  
- 🔥 *McLaren* surged ahead in **Azerbaijan**, overtaking Red Bull.  
- 🏁 *Ferrari* took the lead in **Mexico**, securing a dramatic finish.  
- 🏆 **Constructors' Champion**: *McLaren*  
- 🥈 **Runner-Up**: *Ferrari*  

### **Championship Winners & Runners-Up (2011-2024)** *(Excluding 2020 & 2021)*  
📌 **[View Chart](https://rawcdn.githack.com/Evans-01/F1_Project/ff73a67da6ff8889b1dc6f69a8393afda5abac49/lets-plot-images/Runner%20and%20Winner%20of%20Every%20Season.html)**   
- 🏆 *Lewis Hamilton*: **5 titles** (*2014, 2015, 2017, 2018, 2019*).  
- 🏆 *Sebastian Vettel*: **3 titles**.  
- 🏆 *Max Verstappen*: **3 titles**.  

---
