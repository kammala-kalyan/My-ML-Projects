
## `1`. E-Commerce Customers – Linear Regression

This dataset contains customer information for an e-commerce platform, including behavioral and spending data. Each row represents one customer, and the goal is to predict the yearly amount spent by a customer based on their engagement with the website and app.

It includes features like average session length, time on app, length of membership, and more — useful for building a linear regression model to understand key drivers of customer spending.

### 📂 Dataset
- [Dataset link](https://www.kaggle.com/datasets/srolka/ecommerce-customers)

- **500 rows** → Each row = one customer  
- **8 columns** → Features about customer activity, location, and spending


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

### What I Wanted to Practice

- Building and interpreting a **Linear Regression model**
- Understanding **correlation** between user behavior and spending
- Evaluating predictions with **MAE, RMSE, and R²**
- Visualizing **actual vs predicted** and calculating **percent error**

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
     - Mean Absolute Error: 6.84602715809049
     - Mean Squared Error: 78.86825975788848
     - Root Mean Squared Error: 8.880780357484836
     - Percent Error ≈ **1.45%**
     - Train R² = 0.9887  
     - Test R²  = 0.9855

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
