# ⚽ Intelligent Football Transfer Recommendation

## 📥 What Does It Do
This application helps football clubs **find the best players to sign**, based on:
- Transfer Budget (mandatory)
- Select Club (mandatory, from top 5 leagues)
- Min Age (optional)
- Max Age (optional)
- Nationality (optional)

> ![1](https://github.com/user-attachments/assets/2d81ba4b-dc1e-477c-ac28-c03eabbbfa5b2c)

---

## 🔍 How It Works
- Analyzes each club’s **weakest 5 parameters** in the league table (e.g., xGA, Home_L, GA, etc.)
- Maps these weaknesses to relevant **player performance stats** (e.g., Expected_xGA, Expected_npxG)
- Calculates **percentiles** for each player on these stats to get a balanced total score
- Applies realistic filters:
  - Excludes players from the same club
  - Excludes players from clubs that finished **more than 3 places higher** in the league table
  - Excludes players without valid market value or beyond transfer budget

---

## 📊 Results
Generates a ranked list of recommended players including:
- Player name
- Club
- Position
- Nation
- Age
- Market value
- Total score percentile

> ![2](https://github.com/user-attachments/assets/ab94747c-aa8e-4031-b286-b3cb23e75b2c)

---

## 🗂 Data
- Dataset was **custom-built**:
  - Collected raw player and club data from multiple public football sources
  - Used PySpark scripts to clean, merge, and transform
- Covers:
  - Player stats & transfer market value
  - League tables for Premier League, La Liga, Bundesliga, Serie A, Ligue 1
- No direct data source offers this combined dataset; it was built through multiple transformations

---

## 🎬 Demo
Example: recommending transfers for **Everton** with:
- Transfer budget: 60 million €
- Max player age: 27

> ![1](https://github.com/user-attachments/assets/d0155dca-195b-4ece-b1fd-4a314e1df8e1)

After running:
- Identifies Everton’s weakest parameters
- Maps to player stats
- Ranks players by percentile score

> ![image](https://github.com/user-attachments/assets/9edf9068-1e86-4a2d-9f15-7fd350b7df03)

---

## ⚙ Tech Stack
- **PySpark** in Databricks notebooks
- DataFrames, Window functions, safe type casting
- Dynamic dropdown & widgets for user input
- Custom percentile scoring logic

---

## 🧠 Why It’s Interesting
- Dataset created manually by combining multiple sources
- Avoids unrealistic transfers by checking league position constraints
- Fully dynamic: user can filter by age, position, nationality, etc.
- Scalable: PySpark handles large data

---

## 🚀 Future Work & Ideas
- Store processed data in **Azure Data Lake** or Blob Storage
- Use **Databricks Workflows** for automated ETL and refreshing
- Build **Power BI** dashboards or **Streamlit** apps for visualization
- Add real-time updates using football APIs
- Integrate **machine learning** for advanced player rating or price prediction

---

## ✅ Conclusion
A practical **end-to-end data engineering project** built entirely in Databricks:
- From raw data collection → cleaning → transformation → analysis → recommendations
- Combines sports context with data engineering & analytics
- Ready to be expanded with cloud & visualization tools

---

> ⚡ **Built by combining football data engineering & analytics for intelligent transfer decisions!**
