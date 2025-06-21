# Predictive Model for Maternal Health Risk

### An End-to-End Machine Learning Project

This project develops a machine learning model to predict the maternal risk level (Low, Medium, or High) during pregnancy based on patient vital signs. The entire project, from data exploration to a final interactive web prototype, is documented here.

---

## 🚀 Project Overview

The primary goal of this project is to build a reliable classifier that can assist healthcare professionals in identifying at-risk patients early. By leveraging patient data such as age, blood pressure, blood sugar, and heart rate, the model provides a risk assessment, enabling timely intervention and potentially improving maternal outcomes.

This repository demonstrates a complete machine learning workflow, including data analysis, model comparison, and the deployment of a functional prototype.

## ✨ Key Features

* **Detailed Exploratory Data Analysis (EDA):** In-depth analysis of the dataset to uncover patterns, correlations, and key insights.
* **Comparative Model Analysis:** A baseline Logistic Regression model was built and evaluated, revealing weaknesses that were subsequently addressed.
* **High-Performance Final Model:** A Random Forest Classifier was trained, achieving **81% accuracy** and significantly improving performance on all risk classes.
* **Model Interpretability:** Feature importance analysis was conducted to understand the key drivers behind the model's predictions. **Blood Sugar (BS)** and **Systolic Blood Pressure** were identified as the most influential factors.
* **Interactive Web Prototype:** An HTML/JavaScript interface (`index.html`) that allows users to input patient data and receive a live risk prediction.

## 🛠️ Tech Stack

* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, etc
* **Frontend:** HTML, Tailwind CSS, JavaScript
* **Environment:** Jupyter Notebook

---

## 📁 File Structure

This repository contains the three core components of the project:

1.  **`Maternal-Health-Risk-Data-Set.csv`**: The raw dataset used for training and evaluating the models. It contains anonymized patient data with 6 features and 1 target variable.
2.  **`Maternal-Risk-ML.ipynb`**: The main Jupyter Notebook that documents the entire data science process, from loading the data to the final model evaluation.
3.  **`index.html`**: The interactive web prototype. This file can be opened in any browser to use the model live.

---

## ⚙️ Methodology

The project followed a structured machine learning workflow:

1.  **Data Exploration & Cleaning:** Loaded the dataset and performed EDA to understand its structure and identify key features.
2.  **Preprocessing:** Converted categorical labels to numerical format and applied `StandardScaler` to normalize the feature data for optimal model performance.
3.  **Baseline Modeling:** A Logistic Regression model was trained to establish a baseline performance. Its weaknesses (particularly low recall for the 'mid risk' class) were identified.
4.  **Advanced Modeling:** A `RandomForestClassifier` was trained, which dramatically improved upon the baseline, especially in correctly identifying the medium-risk class.
5.  **Evaluation & Interpretation:** The final model was evaluated using a classification report and confusion matrix. Feature importance was extracted to ensure the model's predictions were logical.
6.  **Prototyping:** A simple Decision Tree was trained to extract human-readable `if/else` rules, which were then implemented in JavaScript to create the interactive `index.html` demo.

## 📊 Model Performance

The final Random Forest model achieved a significant improvement over the baseline, with an overall accuracy of **81%**.

**Classification Report (Random Forest):**
| Metric | low risk | mid risk | high risk |
| :--- | :--- | :--- | :--- |
| **Precision** | 0.86 | 0.74 | 0.87 |
| **Recall** | 0.75 | 0.84 | 0.85 |
| **F1-Score** | 0.80 | 0.79 | 0.86 |

---

## 🚀 How to Use

### Viewing the Analysis
The complete analysis and code can be viewed by opening the **`Maternal-Risk-ML.ipynb`** file directly in GitHub.

### Running the Interactive Demo
1.  Download the **`index.html`** file from this repository.
2.  Open the file in any modern web browser (e.g., Chrome, Firefox, Edge).
3.  Enter new values for the patient's vitals and click the **"Predict Risk"** button to see the model in action.
