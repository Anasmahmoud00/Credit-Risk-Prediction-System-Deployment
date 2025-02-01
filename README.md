

# Credit Risk Prediction System

## Overview
This project implements a machine learning system for predicting credit risk using historical loan data. The system uses various borrower characteristics and loan attributes to predict the likelihood of loan default, helping financial institutions make informed lending decisions.

## Data set
Link: https://www.kaggle.com/code/mahmoudalisalem/credit-risk-prediction/input?scriptVersionId=200583575
## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Performance](#model-performance)
- [Usage](#usage)
- [Contributing](#contributing)

## Features
- Data preprocessing and cleaning of loan application data
- Feature engineering and selection
- Principal Component Analysis (PCA) for dimensionality reduction
- Implementation of multiple machine learning models:
  - Random Forest Classifier
  - XGBoost Classifier
- Model performance evaluation with metrics:
  - Accuracy
  - F1 Score
  - Confusion Matrix
- Visualization of results and model performance

## Technologies Used
- Python 3.x
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - xgboost
  - matplotlib
  - seaborn
  - plotly

## Project Structure
```
├── data/
│   └── loan/
│       └── loan.csv
├── notebooks/
│   └── credit-risk-prediction.ipynb
├── src/
│   ├── preprocessing/
│   ├── models/
│   └── visualization/
└── README.md
```

## Installation
1. Clone the repository:
```bash
git clone https://github.com/Anasmahmoud00/Credit-Risk-Prediction-System-Deployment.git
cd Credit-Risk-Prediction-System-Deployment
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Data Preprocessing
The system performs several preprocessing steps:
1. Handling missing values
   - Removes columns with >20% missing values
   - Uses IterativeImputer for remaining missing values

2. Feature engineering
   - Encoding categorical variables
   - Custom encoding for sub-grades
   - One-hot encoding for categorical features

3. Data scaling
   - MinMax scaling of numerical features

4. Dimensionality reduction
   - PCA to reduce features to 25 components

## Model Performance

### XGBoost Classifier
Training Results:
- Accuracy: 97.21%
- F1 Score: 97.21%

Testing Results:
- Accuracy: 96.85%
- F1 Score: 96.85%

### Random Forest Classifier
Comparable performance to XGBoost with:
- High precision and recall scores
- Good generalization on test data
- Strong performance across different loan categories

## Usage
1. Prepare your data in the same format as the sample loan dataset

2. Run the preprocessing pipeline:
```python
python src/preprocessing/preprocess.py --input data/loan.csv
```

3. Train the model:
```python
python src/models/train.py --input data/processed/loan_processed.csv
```

4. Make predictions:
```python
python src/models/predict.py --input data/new_applications.csv
```

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



## Acknowledgments
- Dataset provided by LendingClub
- Special thanks to all contributors and maintainers
