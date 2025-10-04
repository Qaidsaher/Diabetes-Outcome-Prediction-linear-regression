# Diabetes Outcome Prediction – Linear Regression

## 🧠 Overview
Developed by **Saher Qaid**, this project demonstrates how **Linear Regression** can be used to predict diabetes outcomes using real-world medical data.  
It covers all stages of a typical machine learning workflow — from data exploration and preprocessing to model evaluation, visualization, and feature interpretation.

---

## 📦 Repository Information
**Repository Name:** `QaidSaher/Diabetes-Outcome-Prediction-Linear-Regression`  
**Created by:** Saher Qaid  
**Created on:** October 04, 2025  
**Description:** A complete machine learning project by Saher Qaid demonstrating the use of Linear Regression to predict diabetes outcomes using real-world health indicators. Includes data exploration, scaling, model training, evaluation metrics, and visual insights.  

---

## 📊 Dataset Overview
The dataset (`diabetes_dataset.csv`) includes medical and demographic factors commonly associated with diabetes risk.

| Feature | Description |
|----------|--------------|
| Pregnancies | Number of pregnancies |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-hour serum insulin (mu U/ml) |
| BMI | Body Mass Index (weight in kg / (height in m)^2) |
| DiabetesPedigreeFunction | Family history indicator for diabetes |
| Age | Patient age in years |
| Outcome | Target variable (1 = diabetic, 0 = non-diabetic) |

---

## ⚙️ Project Workflow

### 1️⃣ Data Exploration
- Loaded the dataset using **pandas** and explored its structure.
- Displayed dataset shape, column names, and previewed the first five rows.

### 2️⃣ Data Splitting
- Divided data into **training (70%)** and **testing (30%)** sets.  
- Used a consistent seed derived from university ID digits for reproducibility.

### 3️⃣ Feature Scaling
- Applied **StandardScaler** to normalize input features based on training data only.

### 4️⃣ Model Training
- Trained a **Linear Regression** model using `scikit-learn`.  
- The model learns coefficients representing the influence of each health metric on diabetes outcome.

### 5️⃣ Model Evaluation
| Metric | Meaning | Result (Example) |
|:--|:--|:--|
| **R² (R-squared)** | Explains proportion of variance captured by model | 0.3088 |
| **MAE (Mean Absolute Error)** | Average prediction error | 0.3286 |
| **RMSE (Root Mean Squared Error)** | Measures error magnitude | 0.4019 |

These results suggest the linear model explains roughly **31% of the outcome variation**, offering a baseline for predictive modeling.

### 6️⃣ Visualization
- **Parity Plot:** Displays actual vs. predicted diabetes outcomes.  
- **Residuals Plot:** Highlights the distribution of prediction errors.  

Both visuals confirm the model’s trend-following ability but show expected deviations due to binary output values.

### 7️⃣ Coefficients & Feature Influence
| Feature | Coefficient | Interpretation |
|----------|--------------|----------------|
| Glucose | +0.1908 | Higher glucose → higher diabetes likelihood |
| BMI | +0.0907 | Higher BMI → higher risk |
| Pregnancies | +0.0681 | Slight positive correlation |
| BloodPressure | -0.0394 | Weak negative effect |
| Insulin | -0.0183 | Weak negative relationship |
| Age | +0.0284 | Slight increase with age |

🔹 **Top Influencer:** *Glucose*  
🔹 **Secondary Factors:** *BMI*, *Pregnancies*  

### 8️⃣ Key Observations
- Linear Regression provides interpretability and insight into feature influence.  
- However, since **Outcome** is binary, it’s not ideal for precise classification.  
- The model’s visual and numerical results confirm moderate but meaningful predictive ability.

### 9️⃣ Limitations & Future Work
1. Predictions may fall outside the binary [0, 1] range.  
2. Linear assumptions limit model flexibility.  
3. Non-linear classifiers (e.g., Logistic Regression, Decision Trees, SVMs) could improve accuracy.  
4. Feature engineering and correlation analysis could further refine predictions.

---

## 📈 Summary of Findings
- The model explains ~31% of the variance in diabetes outcomes.  
- **Glucose** is the strongest indicator of diabetes, followed by **BMI** and **Pregnancies**.  
- The residual plots show reasonable fit but not perfect prediction boundaries.  
- This project serves as an educational baseline for binary classification using regression.

---

## 🧰 Tools & Technologies
- **Python 3.10+**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**

---

## 🚀 How to Run Locally
```bash
# Clone the repository
git clone https://github.com/QaidSaher/Diabetes-Outcome-Prediction-Linear-Regression.git

# Open in Jupyter Notebook or Google Colab
# Upload the 'diabetes_dataset.csv' file and execute cells sequentially.
```

---

## 👨‍💻 Author
**Saher Qaid**  
Data Science & Machine Learning Developer  
📧 Contact: [saherqaid2020@gmail.com]  
🌐 GitHub: [github.com/Qaidsaher](https://github.com/Qaidsaher)

---

## 📜 License
This project is provided for **educational and research purposes**.  
You may use or modify it with appropriate credit to the author.
