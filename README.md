# student_performance# Student Performance Prediction Using Machine Learning

## Project Overview
This project predicts student academic performance using Machine Learning techniques. The model analyzes different student-related factors such as study hours, previous scores, sleep hours, and practice papers to estimate the overall performance index.

The project uses a Multiple Linear Regression algorithm to build the prediction model and provides accurate performance predictions based on user input.

---

# Project Objective
The main objective of this project is to:
- Analyze factors affecting student performance
- Build a Machine Learning regression model
- Predict student performance using academic and lifestyle data
- Understand relationships between study habits and results

---



The dataset contains the following features:

| Feature Name | Description |
|---|---|
| Hours Studied | Number of study hours per day |
| Previous Scores | Scores obtained in previous exams |
| Extracurricular Activities | Participation in extracurricular activities (Yes/No) |
| Sleep Hours | Average sleeping hours per day |
| Sample Question Papers Practiced | Number of sample papers practiced |
| Performance Index | Overall student performance score (Target Variable) |

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle
- Flask

---

# Machine Learning Workflow

## 1. Data Collection
The dataset is loaded using Pandas.

```python
import pandas as pd

df = pd.read_csv("Student_Performance.csv")
```

---

## 2. Data Preprocessing

Data preprocessing includes:
- Handling categorical values
- Feature selection
- Splitting dataset into training and testing sets

### Encoding Categorical Data

The `Extracurricular Activities` column contains Yes/No values which are converted into numerical values.

| Original Value | Encoded Value |
|---|---|
| Yes | 1 |
| No | 0 |

```python
df["Extracurricular Activities"] = df["Extracurricular Activities"].map({
    "Yes":1,
    "No":0
})
```

---

## 3. Exploratory Data Analysis (EDA)

EDA is performed to understand:
- Feature relationships
- Correlations
- Data distribution

Libraries used:

```python
import matplotlib.pyplot as plt
import seaborn as sns
```

Visualization techniques:
- Heatmaps
- Histograms
- Scatter plots
- Correlation matrix

---

# Model Development

## Algorithm Used
### Multiple Linear Regression

Linear Regression is used to predict continuous numerical values.



# Model Evaluation

The model performance is evaluated using:

## Mean Squared Error (MSE)

```python
from sklearn.metrics import mean_squared_error

mse = mean_squared_error(y_test, y_pred)

print(mse)
```

## R-Squared Score

```python
from sklearn.metrics import r2_score

score = r2_score(y_test, y_pred)

print(score)
```

---

# Saving the Model

The trained model is saved using Pickle.

```python
import pickle

pickle.dump(model, open("student_model.pkl", "wb"))
```

---

# Loading the Saved Model

```python
model = pickle.load(open("student_model.pkl", "rb"))
```

---

# User Prediction Example

```python
hours_studied = 5
previous_scores = 75
extra_activities = 1
sleep_hours = 7
papers_practiced = 4

prediction = model.predict([[
    hours_studied,
    previous_scores,
    extra_activities,
    sleep_hours,
    papers_practiced
]])

print(prediction)
```

---

# Project Structure

```bash
Student-Performance-Prediction/
│
├── dataset/
│   └── Student_Performance.csv
│
├── models/
│   └── student_model.pkl
│
├── notebook/
│   └── student_performance.ipynb
│
├── templates/
│   └── index.html
│
├── app.py
├── requirements.txt
└── README.md
```

---

# Installation

## Clone Repository

```bash
git clone <repository-link>
```

## Install Required Libraries

```bash
pip install -r requirements.txt
```

---

# Requirements

```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
flask
pickle-mixin
```

---

# Run the Project

```bash
python app.py
```

---

# Future Enhancements

- Add advanced Machine Learning algorithms
- Improve frontend UI
- Deploy using cloud platforms
- Add real-time analytics dashboard
- Add student report generation

---

# Learning Outcomes

This project helps in understanding:
- Machine Learning workflow
- Data preprocessing
- Regression algorithms
- Model evaluation
- Data visualization
- Flask deployment

---

# Conclusion

This project demonstrates how Machine Learning can be used to predict student academic performance based on different educational and lifestyle factors.

The project provides practical experience in:
- Python programming
- Data analysis
- Machine Learning model building
- Model deployment

---

# Author

swarnalatha

**Swarna**

Machine Learning Enthusiast | Python Developer | Aspiring Data Analyst
