# Fuel Price Asymmetry in France

**Repository for the Master's thesis**: *"Existe-t-il des asymétries dans les ajustements des prix à la pompe ?"*  
**Author**: Gaël Pefourque  
**Academic Year**: 2023–2024  
**Institution**: Université Paris-Est Créteil (Master 1 Économie appliquée, parcours MASERATI)

---

## 🔍 Overview

This project investigates whether there are **asymmetries in the adjustments of retail fuel prices** in France in response to changes in the price of crude oil (Brent). The study focuses on the year 2022, leveraging high-frequency data at the gas station level.

It uses econometric modeling, specifically **Error Correction Models (ECM)** and **cointegration analysis**, to detect and quantify such asymmetries.

---

## 📊 Main Findings

- Evidence of asymmetric price adjustments: fuel prices **increase faster than they decrease** following changes in crude oil prices.
- Competitive intensity (proxied by number of nearby stations) significantly affects price behavior.
- Margins are higher and price adjustments more frequent on highways.

---

## 📈 Data

- **Fuel prices**: Daily prices for diesel, SP95, SP95-E10, and SP98 from French gas stations (source: [prix-carburants.gouv.fr](https://www.prix-carburants.gouv.fr)).
- **Brent price**: Daily Brent spot price from U.S. Energy Information Administration.
- **Exchange rate**: USD/EUR from Boursorama.

The dataset includes:
- Over **9 million price observations**.
- Station-level details: location, fuel type, station type (highway vs road), etc.

---

## ⚖️ Methodology

1. **Data Cleaning and Processing**:
   - Conversion of Brent prices into EUR/litre.
   - Calculation of HT (tax-excluded) fuel prices.
   - Computation of competition index (stations within 5km).

2. **Econometric Modeling**:
   - Step 1: Estimate long-term relationship (cointegration) between Brent and fuel prices.
   - Step 2: Apply ECM with asymmetry using Engle-Granger two-step procedure.
   - Step 3: Use Wald test to detect significance of asymmetry.

---

## ⚙️ Requirements

- Python 3.9+
- Pandas, Numpy
- Statsmodels
- Matplotlib / Seaborn
- Scikit-learn

---

## 🔢 Repository Structure

```
├── preprocessing/         # Jupyter notebooks with preprocessing
├── eda/                   # Jupyter notebooks with exploratory analysis
├── model/                 # Source code for modeling and processing
├── figures/               # Graphs and plots for the thesis
├── thesis.pdf             # Full PDF of the final thesis (French)
└── README.md
```

---

## 💡 Motivation

Understanding how fuel prices respond to oil price shocks is essential for:
- Public policy (e.g., windfall taxes, price controls)
- Consumer welfare
- Debates around market power and transparency

---

## ✍️ Citation

If you use this work in your research or publication, please cite it as:

> Pefourque, G. (2024). *Existe-t-il des asymétries dans les ajustements des prix à la pompe ?* Université Paris-Est Créteil.

---

## 🙌 Acknowledgements

Thanks to **Ferhat Mihoubi** for supervising this research.
