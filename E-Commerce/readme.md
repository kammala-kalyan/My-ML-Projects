<!--
## `1`. E-Commerce Customers - Linear Regression Project 

This project analyzes customer data from an e-commerce company to predict the yearly amount spent by a customer.

### 📂 Dataset
- [Dataset link](https://www.kaggle.com/datasets/srolka/ecommerce-customers)
  
### What I did:
- Loaded and explored the dataset
- Features Selected (Based on Correlation)
- Visualized correlations using pairplot and heatmap
- Trained a Linear Regression model
- Evaluated with MAE, RMSE, and R² scores
- Achieved **1.45% average percent error**

### Output & Evaluation
- Evaluation was done on test data (20%) using standard regression metrics.

| Metric                  | Value     |
| ----------------------- | --------- |
| Train R² Score          | 0.9827    |
| Test R² Score           | 0.9892    |
| Mean Absolute Error     | Low       |
| Root Mean Squared Error | Low       |
| Avg Percent Error     | **1.45%** |

#### Interpretation:

- The model predicts yearly customer spending with very high accuracy and minimal error.
- No signs of overfitting were found (Test R² > Train R²).

#### Model Evaluation: Actual vs Predicted 
<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Actual%20Vs%20Predicted1.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Actual%20VS%20Predicted.png" width="45%" />
</p>


### Navigate to Project Notebook:
🔗 E-Commerce Linear Regression Notebook : [Click Here !](https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/E-Commerce_code.ipynb)
--
## `1`. E-Commerce Customers – Linear Regression

This project analyzes **customer behavior and spending** from an e-commerce company.  
The goal was to build a linear regression model to predict how much a customer is likely to spend annually based on their profile.

---

### 📂 Dataset
- [Dataset link](https://www.kaggle.com/datasets/srolka/ecommerce-customers)

- **500 rows** → Each row = one customer  
- **8 columns** → Features about customer activity, location, and time spent

---

### Features and Their Meaning

| Feature Name            | Description                                               |
|-------------------------|-----------------------------------------------------------|
| `Email`                | Customer’s email ID                                       |
| `Address`              | Physical address                                          |
| `Avatar`               | Profile image (not used in modeling)                      |
| `Avg. Session Length`  | Average session duration on the website                   |
| `Time on App`          | Time spent on the mobile app                              |
| `Time on Website`      | Time spent on the website                                 |
| `Length of Membership` | How long the customer has been with the company           |
| `Yearly Amount Spent`  | Target variable – total yearly spending (in dollars)      |

---

### What I Wanted to Practice

- **Linear Regression**: To build a predictive model using continuous input features  
- **Correlation Analysis**: Understand feature impact on target  
- **Model Evaluation**: Using metrics like R², MAE, RMSE, and visual comparisons  
- **Data Interpretation**: Translate numeric insights into business understanding

---

### Work Flow with Steps Followed:

1. **Loaded and Explored the Data**
   - Imported dataset using `pandas`
   - Checked structure, null values, and datatypes

2. **Performed Exploratory Data Analysis**
   - Plotted a `pairplot` to view relationships among all numerical features
   - Generated a `correlation heatmap` to detect strong associations

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/heatmap.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/pairplot.png" width="45%" />
</p>

3. **Selected Relevant Features**
   - Based on heatmap & pairplot, selected:
     ```
     ['Avg. Session Length', 'Time on App', 'Time on Website', 'Length of Membership']
     ```
   - Target: `Yearly Amount Spent`

4. **Trained a Linear Regression Model**
   - Split data into training and test sets (80-20)
   - Trained using `LinearRegression()` from scikit-learn

5. **Evaluated the Model**
   - Computed:
     - `Train R²` Score → 0.9827  
     - `Test R²` Score → 0.9892  
     - Mean Absolute Error and RMSE → Very Low  
     - **Average Percent Error** → Just **1.45%**

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Actual%20Vs%20Predicted1.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Actual%20VS%20Predicted.png" width="45%" />
</p>

---

### Navigate to Project Notebook:

🔗 E-Commerce Linear Regression Notebook: [Click Here!](https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/E-Commerce_code.ipynb)

---

## Conclusion

This mini project gave me hands-on practice with **Linear Regression** and taught me how customer features can be used to accurately predict business metrics like **yearly spending**.  
With **simple preprocessing** and **feature selection**, I built a powerful regression model with **minimal error** — making it a great example of applying ML to real-world business problems.

---
-->
## `1`. E-Commerce Customers – Linear Regression

This project explores **customer spending patterns** for an e-commerce company and builds a **Linear Regression model** to predict the **Yearly Amount Spent** based on customer behavior and profile features.

---

### 📂 Dataset
- [Dataset link](https://www.kaggle.com/datasets/srolka/ecommerce-customers)

- **500 rows** → Each row = one customer  
- **8 columns** → Features about customer activity, location, and spending

---

### Features and Their Meaning

| Feature Name            | Description                                                 |
|-------------------------|-------------------------------------------------------------|
| `Email`                | Customer's email address                                    |
| `Address`              | Physical location (not used in modeling)                   |
| `Avatar`               | Profile picture file (not used in modeling)                |
| `Avg. Session Length`  | Average session duration on the website                    |
| `Time on App`          | Time spent on the mobile app                               |
| `Time on Website`      | Time spent on the website                                  |
| `Length of Membership` | How long the customer has been with the company            |
| `Yearly Amount Spent`  | Target variable – total yearly spending by the customer     |

---

### What I Wanted to Practice

- Building and interpreting a **Linear Regression model**
- Understanding **correlation** between user behavior and spending
- Evaluating predictions with **MAE, RMSE, and R²**
- Visualizing **actual vs predicted** and calculating **percent error**

---

### Work Flow with Steps Followed:

1. **Loaded and Inspected the Data**
   - Loaded using pandas and checked for missing/null values
   - Used `.describe()` to get a statistical summary

2. **Exploratory Data Analysis (EDA)**
   - Plotted pairplot to explore feature relationships
   - Generated a correlation heatmap to identify strong predictors

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/pairplot.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Correlation%20HeatMap.png" width="45%" />
</p>

3. **Visualized Key Feature Relationships**
   - Created scatter plots between `Yearly Amount Spent` and:
     - `Avg. Session Length`
     - `Time on App`
     - `Length of Membership`

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Avg%20session%20Length%20vs%20Yearly%20Amount%20Spent.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Time%20On%20app%20vs%20Yearly%20amount%20spent.png" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Length%20of%20Member%20ship%20vs%20Yearly%20Amount%20spent.png" width="45%" />
</p>

4. **Selected Features & Created Train/Test Split**
   - Based on correlation and scatter plots, selected:
     ```
     ['Avg. Session Length', 'Time on App', 'Length of Membership']
     ```
   - Used `train_test_split()` to split data 80% train and 20% test

5. **Trained Linear Regression Model**
   - Fitted `LinearRegression()` model on training data
   - Extracted coefficients to interpret feature importance

6. **Made Predictions & Evaluated the Model**
   - Predicted `Yearly Amount Spent` on test data
   - Calculated:
     - **Mean Absolute Error (MAE)**
     - **Root Mean Squared Error (RMSE)**
     - **Percent Error** ≈ **1.45%**
     - **Train R²** = 0.9887  
     - **Test R²** = 0.9855

   - Plotted regression line vs actual values
   - Created scatter plot of actual vs predicted
   - Displayed residual heatmap

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Actual%20VS%20Predicted.png" width="45%" />
  &nbsp;&nbsp;
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Actual%20vs%20Predicted%20in%20Scatterplot.png" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Images/Actual%20Vs%20Predicted%20heatmap.png" width="45%" />
</p>

---

### Navigate to Project Notebook:

🔗 E-Commerce Linear Regression Notebook: [Click Here!](https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/E-Commerce_code.ipynb)

---

## Conclusion

This mini project gave me hands-on practice with **Linear Regression** and taught me how customer features can be used to accurately predict business metrics like **yearly spending**.  
With **simple preprocessing** and **feature selection**, I built a powerful regression model with **minimal error** — making it a great example of applying ML to real-world business problems.
