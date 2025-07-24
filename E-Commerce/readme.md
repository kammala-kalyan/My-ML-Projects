
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
  
### Actual vs Predicted Heat Map:
<img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/Actual%20Vs%20Predicted1.png" width="500">

### Navigate to Project Notebook:
🔗 E-Commerce Linear Regression Notebook : [Click Here !](https://github.com/kammala-kalyan/My-ML-Projects/blob/main/E-Commerce/E-Commerce_code.ipynb)
