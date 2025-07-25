
## `3`. Daily Website Visitors -(Logistic Regression)

This dataset contains **daily website traffic logs** for a fictional site, including user activity across days of the week.  
Each row represents one day of traffic.

### 📂 Dataset
- [Dataset link](https://www.kaggle.com/datasets/bobnau/daily-website-visitors)

- **2167 rows** → Each row represents one day of website traffic  
- **8 columns** → Features like visits, date, and day of week

### Features and Their Meaning

| Feature Name           | Description                                               |
|------------------------|-----------------------------------------------------------|
| `Row`                  | Serial number (index) of the record                       |
| `Day`                  | Day number in sequence (1 for first day, and so on)       |
| `Day.Of.Week`          | Name of the weekday (e.g., Monday, Tuesday, etc.)         |
| `Date`                 | Calendar date of the record (MM/DD/YYYY format)           |
| `Page.Loads`           | Total number of pages loaded on that day (includes repeats)|
| `Unique.Visits`        | Number of distinct users who visited the website          |
| `First.Time.Visits`    | Users visiting the site for the first time                |
| `Returning.Visits`     | Repeat visitors who have visited before                   |


This project was designed to help me practice two key machine learning concepts:

- **Logistic Regression**: For binary classification — predicting whether a day is a *high-traffic day* or not.
- **Regularization (L1/Lasso)**: To automatically select the most relevant features and avoid overfitting.

I wanted to apply both in a real dataset workflow — starting from raw data and ending with model evaluation and visual insights.

### How I Used the Dataset

- I took this real-world web traffic dataset to **practice Logistic Regression and L1 Regularization**.  
- The goal was to build a model that predicts whether a given day had **high website traffic**.

### Steps I Followed

1. **Loaded and Cleaned the Data**
   - Removed the `Row` column
   - Fixed number formatting by removing commas in numeric columns
   - Converted the `Date` column to datetime

2. **Created New Features**
   - Extracted `Day`, `Month`, and `Day.Of.Week` from the date
   - Created a new feature `IsWeekend` to identify Saturdays and Sundays

3. **Defined Target Variable**
   - Created `HighTraffic` as binary output:  
     `1` if `Page.Loads` > average, else `0`

4. **Initial Feature Selection (L1 Regularization)**
   - Used `LogisticRegression` with `penalty='l1'` and `SelectFromModel`
   - Automatically selected features with non-zero coefficients
   - Visualized the coefficients with a barplot (green = selected, red = removed)
   - <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/L1%20Regularization%20feature%20Selection.png" width="400px">

5. **Explored Feature Relationships**
   - Used a heatmap to view correlations between features and target
   - <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Heatmap.png" width="400px">
   - Plotted logistic regression fit curves for each feature vs `HighTraffic`
<div align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Unique%20vs%20HT.png" width="400px">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/F%20vs%20H.png" width="400px">
</div><br>

<div align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Return%20Vs%20HT.png" width="400px">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/IsWeekend%20Vs%20HT.png" width="400px">
</div><br>

<div align="center">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Month%20vs%20HT.png" width="400px">
  <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Day%20Vs%20HT.png" width="400px">
</div>

6. **Manually Refined Features**
   - Based on visual patterns, manually chose:
     ```
     ['Unique.Visits', 'First.Time.Visits', 'Returning.Visits', 'IsWeekend']
     ```
   - These were intuitive, strong predictors and kept the model simple

7. **Trained Final Model**
   - Built a pipeline with `StandardScaler` + `LogisticRegression`
   - Trained on 80% of the data, tested on the remaining 20%

8. **Evaluated the Model**
   - Generated confusion matrix and classification report
   - <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Confusion%20Matrix.png" width="400px">
   - Calculated final accuracy score : 95.8525 %

9. **Visualized Final Predictions**
   - Plotted **Actual vs Predicted Probabilities**
     - Green dots = actual class (0 or 1)
     - Red dots = predicted probabilities from the model
     - <img src="https://github.com/kammala-kalyan/My-ML-Projects/blob/main/Daily%20Website%20Visitors/Actual%20Vs%20Predicted.png" width="400px">

---

🎯 Final Output:
- Features used: `['Unique.Visits', 'First.Time.Visits', 'Returning.Visits', 'IsWeekend']`
- Evaluation: Confusion matrix, accuracy, logistic plots
- Visuals: Coefficient barplot, correlation heatmap, logistic fits, and predicted scatter plot



