# ⚽ FIFA 2026 Player Insights — Archetypes, World-Class Probability, and Shortlist

> End-to-end data science project: engineer soccer features, discover player archetypes (unsupervised), predict “World-Class by 2026” (supervised), and export a recruitment shortlist.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4%2B-orange)
![Status](https://img.shields.io/badge/status-completed-brightgreen)

---

## 1️⃣ Project Goal
Identify **undervalued, high-potential players** for 2026 squads by:
- Engineering **position-aware features** (per-90, indices, trajectory, form)
- Clustering to find **player archetypes** (e.g., Poacher, Playmaker, Defensive Rock, Shot-Stop GK)
- Training a **balanced classifier** to estimate *World-Class by 2026* probability


---

## 2️⃣ Data
- **File(s):**
  `data/fifa2026_players.csv`

- **Columns:**  
  `name, age, nationality, club, position, minutes_played_24_25, goals, assists, shots, key_passes, xG, xA, pass_accuracy_pct, tackles, interceptions, clearances, aerials_won, saves, clean_sheets, injury_days_24_25`.

> Notes: GK-only fields are NaN for outfielders (and vice versa) to practice realistic cleaning.

---

##  3️⃣ Workflow
1. **Data Cleaning**  
   - Handle NaN values by position (GK vs outfield)
   - Standardize numeric ranges
   - Encode categorical variables  

2. **Feature Engineering**  
   - Per-90 stats (goals, assists, tackles, etc.)  
   - Composite indices (FinishingIndex, CreatorIndex, StopperIndex, ShotStopIndex)  
   - Form trends (2023–2025)  

3. **Exploratory Data Analysis (EDA)**  
   - Correlation heatmaps  
   - Archetype clustering visualizations  
   - Distributions by position & age  

4. **Machine Learning Models**  
   - **Unsupervised:** KMeans clustering for player archetypes  
   - **Supervised:** Random Forest & Logistic Regression for World-Class prediction  
   - **Evaluation:** Precision metric for scouting use-cases  




