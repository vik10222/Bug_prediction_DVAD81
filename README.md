# Bug Prediction Assignment

This repository contains the code and notebooks for a machine learning pipeline to predict software bugs. The workflow includes data cleaning, feature selection, hyperparameter optimization with Optuna, and ensemble model construction.

## Project Structure

```
.
├── data/
│   ├── raw/                # Raw input data files (place your dataset here)
│   └── processed/          # Cleaned and preprocessed data
├── notebooks/
│   ├── dataCleaning.ipynb  # Data cleaning, exploration, and initial model evaluation
│   ├── threshold_inv.ipynb # Feature importance threshold testing
│   ├── Catboost.ipynb      # Optuna optimization for CatBoostClassifier
│   ├── rf.ipynb            # Optuna optimization for RandomForestClassifier
│   ├── ExtraTree.ipynb     # Optuna optimization for ExtraTreesClassifier
│   ├── SVM.ipynb           # Optuna optimization for SVM
│   ├── svc_onerest.ipynb   # One-vs-Rest SVM optimization
│   └── ensemble.ipynb      # Ensemble model construction and evaluation
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/bug-prediction.git
   cd bug-prediction
   ```

2. **Create a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Prepare data**\
   Place your raw dataset (e.g., `bugs.csv`) in `data/raw/`.

2. **Data cleaning & initial evaluation**\
   Run `notebooks/dataCleaning.ipynb` to explore and preprocess the data and perform initial baseline model evaluations.

3. **Feature importance thresholding**\
   Run `notebooks/threshold_inv.ipynb` to identify and filter features based on importance thresholds.

4. **Hyperparameter optimization**\
   For each model, run the corresponding notebook under `notebooks/`:

   - `Catboost.ipynb`
   - `rf.ipynb`
   - `ExtraTree.ipynb`
   - `SVM.ipynb`
   - `svc_onerest.ipynb`

   These notebooks leverage Optuna to find the best hyperparameters.

5. **Ensemble model**\
   Run `notebooks/ensemble.ipynb` to combine individual models into an ensemble and evaluate overall performance.

## Results

- Key performance metrics and plots can be found within the respective notebooks under the `results/` section (output cells).
- Final ensemble metrics are summarized in `ensemble.ipynb`.

## Contributing

Contributions are welcome! Please open issues or pull requests for improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

