# Soccer Performance Analysis

> An end-to-end performance analysis for a professional soccer club, turning raw match and player event data into decision-ready insights on team effectiveness, player value, and tactical efficiency.

This project analyzes match, player, and team performance data to uncover where games are being won, where points are being lost, and which levers the technical staff and front office can pull to improve results. It was built to simulate a real club analytics engagement, from data cleaning through to an interactive dashboard, with the goal of supporting recruitment, tactical, and performance decisions rather than just describing past matches.

## ⚽ Business Problem

Clubs generate huge volumes of match data, but without a consolidated view, decisions on tactics, recruitment, and squad investment often come down to the eye test instead of evidence.

**The core problem:** performance data exists, but it isn't organized to answer the questions that matter: which players create real value, where the team is underperforming its underlying numbers, and what is costing points.

**Why it matters:**
- Transfer and wage budgets get allocated inefficiently without a clear view of player contribution
- Tactical adjustments become reactive instead of pattern-driven
- Underperforming areas of the pitch or phases of play go unnoticed until they show up in the league table

**If ignored:** the club risks overpaying for low-impact players, missing undervalued talent, and repeating tactical weaknesses that a proper analysis would have surfaced weeks earlier.

**Key stakeholders:** Head Coach, Technical Director, Performance Analysts, Recruitment/Scouting, Sporting Director, and Finance, each needing a different cut of the same data.

## 🎯 Project Objective

This analysis converts raw event and match data into a structured framework for sporting decisions. Specifically, it aims to:

- Identify top-performing players by output and efficiency (per 90 minutes)
- Measure team performance against underlying metrics (xG, xGA, xPoints)
- Understand attacking and defensive patterns by phase of play
- Compare performance home vs. away and across match states
- Surface opportunities to improve results through tactical and personnel changes
- Highlight undervalued players and positions for recruitment

### Questions Answered

1. Which players generate the most goal contribution, and which are most efficient per 90?
2. Is the team over- or under-performing its expected goals, and is that sustainable?
3. Where on the pitch are chances being created and conceded?
4. How does performance change by match state (leading, drawing, trailing)?
5. How effective is the press, and where is possession being lost?
6. Which positions or profiles offer the best recruitment value?

## 📊 Dataset Overview

| Attribute | Description |
|---|---|
| **Source** | `<e.g. StatsBomb Open Data / FBref / Opta export / Kaggle>` |
| **Rows** | `<number>` |
| **Columns** | `<number>` |
| **Time Period** | `<e.g. 2023/24 season>` |
| **Competition(s)** | `<e.g. Premier League, La Liga>` |
| **Key Variables** | Player, Team, Match Date, Minutes Played, Goals, Assists, Shots, xG, xA, Passes, Pressures, Position |
| **Data Quality Notes** | `<e.g. duplicate events removed, player names standardized, minutes normalized to per 90>` |
| **Limitations** | `<e.g. no tracking data, single-season sample, no injury or fitness data>` |

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** | `<e.g. data cleaning, feature engineering, EDA, pitch visualizations (mplsoccer)>` |
| **SQL** | `<e.g. data extraction, joins, and aggregation by player/team/match>` |
| **Excel** | `<e.g. initial data audit and quick pivots>` |
| **Power BI / Tableau** | `<e.g. interactive dashboard and KPI reporting>` |

> Remove any tool rows not used in your version of this project.

## 🔄 Methodology

```
Raw Match & Event Data
        ↓
Data Cleaning
        ↓
Data Validation
        ↓
Exploratory Data Analysis
        ↓
Metric Development
        ↓
Dashboard Design
        ↓
Tactical & Recruitment Insights
        ↓
Recommendations
```

1. **Raw Data**: Match and event data loaded in its original form, preserving full granularity (passes, shots, duels, pressures).
2. **Data Cleaning**: Resolved missing values, duplicate events, inconsistent player and team naming, and mismatched minutes played.
3. **Data Validation**: Cross-checked totals against official match results and league tables (e.g. goals scored, points).
4. **Exploratory Data Analysis**: Explored patterns in shot quality, possession, pressing, and positional output to decide what deserved deeper analysis.
5. **Metric Development**: Built metrics a coach or sporting director would actually use, such as per-90 rates, xG difference, and progressive actions.
6. **Dashboard Design**: Translated findings into an interactive dashboard focused on clarity and decision-relevance.
7. **Insights**: Interpreted patterns through a tactical and sporting lens, linking each finding to an action.
8. **Recommendations**: Converted insights into specific next steps for coaching, analysis, and recruitment.

## 📈 Dashboard Preview

### Team Overview
High-level view of results, xG/xGA trends, and points vs. expected points.

![Team Overview](Images/team_overview.png)

### Player Performance
Per-90 output, efficiency, and percentile rankings by position.

![Player Performance](Images/player_performance.png)

### Attacking & Shot Analysis
Shot maps, xG per shot, and chance creation zones.

![Attacking Analysis](Images/attacking_analysis.png)

### Defensive & Pressing Analysis
Pressure regains, PPDA, and defensive actions by pitch zone.

![Defensive Analysis](Images/defensive_analysis.png)

## 📊 Key Metrics

