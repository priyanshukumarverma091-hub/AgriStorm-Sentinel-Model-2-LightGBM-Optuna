# AgriStorm Sentinel

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&pause=1000&color=2EBD85&center=true&vCenter=true&width=750&lines=AgriStorm+Sentinel;AI-Powered+Agricultural+Intelligence;Crop+Yield+Vulnerability+Prediction;LightGBM+%2B+Optuna+Optimization" alt="Typing SVG" />

### AI-Powered Crop Yield Vulnerability Prediction for Rajasthan, India

Predicting historical crop yield changes using machine learning, temporal validation and hyperparameter optimization.

<br/>

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-Regression-2E8B57?style=for-the-badge)
![Optuna](https://img.shields.io/badge/Optuna-Optimization-4169E1?style=for-the-badge)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Research%20Model-success?style=for-the-badge)

</div>

---

## About The Project

**AgriStorm Sentinel** is a machine learning project focused on agricultural yield vulnerability prediction in Rajasthan, India.

Model 2.4 uses LightGBM regression combined with Optuna hyperparameter optimization to predict historical crop yield changes from agricultural and environmental features.

The system uses temporal validation to evaluate model performance on unseen historical years.

## Model 2.4 – Key Features

- LightGBM regression model
- Optuna hyperparameter optimization
- 40 optimization trials
- Expanding-window temporal validation
- Numerical and categorical preprocessing
- Independent temporal testing
- Crop-wise performance evaluation
- Feature importance analysis
- Model serialization and verification
- Baseline performance comparison

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming |
| LightGBM | Gradient boosting regression |
| Optuna | Hyperparameter optimization |
| Scikit-learn | Preprocessing and evaluation |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| SciPy | Sparse matrix utilities |
| Joblib | Model serialization |

## Model Workflow

```mermaid
flowchart TD
    A["Agricultural Dataset"] --> B["Rajasthan Data Filtering"]
    B --> C["Feature Engineering"]
    C --> D["Data Preprocessing"]
    D --> E["Temporal Validation"]
    E --> F["Optuna Optimization"]
    F --> G["LightGBM Training"]
    G --> H["Independent Testing"]
    H --> I["Performance Evaluation"]
    I --> J["Model Export"]
    
    style A fill:#14532d,color:#fff
    style F fill:#166534,color:#fff
    style G fill:#166534,color:#fff
    style J fill:#14532d,color:#fff
```

## Temporal Validation Strategy

The model follows a chronological training and testing approach.

| Stage | Crop Years |
|---|---|
| Training | Up to 2007 |
| Temporal validation | 2005, 2006, 2007 |
| Independent testing | 2008–2010 |
| Optuna trials | 40 |

This approach helps evaluate the model on historical years that are not included in its final training dataset.

## Model Evaluation

The model calculates the following metrics:

| Metric | Description |
|---|---|
| MAE | Mean Absolute Error |
| RMSE | Root Mean Squared Error |
| R² | Coefficient of Determination |
| Baseline MAE | Median-based baseline error |
| MAE Improvement | Improvement over baseline |

Actual metric values are generated when the model is executed.

## Generated Outputs

```text
AgriStorm_Model_2_V2_4/
│
├── model/
│   └── crop_vulnerability_lgbm.pkl
│
├── evaluation/
│   ├── predictions.csv
│   ├── crop_wise_performance.csv
│   └── feature_importance.csv
│
└── reports/
    └── model_report.json
```

## Dataset Requirements

The model expects a previously prepared Pandas DataFrame named `df` and a feature list named `FEATURES`.

Required columns:

- `yield_change_pct` – Prediction target
- `crop_year` – Historical crop year
- `state` – State filtering
- `district_key`
- `dominant_crop`
- `season`

The dataset must contain the required feature columns used by the preprocessing pipeline.

## Important Limitations

- Predicts historical yield change, not directly observed crop damage.
- Evaluation is restricted to Rajasthan and the available historical period.
- Independent validation is required before real-world deployment.

## Project Information

| Detail | Information |
|---|---|
| Project | AgriStorm Sentinel |
| Model Version | 2.4 |
| Algorithm | LightGBM + Optuna |
| Region | Rajasthan, India |
| Task | Regression |
| Validation | Temporal Validation |

## Author

**Priyanshu Kumar Verma**

---

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1500&color=2EBD85&center=true&vCenter=true&width=600&lines=Building+Intelligence+for+Agriculture;Data+Driven.+Research+Focused.;AgriStorm+Sentinel" alt="Footer Animation" />

**AgriStorm Sentinel | Model 2.4**

*Machine Learning for Agricultural Intelligence*

</div>
