# Student Exam Score Prediction

## Project Overview
This project predicts students' exam scores based on various performance factors using regression techniques. The dataset is **Student Performance Factors** from Kaggle.  

The project covers:  
- Data cleaning and preprocessing  
- Exploratory Data Analysis (EDA)  
- Linear Regression (with and without outliers)  
- Polynomial Regression  
- Feature combination experiments  

---

## Dataset
The dataset includes features such as:  
`Hours_Studied`, `Attendance`, `Parental_Involvement`, `Access_to_Resources`, `Extracurricular_Activities`, `Sleep_Hours`, `Previous_Scores`, `Motivation_Level`, `Internet_Access`, `Tutoring_Sessions`, `Family_Income`, `Teacher_Quality`, `School_Type`, `Peer_Influence`, `Physical_Activity`, `Learning_Disabilities`, `Parental_Education_Level`, `Distance_from_Home`, `Gender`, `Exam_Score`

---

## Methodology

1. **Data Cleaning**
   - Checked for missing values and removed incomplete rows.
   - Identified numerical and categorical features.
   - Encoded categorical variables using LabelEncoder.
   - Removed outliers using the IQR method.

2. **Exploratory Data Analysis**
   - Visualized distributions for numerical and categorical features.

3. **Regression Models**
   - **Linear Regression**:
     - With outliers
     - Without outliers
   - **Polynomial Regression** (degree=2)

4. **Feature Experiments**
   - Only `Hours_Studied`
   - `Hours_Studied + Sleep_Hours + Attendance`

5. **Evaluation Metrics**
   - Mean Squared Error (MSE)  
   - R² score  

---

## Results

| Model                               | MSE    | R²     |
|------------------------------------|--------|--------|
| Linear Regression (with outliers)  | 5.08   | 0.668 |
| Linear Regression (without outliers) | 1.26 | 0.875 |
| Polynomial Regression (degree=2)   | 4.30   | 0.719 |

**Insights:**  
- Removing outliers significantly improved model performance.  
- Linear regression on cleaned data provided the best predictions.  
- Polynomial regression did not improve performance for this dataset.  

---

## Visualizations
- Feature distributions and counts  
- Residuals plots  
- Actual vs Predicted exam scores  
- Feature coefficients  

---

## Tools & Libraries
- Python 3.x  
- Pandas  
- NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  

---

## Conclusion
Proper data cleaning and feature selection are key to building accurate predictive models. In this dataset, **linear regression on cleaned data** gave the most reliable predictions of student exam scores.
