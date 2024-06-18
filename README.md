# Stock-market-prediction
Predicting future stock performance using Earnings Call Transcripts and year-over-year financial metric changes
# Project ReadMe

## Overview

This project aims to predict stock growth by leveraging Earnings Call transcripts and financial data. It integrates an NLP model and a statistical learning model to enhance prediction accuracy, providing a robust tool for portfolio management.

## Objectives

1. **Construct a Profitable Portfolio**: Utilize Earnings Call transcripts and financial data to create a portfolio that consistently outperforms the market.
2. **Enhance Investment Decisions**: Integrate NLP model results with financial metrics to improve the accuracy and reliability of stock growth predictions.
3. **Automate Portfolio Management**: Develop a fully automated system for constructing and managing a profitable portfolio, minimizing the need for human intervention.
4. **Support Professional Portfolio Managers**: Provide predicted probabilities to compare different stocks, serving as a valuable tool for professional portfolio managers to make informed investment decisions.

## Data Collection

### Textual Data
- **Source**: Earnings Call transcripts.
- **Processing**: 
  - Remove non-informative phrases, such as those from the call operator and any greetings or goodbyes.
  - Clean and preprocess text for NLP modeling.

### Financial Data
- **Source**: Company financial reports.
- **Processing**:
  - Collect financials reported before the earnings call.
  - Standardize data by calculating year-over-year changes for each financial metric to account for seasonality.

### Market Capitalization and Prices
- **Market Capitalization**: Use the last known value before the Earnings Call date.
- **Price Change Calculation**: 
  - Calculate the ratio of the closing price on the call date plus 90 days to the closing price on the call date plus 1 day.

## Model Training

### NLP Model
- Train the NLP model on cleaned Earnings Call transcripts.
- Evaluate the model using precision to focus on the proportion of correctly predicted growing stocks in our portfolio.

### Financials Model
- Use the results of the NLP model as input.
- Integrate financial data to train a statistical learning model, enhancing prediction accuracy.

## Evaluation

- **Precision**: Use precision on the top 100 stocks with the highest predicted probability of growth for each period.
- **Comparison with Market**: Compare model performance against the market to ensure it consistently outperforms.

## Implementation Steps

1. **Data Collection**:
   - Execute `Data_Collection.ipynb` to gather and preprocess textual and financial data.
2. **NLP Model Training**:
   - Run `NLP_Model.ipynb` to train the model on Earnings Call transcripts.
3. **Financials Model Training**:
   - Execute `Financials_Model.ipynb` to train the statistical learning model using NLP model predictions and financial data.
4. **Evaluation**:
   - Assess model performance using precision and market comparison metrics.

## Usage

- **Portfolio Construction**: Use the model to construct a profitable portfolio without manual intervention.
- **Professional Use**: Utilize predicted probabilities to compare different stocks, aiding professional portfolio managers in decision-making.

## Conclusion

This project provides a comprehensive approach to predicting stock growth, combining NLP and financial data analysis to offer a powerful tool for portfolio management. The model's consistent outperformance of the market ensures its reliability and effectiveness.

---

For further details, please refer to the respective Jupyter notebooks (`Data_Collection.ipynb`, `NLP_Model.ipynb`, `Financials_Model.ipynb`) included in this project.
