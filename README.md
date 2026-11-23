# Heart Disease Prediction

**Live App:** [Open the app](https://heartdiseaseprediction-ftjj4pkvs727w5hxjndzzp.streamlit.app/)

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

## Bagging and Boosting Experiment
I also tried ensemble methods using 5-fold cross-validation:

| Model | Accuracy |
|---|---|
| Logistic Regression | 84.1% |
| AdaBoost | 82.8% |
| KNN | 82.6% |
| Random Forest | 82.6% |
| Gradient Boosting | 81.7% |
| Bagging | 80.4% |
| XGBoost | 79.2% |

Ensemble methods did not beat the simple models on this small dataset (918 rows); all scores fall within one standard deviation of each other, so I kept KNN in the app.

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
