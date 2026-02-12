# ⚡ EV Charging Infrastructure Optimization

### A Data-Driven Approach using XGBoost and MCDM

* **Interactive Enhanced EV Heat Map:** [Click here to view the Interactive Map](https://github.com/Sarvagya-Sharma/Decision-Support-Tool-for-EV-Infrastructure-Planning/blob/main/notebooks/Enhanced_EV_Map.html)

---

## 📖 Project Overview

The rapid adoption of Electric Vehicles (EVs) is hindered by "range anxiety" and the lack of accessible charging infrastructure. This project aims to solve the **Optimal Location Problem** for EV charging stations using a machine learning pipeline.

By integrating diverse geospatial datasets (traffic volume, population density, commercial/residential POIs, and road networks), we predict charging demand at a granular level and rank locations using a Multi-Criteria Decision Making (MCDM) system.

### 🔑 Key Features

* **Geospatial Feature Engineering:** Aggregated OpenStreetMap (OSM) data, demographic stats, and traffic sensor logs.
* **Predictive Modeling:** Trained an **XGBoost Regressor** to predict localized energy demand scores (R² ≈ 0.88).
* **Decision Support System:** Implemented an **MCDM Layer** to filter and rank the "Top 300" investment-ready sites.
* **Interactive Reporting:** Fully automated Quarto-based reporting with interactive geospatial visualizations.

---

## 📂 Project Organization

```
├── README.md          <- The top-level README for describing highlights for using this ML project.
│
├── notebooks          <- Jupyter notebooks. Naming convention: snake_case (e.g., final_last_model.ipynb).
│
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment.
│
├── src                <- Source code for use in this project.
│   ├── __init__.py    <- Makes src a Python module.
│   │
│   ├── data
│   │   ├── processed      <- The final, canonical data sets for modeling.
│   │   └── raw            <- The original, immutable data dump (OSM, Traffic, etc.).
│   │
│   ├── preprocessing_data           
│   │   └── pre-processing.py  <- Scripts to clean, merge, and impute missing data.
│   │
│   ├── feature_engineering       
│   │   └── build_features.py  <- Scripts to create density maps, centrality scores, and entropy indices.
│   │
│   ├── models         
│   │   ├── predict_model.py   <- Script to generate demand scores using the trained model.
│   │   └── train_model.py     <- Script to train XGBoost and save model artifacts.
│   │
│   ├── visualization  
│   │   └── visualize.py       <- Scripts to create static plots and interactive Folium maps.
│   │
│   └── main.py  <- Main orchestrator script to run the full pipeline.
│
├── LICENSE      <- MIT License terms.
```



## 📊 Results Summary

* **Best Model:** XGBoost Regressor
* **Accuracy:** RMSE: 42.1 | R²: 0.88
* **Top Predictors:** Traffic Volume, Commercial POI Density, Road Network Centrality.
* **Output:** A prioritized list of 300 optimal coordinates for charging stations, visualized in `reports/final_project_report`.

---


---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
