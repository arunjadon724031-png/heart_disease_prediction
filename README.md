# heart_disease_prediction

# Heart Disease Prediction

A machine learning web app that predicts whether a patient is at **high or low risk of heart disease** from basic health details.

## Features
- Takes 11 inputs: age, sex, chest pain type, resting blood pressure, cholesterol, resting ECG, fasting blood sugar, max heart rate, exercise-induced angina, oldpeak (ST depression) and ST slope
- Shows a High Risk or Low Risk result with one click
- Built with an interactive Streamlit interface

## Model
I trained and compared 5 classification models on `heart.csv`:

| Model | Accuracy | F1 Score |
|---|---|---|
| Logistic Regression | 86.96% | 0.8857 |
| KNN | 86.41% | 0.8815 |
| Naive Bayes | 85.33% | 0.8683 |
| SVM | 84.78% | 0.8679 |
| Decision Tree | 75.54% | 0.7783 |

The app uses the **KNN** model. Categorical features are one-hot encoded and numeric features are scaled before prediction.

## Tech Stack
Python, Pandas, Scikit-Learn, Joblib, Streamlit

## Project Files
- `Secondmlmodel.ipynb`: data preparation, training and model comparison
- `app.py`: Streamlit web app
- `KNN_heart.pkl`, `scale.pkl`, `columns.pkl`: saved model, scaler and column order
- `heart.csv`: dataset

## How to Run
```bash
pip install streamlit pandas scikit-learn joblib
streamlit run app.py
```

## Disclaimer
This project is for learning purposes only and is not a substitute for medical advice.
