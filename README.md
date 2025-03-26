# Volunteer Retention Prediction

## Project Goal  
The goal of this project was to develop a predictive model that would help the foundation anticipate whether volunteers would continue participating in its program for the next edition. This insight aims to enable proactive strategies to improve volunteer retention.  

Due to the pilot nature of the project, the analysis focused on basic predictive models. Further research could incorporate more advanced techniques and additional data sources.  
As per the client’s requirements, variable names have been retained in their original language and in the abbreviated form provided by the client.

---

## Data  
The dataset was sourced from the foundation’s educational program management platform and included information about volunteers and the schools where they conducted classes. Key variables:  
- **Volunteer information:**  
  - Gender  
  - Year of study  
  - Level of study (e.g., Bachelor's, Master's)  
  - Field of study  
  - University name and city  

- **Program participation:**  
  - Participation in the program edition  
  - Participation in the program round (each edition consists of two or three rounds)  
  - Volunteer thematic track (the foundation’s program includes several thematic tracks)  

- **School information:**  
  - School name  
  - City where the school is located  

---

## Data Preparation  
The following steps were performed to clean and preprocess the data:  
- **Loading and preprocessing:**  
  - Merging datasets (based on the `student_id` column)  
  - Renaming variables or values (e.g., converting "XVIII" to "1")  
  - Data cleaning (removing duplicates and outliers)  

- **Handling missing values:**  
  - Missing values were flagged instead of imputed, due to the nature of the data.  

- **Encoding categorical variables:**  
  - Applied frequency encoding and one-hot encoding based on variable characteristics.  

- **Splitting the dataset:**  
  - The dataset was divided into training and test sets for modeling.  

---

## Exploratory Data Analysis (EDA)  
EDA was conducted to understand data structure, identify variable relationships, and detect potential anomalies. Techniques included:  
- **Visualizations:** Bar charts, correlation matrices, etc.  
- **Statistical tests:** Chi-square test, Spearman correlation, and Kruskal-Wallis test, selected according to variable scale and relationship specifics.  

---

## Modeling  
Several machine learning models were trained and evaluated:  
- **Logistic Regression:** Used as a baseline model to explore basic relationships between variables.  
- **Random Forest:** Selected for its robustness against overfitting and ability to capture complex dependencies.  
- **XGBoost and LightGBM:** High-performance models known for their accuracy in classification tasks.  

### Model Evaluation  
The models were assessed using the following metrics:  
- **Accuracy**  
- **Sensitivity (Recall)**  
- **Specificity**  
- **ROC Curve**  

The best-performing models were **XGBoost** and **LightGBM**, which achieved high classification accuracy (approximately [percentage]% of cases).  

---

## Feature Importance Analysis  
Feature importance analysis was conducted to determine which variables had the greatest impact on predictions. Key insights were derived based on these findings.

---

## Conclusions  
This project provided the foundation with a preliminary predictive model to better understand volunteer behavior.  
The results indicate that certain demographic variables (e.g., field of study, university location) had the greatest impact on whether a volunteer would continue in the program.  

Future work could include integrating additional data sources and testing more advanced modeling techniques to improve predictive accuracy.  

---

## Technology Stack  
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, XGBoost, LightGBM  
- **Environment:** Google Colab  

---

## Code and Notebook  
The full code and notebook are available on Google Colab. You can access it [here](https://colab.research.google.com/drive/1jSJ0JrOS7ep-LryF1lG87IZGSEvItKFc?usp=sharing).  
