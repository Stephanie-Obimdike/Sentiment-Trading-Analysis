Sentiment and Trading Analysis
This project analyzes the relationship between market sentiment and trading performance across 184,263 trades to identify behavioral biases and optimize trading strategies.

Setup and How to Run
Environment: This project is designed to run in Google Colab or any Jupyter Notebook environment.
Dependencies: Ensure you have pandas, matplotlib, scikit-learn, and joblib installed.
Data: Upload your merged file containing the trades and sentiment index data.
Execution: Run the cells in the notebook sequentially to perform the data cleaning, visualization, and model training.

Methodology
Data Merging: Aligned thousands of trades with daily sentiment data using timestamps to create a unified dataset.
Feature Engineering: Converted categorical sentiment into numerical indices and included "Size USD" to capture trader behavior.
Model Selection: Implemented a Decision Tree Classifier to predict trade outcomes (Win/Loss).
Validation: Split the data into 80% training and 20% testing sets to verify accuracy on unseen data.

Insights
The Sentiment Gap: Win rates are highest during Extreme Greed (49.0%) and lowest during Neutral market conditions (31.7%).
Volume Paradox: The highest trade volume occurs during Fear (133,871 trades), which correlates with a lower win rate compared to Greed phases.
Predictive Power: The model achieves an accuracy of 58.26%, proving that combining sentiment with trade size offers a statistical edge in predicting outcomes.

Strategy Recommendations:
1. The fear filter for small traders: Small traders have the lowest win rates during the fear and neutral market sentiments. This means that the filter should trigger a warning to reduce trade frequency in order to prevent panic trading.
2. Extreme Greed Boost: Since the highest win rate occurs during extreme greed, there should be an indicator to let traders increase USD size to be able to be more profitable.
