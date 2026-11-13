# XGBoost Hotel Booking Classification

A machine learning project that uses XGBoost to predict hotel booking cancellations. This project demonstrates classification techniques using the hotel booking demand dataset.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Model Performance](#model-performance)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements an XGBoost classifier to predict whether a hotel booking will be canceled or not. The model uses various features such as lead time, arrival date, stay duration, guest information, and booking characteristics to make predictions.

## ✨ Features

- **Data Analysis**: Exploratory data analysis of hotel booking data
- **XGBoost Classification**: Implementation of gradient boosting for binary classification
- **Hyperparameter Tuning**: Randomized search for optimal model parameters
- **Model Evaluation**: Cross-validation and accuracy metrics
- **Feature Importance**: Visualization of important features
- **Decision Trees**: Visualization of XGBoost decision trees

## 🔧 Prerequisites

Before running this project, make sure you have the following installed:

- **Python 3.7+** (Python 3.8 or higher recommended)
- **pip** (Python package installer)
- **Jupyter Notebook** (for running the notebook)

## 📦 Installation

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd XGBoostClassification
```

### Step 2: Create a Virtual Environment (Recommended)

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

This will install the following packages:
- `pandas` - Data manipulation and analysis
- `xgboost` - Gradient boosting framework
- `numpy` - Numerical computing
- `scikit-learn` - Machine learning utilities
- `matplotlib` - Data visualization
- `jupyter` - Jupyter Notebook environment

## 🚀 Usage

### Running the Notebook

1. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

2. **Open the Notebook:**
   - Navigate to `XGBoostHotelBookings.ipynb` in the Jupyter interface
   - Click on the notebook to open it

3. **Run the Cells:**
   - Run cells sequentially using `Shift + Enter`
   - Or run all cells using `Cell > Run All` from the menu

### Expected Workflow

The notebook follows this workflow:

1. **Install XGBoost** (if not already installed)
2. **Import Libraries** - Load necessary Python packages
3. **Load Data** - Read the `hotel_bookings_clean.csv` file
4. **Data Exploration** - Analyze dataset structure and statistics
5. **Data Visualization** - Visualize target variable distribution
6. **Feature Correlation** - Analyze correlations with target variable
7. **Model Training** - Train XGBoost classifier with default parameters
8. **Baseline Evaluation** - Evaluate initial model performance
9. **Feature Importance** - Visualize important features
10. **Cross-Validation** - Perform cross-validation for model assessment
11. **Hyperparameter Tuning** - Optimize model parameters using RandomizedSearchCV
12. **Final Evaluation** - Evaluate optimized model

## 📁 Project Structure

```
XGBoostClassification/
│
├── XGBoostHotelBookings.ipynb    # Main Jupyter notebook
├── hotel_bookings_clean.csv      # Dataset file
├── requirements.txt               # Python dependencies
├── README.md                     # English documentation
└── README_FA.md                  # Persian documentation
```

## 📊 Dataset

The project uses the **Hotel Booking Demand Dataset** which contains:
- **119,210 rows** of booking data
- **53 columns** including features and target variable
- **Target Variable**: `is_canceled` (binary: 1 = canceled, 0 = not canceled)

### Dataset Features Include:
- Lead time
- Arrival date information (week number, day, month)
- Stay duration (weekend nights, week nights)
- Guest information (adults, children, babies)
- Booking characteristics (repeated guest, previous cancellations)
- Hotel type (City/Resort)
- Meal type
- Market segment
- And more...

**Dataset Source**: [Kaggle - Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)

## 📈 Model Performance

The model achieves the following performance:

- **Baseline Accuracy**: ~81.5%
- **Cross-Validation Accuracy**: ~81.5%
- **Optimized Model Accuracy**: ~83.5% (after hyperparameter tuning)

### Best Parameters Found:
- `max_depth`: 10
- `n_estimators`: 40
- `learning_rate`: ~0.17
- `subsample`: 0.5
- `alpha`: 0.001

## 🔍 Key Insights

- The dataset shows an imbalanced distribution of canceled vs. non-canceled bookings
- Lead time and other temporal features are highly correlated with cancellations
- XGBoost effectively captures non-linear relationships in the data
- Hyperparameter tuning significantly improves model performance

## 🤝 Contributing

Contributions are welcome! If you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Notes

- Make sure the `hotel_bookings_clean.csv` file is in the same directory as the notebook
- The notebook includes inline comments explaining each step
- Some cells may take a few minutes to execute, especially hyperparameter tuning

## 📄 License
MIT

## 🙏 Acknowledgments

- Dataset provided by [Kaggle](https://www.kaggle.com/)
- XGBoost library developers
- Scikit-learn community

---

**Note**: If you encounter any issues, please check that all dependencies are correctly installed and that the dataset file is in the correct location.

