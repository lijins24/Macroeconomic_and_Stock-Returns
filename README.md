# Sector Rotation Strategy
This project investigates the influence of macroeconomic factors on the monthly returns of U.S. sector ETFs (Exchange-Traded Funds). By employing machine learning techniques such as XGBoost and LightGBM, alongside advanced feature engineering using Genetic Programming (GP), we aim to predict sector outperformance relative to the broader market. This approach integrates traditional statistical methods like OLS (Ordinary Least Squares) and innovative nonlinear feature generation to deliver actionable insights for sector-based investment strategies.
## Project Motivation
Sector ETFs represent groups of stocks from specific economic sectors (e.g., Technology, Energy, and Financials), allowing investors to gain exposure to an entire sector’s performance. Each sector responds differently to changes in economic conditions. For instance, sectors like Energy and Utilities are sensitive to commodity price fluctuations, while sectors like Financials and Consumer Discretionary respond to interest rates, inflation, and consumer spending. These relationships also vary across economic cycles, including the early, mid, late, and recession phases.

Understanding these relationships can enable better investment decisions by identifying which economic indicators are likely to drive sector returns above those of the S&P 500. This project examines these dynamics, identifying influential macroeconomic factors that impact sector performance and optimizing the model’s predictive accuracy through GP.
## Project Structure
### Phase 1
### Data Collection and Preprocessing
We gathered over 100 macroeconomic factors (e.g., bond yields, CPI, PPI) and preprocessed them by filling missing values, standardizing data, and managing multicollinearity using Variance Inflation Factor (VIF).
### Feature Engineering: 
Genetic Programming was used to generate new features by combining selected macroeconomic factors. GP allowed us to capture nonlinear interactions between factors, potentially enhancing the model’s predictive power.
### Predictive Modeling:
Ordinary Least Squares (OLS) regression was used to calculate rolling exposures of each factor, providing insights into time-varying relationships between factors and sector returns.

Machine Learning Models (XGBoost and Reinforcement Learning) were then applied to predict the four sectors with the highest excess returns over the S&P 500 benchmark, using a rolling 3-year window for training and prediction.
### Phase 2
Refine the issues found in Phase 1 then apply machine learning techniques, such as XGBoost and LightGBM using different combination of features outputs from Phase 1 and features picked through domain knowledge to contruct portfolios.
### Evaluation:
Key evaluation metrics used to measure model performance include:

Top-4 Accuracy: Fraction of correctly predicted top-performing sectors.
Sharpe Ratio: Risk-adjusted performance metric.
Sortino Ratio: Focused on downside risk.
Maximum Drawdown: Largest observed loss from peak to trough.
Cumulative Returns: Visualization of portfolio growth over time.

Backtesting again benchmark S&P 500
## Key Files
Project Part 1.ipynb: contains code for entire phase 1 of the project.
Project Part 2.ipynb: contains code for entire phase 2 of the project.

BackTesting.ipynb: backtesting process and metrics
5500_Dataset.csv: containing raw datasets of sector ETF returns and macroeconomic indicators.

