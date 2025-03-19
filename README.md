# Final_Capstone
folder containing final capstone assignment for ML/AI class

# Housing Price Prediction - Final Capstone Project Report

## **1. Problem Statement**
Housing prices are influenced by various factors, such as location, population density, and median household income. This project aims to develop a **machine learning model** that accurately predicts housing prices based on a dataset of California housing prices.

The model can be useful for:
- **Real estate investors** to assess property values
- **Homebuyers** to evaluate fair market prices
- **Urban planners and policymakers** for housing affordability analysis

### **2. Challenges:**
- Sources appropiate data
- Handling and cleaning data appropiately
- Handling missing data effectively
- Selecting relevant features for better predictive power
- Choosing the best model to maximize accuracy

---
## **3. Model Outcomes & Predictions**
- **Type of Learning:** Supervised Learning
- **Problem Type:** Regression
- **Expected Output:** Predicting the **median house value** based on various features.
- **Machine Learning Models Used:**
  - **Linear Regression**
  - **Ridge Regression**
  - **Lasso Regression**
  - **Bayesian Ridge Regression**
  - **Random Forest Regressor (Original & Improved)**

---
## **4. Data Acquisition**
- **Dataset:** Kaggle - California Housing Prices
- **Number of Rows:** ~20,000
- **Number of Columns:** 10

### **5. Key Features:**
- `total_rooms`: Total number of rooms per block.
- `total_bedrooms`: Total number of bedrooms per block.
- `population`: Total population in the block.
- `households`: Number of households in the block.
- `median_income`: Median income per household.
- `ocean_proximity`: Categorical variable indicating location type (e.g., near ocean, inland).

### **6. Feature Engineering:**
- **One-Hot Encoding** applied to `ocean_proximity` to convert it into multiple binary columns.
- **Feature selection** based on correlation matrix analysis

---
## **7. Data Preprocessing & Preparation**
- **Handling Missing Data:**
  - initially dropped rows with NaNs for easy data handling.
  - Filled NaNs with zeros for categorical features in One-Hot-Encoder created features.
- **Data Splitting:**
  - **60% Training**, **20% Validation**, **20% Test Split**
  - Ensured categorical variables were **encoded consistently** across train/test sets.

---
## **8. Modeling Approaches**
### **Baseline Models:**
- **Linear Regression**: Initial benchmark model.
- **Ridge & Lasso Regression**: Regularization techniques to reduce overfitting.
- **Bayesian Ridge Regression**: Probabilistic regression approach.

### **9. Advanced Model:**
- **Random Forest Regressor (Original & Improved)**:
  - Initial model: **R² ~ 60%**
  - Improved model (with feature engineering): **R² ~ 81%**

---
## **10. Model Evaluation**
### **Evaluation Metrics Used:**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R² Score** (Explains variance in target variable)

| Model | R² Score | MSE | MAE |
|-------------------------|---------|----------------|-------------|
| Linear Regression | 0.5388 | 6.41e+09 | 59,345.41 |
| Ridge Regression | 0.5388 | 6.32e+09 | 59,247.70 |
| Random Forest (Original) | 0.6008 | 5.47e+09 | 53,165.95 |
| Random Forest (Improved) | 0.8142 | 2.54e+09 | 33,163.26 |

### **11. Conclusions:**

**After Linear Regression first run, different ways to improve it (Ridge, Lasso) didn't improve it much**
**Random forest model worked much better than Linear Regression from the get go**
**One-hot encoding significantly improved model accuracy** (from 60% to 81% R²).
**Future potential improvements:** additional feature engineering.

---
## **12. How to Run the Project**
### **Requirements:**
- Python 3.8+
- Required libraries:
  ```bash
  pip install pandas numpy scikit-learn seaborn matplotlib
  ```
---
## **13. Authors & Acknowledgments**
- **Author:** Bruna Moscol
- **Dataset Source:** Kaggle - California Housing Prices
- **Course:** Introduction to Machine Learning and AI 

---
## **14. License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

