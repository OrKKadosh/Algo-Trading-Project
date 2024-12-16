# **Enhancing Stock Market Prediction with Sentiment Analysis and Machine Learning**

## **Overview**
This project leverages sentiment analysis from **social media** and **financial websites**, combined with technical analysis, to predict stock market trends. By integrating data from multiple sources and training an **XGBoost model**, the system achieves better predictive accuracy and higher returns compared to standard strategies.

---

## **Features**
- **Sentiment Analysis**:
  - Extracts social media posts (Twitter, Reddit) using APIs like **Snscrape** and scores sentiment with **VaderSentiment**.
  - Collects financial article sentiments using **AlphaVantage**.
- **Technical Indicators**:
  - Calculates **MACD** values, normalized using the ATR indicator for volatility adjustment.
- **Machine Learning Model**:
  - Trains an **XGBoost model** on sentiment and technical data to classify stocks as:
    - `0 (Sell)`, `1 (Neutral)`, `2 (Buy)`.

---

## **How It Works**
1. **Data Collection**:
   - Gathered financial reports, news articles, and social media posts for **S&P500 stocks**.
2. **Sentiment Scoring**:
   - Assign sentiment scores to news, tweets, and Reddit posts based on relevance and engagement.
3. **Training & Testing**:
   - Used 9 months of data for training and 3 months for testing.
   - Model classified stocks by return probabilities.
4. **Backtesting**:
   - Simulated trades based on model predictions (Buy at `2`, Sell at `0`).

---

## **Results**
- **Backtest Performance** (last 3 months, hyped stocks):
  - **Mean ROI**: 3%-4%.
  - **Sharpe Ratio**: 0.7-1.1.
  - **Maximum Drawdown**: -3% to -7%.
- Improved returns by **1.25x to 5x** over non-model strategies.

---

## **Technologies**
- **Python**: Core programming language.
- **APIs**:
  - **Snscrape** for Twitter data.
  - **AlphaVantage** for financial data.
  - **VaderSentiment** for sentiment scoring.
- **XGBoost**: Machine learning model.
- **MACD & ATR**: Technical indicators.

---

## **Key Findings**
- Adding more data (social media, sentiment analysis) improved accuracy.
- The model outperformed "Buy & Hold" strategies in hyped stocks.
- Balancing the classification target (`0`, `1`, `2`) improved performance.

---

## **Challenges**
- **API Limitations**:
  - Inconsistent data availability across stocks.
  - Restrictions on sentiment scores for financial advice.
- **Data Gaps**: Limited information for low-profile stocks reduced accuracy.
- **Resource Constraints**: Limited infrastructure for large-scale deployment.

---

## **Contributors**
- **Or Kadosh**
- **Shir Chen**
- **Itay Hakmon**
- **Boaz Bar-David**

---

## **Disclaimer**
This project is for educational purposes only and is not intended for real-world trading or financial advice.


## Installation
Install the requireded packages in the wanted environment

```bash
pip install -r requirements.txt
```

## Usage
In order to run the backtesting algorithm, run the model_train_and_backtesting.py file.

## Credits
This project is the collaborative effort of a group of friends.

Names:

Boaz Bar David

Or Kadosh

Itay Hakmon

Shir Chen
