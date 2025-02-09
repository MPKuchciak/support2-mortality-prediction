project/
│
├── data/
│   ├── raw/               # Raw dataset files (original, untouched)
│   ├── processed/         # Processed dataset files (after cleaning/EDA)
│   ├── models/            # Saved model files (e.g., .pkl or .h5)
│   ├── outputs/           # Output files (e.g., predictions, evaluation metrics)
│   └── visualizations/    # Plots and charts (e.g., confusion matrix, PR curves)
│
├── notebooks/
│   ├── 01_EDA.ipynb       # Exploratory Data Analysis (EDA)
│   ├── 02_Preprocessing.ipynb  # Data cleaning and feature engineering
│   ├── 03_Baseline_Model.ipynb # Baseline model (e.g., Logistic Regression, Decision Tree)
│   ├── 04_Advanced_Models.ipynb # Advanced models (e.g., Random Forest, Boosting, NN)
│   ├── 05_Evaluation.ipynb # Model evaluation and comparison
│   └── 06_Final_Model.ipynb # Final model training and saving
│
├── requirements.txt       # List of Python dependencies (e.g., pandas, scikit-learn)
├── README.md              # Overview of the project
└── config.py              # Optional: Centralized configuration (paths, parameters)
