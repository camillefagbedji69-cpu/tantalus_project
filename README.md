# Primate-Detection-RF: Modeling Aethiops tantalus Detectability

## 📌 Context & Overview
Monitoring forest primates like *Aethiops tantalus* relies heavily on camera-trap data. However, detection rates are not random; they are influenced by habitat structure, resource availability, and environmental factors. This project uses **Random Forest** modeling to identify the ecological drivers of primate detectability, providing essential insights for inventory planning and wildlife management.

## 🎯 Objectives
* **Variable Identification:** Determining which environmental and structural factors most influence detection rates.
* **Model Comparison:** Evaluating whether vegetation type or tree strata diversity provides better predictive power.
* **Predictive Framework:** Building a robust model to estimate detectability based on soil, water, and forest structure.

## 🛠️ Tech Stack & Methodology
* **Language:** R 📊
* **ML Algorithm:** Random Forest (with 10-fold Cross-Validation).
* **Preprocessing:** Collinearity check via **VIF (Variance Inflation Factor)**.
* **Evaluation Metrics:** RMSE, MAE, and $R^2$.
* **Key Variables:** Soil type, Specific richness, Tree height, Distance to water, and Vegetation strata diversity.



## 🚀 Key Results
* **Dominant Drivers:** The **Soil type** emerged as the most critical factor (100% relative importance), followed by **Specific Richness** (55-69%) and **Tree Height**.
* **Ecological Insights:** * Soil and flora richness are better predictors than broad vegetation classifications.
    * The diversity of the middle tree strata and the general vegetation type contributed surprisingly little to the model's accuracy.
* **Model Diagnostics:** While the model achieved high $R^2$ values, the analysis identified potential overfitting due to sample size, highlighting the need for cautious interpretation and further validation.
* **Trade-offs:** Replacing vegetation type with tree diversity slightly increased error rates (RMSE/MAE), suggesting that habitat "characterization" captures a specific synergy that individual diversity indices miss.

## 🔮 Perspectives for Improvement
* **Interaction Effects:** Exploring the synergy between Soil × Specific Richness to understand complex habitat preferences.
* **Vertical Structure:** Integrating 3D forest metrics (e.g., LiDAR-derived canopy density) to model primate movement patterns more accurately.
* **Seasonal Dynamics:** Extending the model to time-series data to account for seasonal shifts in detectability and resource availability.
* **Data Fusion:** Integrating NDVI and forest cover indices from satellite imagery to refine local-scale predictions.