| Metric | Description |
|---|---|
| **Goals / Assists per 90** | Output normalized for minutes played |
| **xG (Expected Goals)** | Quality of chances created, based on shot location and type |
| **xA (Expected Assists)** | Likelihood that a pass becomes a goal assist |
| **xG Difference (xGD)** | xG created minus xG conceded, a stronger indicator of team strength than results alone |
| **Shot Conversion Rate** | Goals as a percentage of shots, compared against xG to assess finishing |
| **Pass Completion % / Progressive Passes** | Ball security and forward progression |
| **PPDA** | Passes allowed per defensive action, a measure of pressing intensity |
| **Possession Won in Final Third** | Effectiveness of high pressing |
| **Points vs. xPoints** | Whether results are matching underlying performance |

## 🔍 Key Findings

> Replace the placeholders below with your actual results.

### 1. A small group of players drives a disproportionate share of team output
- **What happened:** `<e.g. 3 players account for X% of goal contributions>`
- **Why it matters:** Heavy reliance on a few players creates risk if they are injured or sold.
- **Potential impact:** Developing secondary creators reduces dependency and stabilizes performance.

### 2. The team is over/under-performing its expected goals
- **What happened:** `<e.g. scored X goals from Y xG>`
- **Why it matters:** Large gaps between goals and xG are often not sustainable, signalling possible regression or poor finishing.
- **Potential impact:** Adjusting expectations, and finishing or shot-selection work, can protect long-term results.

### 3. Chance creation and concession are concentrated in specific zones
- **What happened:** `<e.g. X% of chances conceded come from the left half-space>`
- **Why it matters:** This points to a repeatable tactical weakness rather than random variance.
- **Potential impact:** Targeted tactical adjustments can reduce high-quality chances against.

### 4. Performance changes significantly by match state
- **What happened:** `<e.g. xG drops by X% when leading>`
- **Why it matters:** Reveals game-management strengths or weaknesses that cost points late in matches.
- **Potential impact:** Improving in-game management could convert draws into wins.

### 5. Pressing effectiveness varies by phase and opponent
- **What happened:** `<e.g. PPDA is X in the first half vs. Y in the second>`
- **Why it matters:** Fading intensity points to fitness, rotation, or tactical-structure issues.
- **Potential impact:** Smarter rotation and pressing triggers can sustain intensity across 90 minutes.

### 6. Undervalued players identified for recruitment
- **What happened:** `<e.g. several players in lower-profile leagues rank in the top percentile for progressive actions per 90>`
- **Why it matters:** High-output, low-cost profiles offer strong value in the transfer market.
- **Potential impact:** Data-driven recruitment can improve squad quality without inflating spend.

## 💼 Sporting Impact

This analysis addresses the original problem: performance data existed, but staff lacked a consolidated, decision-ready view. With this framework in place, the club can:

- **Make recruitment decisions with evidence**, targeting undervalued profiles and avoiding overpays
- **Refine tactics** by pinpointing repeatable weaknesses and strengths by zone and phase
- **Manage workload and rotation** using intensity and output trends
- **Set realistic expectations** by separating performance from variance (goals vs. xG)
- **Improve player development** with per-90 benchmarks and percentile rankings
- **Support long-term planning** by giving coaching and finance a shared, data-backed view

> 📌 In short: this project turns historical match data into a forward-looking decision tool, moving the club from reactive reporting to proactive sporting strategy.

## 🚀 Recommendations

| Recommendation | Why It Matters |
|---|---|
| Reduce reliance on key players | Lowers risk from injuries or departures |
| Address the identified defensive weak zone | Cuts high-quality chances conceded |
| Improve finishing and shot selection | Closes the gap between xG and goals |
| Strengthen game management when leading | Protects points late in matches |
| Target undervalued positions and profiles in recruitment | Maximizes value per transfer dollar |
| Adjust pressing triggers and rotation | Sustains intensity through 90 minutes |
| Review KPIs after every matchday | Catches issues early rather than at mid-season |

## 🔮 Next Steps

- **Predictive models**: forecast match outcomes and expected points
- **Player similarity & scouting models**: find replacement profiles using clustering
- **Expected Threat (xT)**: quantify the value of ball progression
- **Possession-value models**: measure the impact of every action
- **Tracking data integration**: add off-ball movement and positioning analysis
- **Automated dashboard refreshes**: update after every matchday
- **Injury-risk and load modelling**: support rotation decisions
- **Opponent analysis reports**: automate pre-match scouting

## 📂 Project Structure

```
Soccer-Performance-Analysis/
│
├── Data/
├── SQL/
├── Notebooks/
├── Dashboard/
├── Images/
├── Documentation/
├── README.md
└── requirements.txt
```

## ▶️ How to Run

```bash
# Clone the repository
git clone https://github.com/<your-username>/Soccer-Performance-Analysis.git
cd Soccer-Performance-Analysis

# Install dependencies
pip install -r requirements.txt

# Launch the notebooks
jupyter notebook
```

## ⭐ Skills Demonstrated

`Sports Analytics` `Data Cleaning` `SQL` `Python` `Data Visualization` `Dashboard Design` `KPI Development` `Expected Goals (xG) Modelling` `Tactical Analysis` `Recruitment Analytics` `Storytelling with Data`

## 📚 Key Takeaways

This project reinforced that the value of analysis isn't the volume of data processed, but the quality of the decisions it enables. Every step, from cleaning event data to designing the dashboard, was guided by one question: *what would a coach or sporting director need to know to make a better call before the next match?*

Beyond the technical work in Python, SQL, and visualization, this project demonstrates the ability to translate ambiguous sporting questions into structured analysis, and to turn findings into recommendations that coaches and decision-makers can act on.

## 📬 Contact

**`<Your Name>`** · [LinkedIn](https://linkedin.com/in/<your-handle>) · [Email](mailto:<your-email>)
