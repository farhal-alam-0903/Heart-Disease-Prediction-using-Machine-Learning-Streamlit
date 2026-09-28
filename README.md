# Heart Disease Prediction using Machine Learning & Streamlit

A machine learning project that predicts the likelihood of heart disease based on clinical and physiological features. The project includes exploratory data analysis, data preprocessing, feature encoding, feature scaling, model comparison, and a Streamlit web application for making predictions.

> **Note:** This project is for educational and demonstration purposes only. It is not a medical diagnosis or a substitute for professional medical advice.

## Project Overview

The dataset contains **918 patient records** with information such as:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Fasting Blood Sugar
* Resting ECG
* Maximum Heart Rate
* Exercise-Induced Angina
* Oldpeak
* ST Slope
* Heart Disease

The target variable is `HeartDisease`.

## Machine Learning Workflow

The project follows these steps:

1. Load the heart disease dataset
2. Perform exploratory data analysis (EDA)
3. Check dataset shape and information
4. Check duplicate and missing values
5. Encode categorical features using one-hot encoding
6. Split the data into training and testing sets
7. Apply `StandardScaler`
8. Train multiple classification models
9. Compare model performance using Accuracy and F1 Score
10. Save the KNN model, scaler, and expected feature columns
11. Build a Streamlit application for interactive predictions

## Models Tested

The following classification algorithms were evaluated:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Naive Bayes
* Decision Tree
* Support Vector Machine (SVM)

The trained KNN model is saved as:

```text
KNN_heart.pkl
```

The preprocessing objects are saved as:

```text
scaler.pkl
columns.pkl
```

## Model Evaluation

The notebook evaluates the models using:

* Accuracy Score
* F1 Score

The recorded test-set results are:

| Model               | Accuracy | F1 Score |
| ------------------- | -------: | -------: |
| Logistic Regression |   0.8859 |   0.9005 |
| KNN                 |   0.8859 |   0.8995 |
| Naive Bayes         |   0.9130 |   0.9208 |
| Decision Tree       |   0.7609 |   0.7905 |
| SVM (RBF Kernel)    |   0.8967 |   0.9100 |

These results are from the train/test split used in the notebook (`test_size=0.2`, `random_state=42`).

## Streamlit Application

The Streamlit application provides an interactive interface where users can enter:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Fasting Blood Sugar
* Resting ECG
* Maximum Heart Rate
* Exercise-Induced Angina
* Oldpeak
* ST Slope

The application processes the input using the saved feature columns and scaler before passing it to the trained KNN model.

## Installation

Clone the repository:

```bash
git clone https://github.com/farhal-alam-0903/Heart-Disease-Prediction-using-Machine-Learning-Streamlit.git
cd heart-disease-prediction
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Run the Application

Run the Streamlit application with:

```bash
streamlit run app.py
```

The application will open in your browser.

## Project Structure

```text
heart-disease-prediction/
│
├── app.py
├── heart.csv
│
├── KNN_heart.pkl
├── scaler.pkl
├── columns.pkl
│
├── HeartdiseaseFinal.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Streamlit
* Jupyter Notebook

## Future Improvements

* Add probability/confidence visualization
* Improve UI design
* Add model selection
* Perform hyperparameter tuning for KNN
* Add confusion matrix and ROC-AUC analysis
* Deploy the Streamlit application online

## Disclaimer

This application is an educational machine learning project and should not be used for medical diagnosis, treatment, or clinical decision-making.
