# 🇩🇪 Germany 2022 FIFA World Cup Root Cause Analysis

## 📖 Project Overview

Germany entered the 2022 FIFA World Cup as one of the tournament favorites but was eliminated during the group stage. Although the team scored six goals across three matches, they failed to qualify for the knockout stage.

This project performs an end-to-end data analysis to identify the primary reasons behind Germany's elimination. Using PostgreSQL for data storage and Power BI for visualization, the project analyzes attacking performance, midfield control, defensive engagement, and goalkeeping efficiency to determine the key factors that influenced Germany's campaign.

---

# ❓ Problem Statement

Germany finished third in Group E and was eliminated from the FIFA World Cup 2022.

The objective of this project is to answer one question:

**Why did Germany fail to qualify for the knockout stage despite creating numerous attacking opportunities?**

Rather than relying on opinions, this project uses match statistics and visual analytics to identify the primary and secondary causes behind Germany's group-stage exit.

---

# 🎯 Objectives

- Analyze Germany's attacking performance throughout the group stage.
- Evaluate midfield control and ball progression.
- Assess defensive performance using duel and interception statistics.
- Measure goalkeeper performance using advanced goalkeeping metrics.
- Perform a root cause analysis based on statistical evidence.
- Build an interactive Power BI dashboard for data-driven storytelling.

---

# 📊 Dataset

The analysis is based on Germany's three FIFA World Cup 2022 group-stage matches:

- Germany vs Japan
- Spain vs Germany
- Costa Rica vs Germany

The dataset includes match-level team statistics covering:

- Attack
- Passing
- Possession
- Defense
- Duels
- Goalkeeping
- Shooting
- Match Summary

---

# 🛠 Tech Stack

### Database
- PostgreSQL

### Query Language
- SQL

### Data Processing
- Python
- Pandas

### Data Visualization
- Microsoft Power BI

### Power BI Features
- DAX Measures
- Calculated Columns
- Star Schema
- Interactive Dashboard
- KPI Cards
- Slicers

---

# 🔄 Analytics Workflow

```
Data Collection
        │
        ▼
Data Cleaning & Validation
        │
        ▼
PostgreSQL Database
        │
        ▼
SQL Queries
        │
        ▼
Power BI Data Modeling
        │
        ▼
DAX Measures
        │
        ▼
Interactive Dashboard
        │
        ▼
Root Cause Analysis
```

---

# 🗄 Database Schema

The project follows a **Star Schema** design.

## Dimension Table

### dim_match

Contains general information for each match and acts as the central lookup table.

---

## Fact Tables

### Attack
- Goals
- Expected Goals (xG)
- Big Chances
- Big Chances Missed
- Shots on Target
- Touches in Opposition Box
- Final Third Entries

### Passing
- Accurate Passes
- Pass Accuracy
- Through Balls
- Cross Accuracy
- Final Third Passes

### Possession
- Possession Percentage

### Defending
- Tackles
- Interceptions
- Clearances
- Errors Leading to Shot
- Errors Leading to Goal

### Duels
- Ground Duel Success
- Aerial Duel Success
- Total Duel Success

### Goalkeeping
- Saves
- Big Saves
- Goals Prevented

### Match Summary
- Goals Scored
- Goals Conceded
- Match Result

---

# ⭐ Data Model

The dashboard follows a **Star Schema** where all fact tables are connected to a single dimension table (`dim_match`) using the match identifier.

Relationships:

- dim_match → Attack
- dim_match → Passing
- dim_match → Possession
- dim_match → Defending
- dim_match → Duels
- dim_match → Goalkeeping
- dim_match → Match Summary

This structure simplifies filtering, improves performance, and enables consistent cross-table analysis.

---

# 📈 Dashboard Pages

The Power BI dashboard is divided into six analytical sections:

## 1. Executive Dashboard

Provides an overview of Germany's tournament performance through KPIs, match results, and primary findings.

---

## 2. Attack Analysis

Analyzes Germany's attacking efficiency using:

- Goals vs xG
- Big Chances
- Big Chances Missed
- Shots on Target
- Final Third Entries
- Touches in Opposition Box

---

## 3. Midfield Analysis

Evaluates Germany's midfield performance through:

- Possession
- Accurate Passes
- Final Third Progression
- Through Balls
- Ground Duel Success
- Interceptions

---

## 4. Defensive Analysis

Examines defensive performance using:

- Tackles
- Interceptions
- Ground Duel Success
- Aerial Duel Success
- Clearances
- Defensive Errors

---

## 5. Goalkeeping Analysis

Measures goalkeeper contribution through:

- Saves
- Big Saves
- Goals Prevented

---

## 6. Root Cause Analysis

Ranks the factors contributing to Germany's elimination based on evidence gathered from all previous analyses.

---

# 🔍 Root Cause Analysis

## 🥇 1. Poor Finishing (Primary Root Cause)

Germany consistently created high-quality attacking opportunities but failed to convert them efficiently. A high number of missed big chances and the gap between Expected Goals (xG) and actual goals indicate that finishing was the primary reason for Germany's elimination.

---

## 🥈 2. Defensive Engagement (Major Contributing Factor)

Germany struggled to win crucial ground and aerial duels while opponents frequently disrupted attacks through interceptions and successful tackles. These defensive weaknesses allowed opponents to regain possession and capitalize on key moments.

---

## 🥉 3. Goalkeeping Performance (Secondary Contributing Factor)

Although routine saves were made, Germany lacked decisive goalkeeping performances during critical situations. The Goals Prevented metric suggests that the goalkeeper's shot-stopping contribution was below expectations.

---

## 4️⃣ Midfield Defensive Transition (Minor Contributing Factor)

Germany's midfield effectively controlled possession and progressed the ball into attacking areas. However, weaker defensive transitions allowed opponents to regain possession and create counterattacking opportunities.

---

# 💡 Key Findings

- Germany consistently generated high-quality scoring opportunities.
- Expected Goals (xG) exceeded actual goals scored.
- Opponents won several important aerial and ground duels.
- Defensive transitions were inconsistent during crucial moments.
- Goalkeeping lacked match-changing interventions.
- Poor finishing was identified as the primary cause of Germany's group-stage elimination.

---

# 📚 Skills Demonstrated

- Data Cleaning
- Data Modeling
- SQL Querying
- PostgreSQL
- Power BI
- DAX Measures
- Dashboard Design
- KPI Development
- Exploratory Data Analysis (EDA)
- Data Storytelling
- Root Cause Analysis
- Sports Analytics

---

# 🔮 Future Improvements

- Player-level performance analysis.
- Expected Threat (xT) analysis.
- Passing network visualization.
- Player heatmaps.
- Interactive match timeline.
- Comparison with previous FIFA World Cups.
- Predictive analytics using Machine Learning.

---

# 👨‍💻 Author

**Aron Varghese John**

If you found this project interesting or have suggestions for improvement, feel free to connect or provide feedback.

---
