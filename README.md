# Energy ML Prototypes

## Overview
This repository contains a collection of machine learning and optimization prototypes applied to renewable and building energy systems. Each subfolder is an independent case study exploring a different energy engineering problem using data-driven and search-based methods.

## Research / Engineering Motivation
Data-driven modeling and optimization are increasingly used alongside physics-based simulation in energy systems engineering — for prediction (e.g., forecasting energy extraction or consumption) and for decision-making under multiple constraints (e.g., allocating energy production across sources). This repository explores both directions across four case studies: geothermal energy extraction, building energy consumption, hydrogen production, and hybrid energy system allocation.

## Methods
- Regression and gradient-boosted models (Gradient Boosting, XGBoost, LightGBM) and a deep neural network for geothermal energy extraction prediction
- Artificial Neural Network (ANN) for building energy consumption prediction
- Genetic Algorithm (GA) for hydrogen production parameter optimization and hybrid energy system allocation
- Random Forest regression and linear programming for a Flask-based smart energy optimizer prototype
- Financial evaluation methods (NPV, ROI, IRR) applied to the geothermal case study

## Features
- Four independent, self-contained case studies, each with its own README
- Model evaluation using standard metrics (MSE, R²)
- A working Flask API + dashboard prototype (Smart Energy Optimizer)

## Results / Outputs
Each subfolder documents its own results in its local README, including reported MSE/R² values and, where applicable, optimization convergence behavior. Two subfolders include static result figures (`.jpeg`).

## Repository Structure
```
.
├── Geothermal-Analysis/                              # ML-based geothermal energy extraction prediction + economic analysis (NPV/ROI/IRR)
├── Optimization/
│   ├── Building/                                      # ANN-based building energy consumption prediction
│   └── Hydrogen/
│       ├── HES/                                       # Genetic algorithm optimization of a hybrid energy system
│       ├── Hydrogen-Production-Optimization-Biomass-GA/  # Genetic algorithm optimization of hydrogen yield from biomass
│       └── Smart Energy Optimizer/                    # Flask API + dashboard: energy prediction (Random Forest) + allocation (linear programming)
└── README.md
```

## How to Run
Each case study is self-contained. General setup:

```bash
pip install numpy pandas scikit-learn xgboost lightgbm tensorflow matplotlib scipy flask
```

For the Smart Energy Optimizer specifically, a scoped `requirements.txt` is provided:
```bash
cd "Optimization/Smart Energy Optimizer"
pip install -r requirements.txt
python app/app.py
```

For the other case studies, run the relevant `.py` script directly (e.g., `python Geothermal-Analysis/Geothermal_Analysis.py`).

## Technologies Used
Python, scikit-learn, XGBoost, LightGBM, TensorFlow/Keras, SciPy, Flask, pandas, NumPy, Matplotlib

## Limitations
- **All datasets in this repository are synthetically generated** (e.g., via `numpy.random` with fixed seeds), not measured or field data. Results demonstrate methodology, not validated real-world performance.
- These are prototypes built to explore modeling and optimization approaches, not production systems or peer-reviewed research outputs.
- The building energy ANN case study reports a modest R² (~0.33), which is reported honestly in its own README rather than omitted.
- No formal hyperparameter tuning or cross-validation was performed beyond what is documented per case study.

## Future Improvements
- Replace synthetic datasets with real measured or open energy datasets where available
- Add cross-validation and hyperparameter tuning
- Extend toward surrogate modeling for more computationally expensive simulations (e.g., CFD- or physics-based energy models)
- Consolidate the four case studies behind a shared data/evaluation utility module

## Author
Sina Mohammadi
Mechanical Engineering / Energy Systems / AI for Engineering
