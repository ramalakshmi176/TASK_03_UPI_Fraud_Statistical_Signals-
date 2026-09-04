# UPI Fraud Statistical Signals Analysis

## 1. Problem Statement
Digital payment platforms face significant risks from fraudulent activities. Following a 31% surge in fraud reports, this project conducts a statistical investigation to detect abnormal transaction patterns and identify early fraud indicators[cite: 1].

## 2. Dataset Description
- **Type**: Synthetic UPI Transaction Dataset[cite: 1]
- **Size**: 5,000 records
- **Features**: `Transaction_ID`, `User_ID`, `Account_Age_Days`, `Transaction_Amount`, `Hour_of_Day`, `Device_Changes`, `Daily_Freq`, `Is_Fraud`[cite: 1]

## 3. Statistical Methods Used
- **Descriptive Statistics**: Mean, median, standard deviation, quartiles, and skewness analysis[cite: 1].
- **Outlier Detection**: Interquartile Range (IQR) and Z-Score thresholding ($|Z| > 3$)[cite: 1].
- **Hypothesis Testing**:
  - Two-sample T-Test (Transaction Amount vs. Fraud)[cite: 1]
  - Chi-Square Test of Independence (Device Changes vs. Fraud)[cite: 1]

## 4. Fraud Signal Findings
1. **Device Swapping (>2 changes)**: Strongest indicator of unauthorized account access[cite: 1].
2. **Off-Hours Activity (12 AM - 5 AM)**: High concentration of fraud spikes[cite: 1].
3. **High Amount Outliers on Fresh Accounts (<30 days)**: Unusually large transactions on new accounts[cite: 1].

## 5. Visual Analysis
The exploratory charts are stored under `images/eda_patterns.png`[cite: 1].
- **Box Plot**: Shows severe right-skewness and extreme outliers in transaction amounts[cite: 1].
- **Bar Chart**: Highlights elevated fraud rates associated with frequent device changes[cite: 1].
- **Heatmap**: Displays correlation between behavioral metrics and fraud status[cite: 1].

## 6. Business Recommendations
- **MFA Enforcement**: Trigger mandatory Multi-Factor Authentication whenever a device change is detected[cite: 1].
- **Off-Hour Controls**: Apply step-up verification or delayed settlements for high-value transactions between midnight and 5 AM[cite: 1].
- **Dynamic Limits**: Impose initial transaction caps during the first 30 days of account creation[cite: 1].

## 7. Future Scope
- Implement real-time machine learning classification models (XGBoost / Isolation Forests).
- Incorporate geolocation tracking to flag rapid geographical velocity changes.# TASK_03_UPI_Fraud_Statistical_Signals-
