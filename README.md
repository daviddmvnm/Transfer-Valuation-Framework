# FIFA Player Valuation & Development Framework ⚽

A data-driven framework for identifying undervalued football players and quantifying the financial returns of targeted skill development. Originally developed as a technical case study presented to senior data scientists and data science managers in a stakeholder simulation exercise for a major payments company. (I did pass the technical but sold the bag on the final round </3)

## Key Findings

- **The Offensive Premium**: Elite offensive players are valued at 2.6× their defensive counterparts. The market systematically rewards dribbling, passing, and shooting over defensive ability — even within the same leagues, clubs, and positions.
- **Development ROI**: Offensive skill development adds €550K–€880K in value across all positions. Even defenders gain ~1.9× more from offensive development than defensive improvement.
- **Position-Specific Pathways**: Each position has a unique combination of skills that unlocks the offensive premium — there is no one-size-fits-all development strategy.

## Scouting Model

The framework includes a player identification model that:

1. Finds players closest to the next elite skill tier, targeting those needing the smallest improvements to progress
2. Applies position-specific skill weightings for defenders, midfielders, and attackers
3. Ranks candidates by development feasibility, combining age and effort required

**Validation**: Case studies using 2021–2022 data identified players (e.g. Mitchell, Livramento, Guehi) who subsequently achieved 2–2.5× value appreciation on the transfer market.

## Project Structure

```
├── Analysis/
│   ├── EDA.ipynb              # Exploratory data analysis & visualisation
│   └── processing.ipynb       # Data cleaning & feature engineering
├── data/
│   ├── df_players.csv         # Full player dataset
│   ├── gk_players.csv         # Goalkeeper subset
│   ├── outfield_players.csv   # Outfield player subset
│   └── outfield_star_players.csv  # Elite player subset
├── slides_nologo.pptx         # Stakeholder presentation deck
└── requirements.txt
```

## Methods

- **Clustering** (K-Means) to identify distinct elite player archetypes
- **Regression analysis** to quantify marginal returns of skill development by position
- **Threshold-based scouting** to identify players near valuation breakpoints

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Tech Stack

Python · pandas · scikit-learn · matplotlib · seaborn · Jupyter
