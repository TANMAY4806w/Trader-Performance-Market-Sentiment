# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader behavior and performance on Hyperliquid. The analysis uncovers actionable patterns to inform smarter trading strategies.

**Key Findings:**
- Traders show significantly different performance during Fear vs Greed periods
- Optimal leverage and trading frequency vary with market sentiment
- Trader segmentation reveals distinct behavioral archetypes with different risk profiles

## Project Structure

```
Trader-Performance-Market-Sentiment/
├── analysis.ipynb                    # Main analysis notebook
├── fear_greed_index.csv              # Bitcoin Fear/Greed sentiment data
├── historical_data.csv               # Hyperliquid trader transaction data
├── outputs/                          # Generated outputs
│   ├── charts/                       # Visualizations (9 PNG files)
│   │   ├── performance_fear_vs_greed.png
│   │   ├── drawdown_fear_vs_greed.png
│   │   ├── behavior_fear_vs_greed.png
│   │   ├── segment_analysis.png
│   │   ├── insight1_sentiment_profitability.png
│   │   ├── insight2_leverage_sentiment.png
│   │   ├── insight3_frequency_performance.png
│   │   ├── insight4_long_short_bias.png
│   │   └── predictive_model_results.png
│   ├── daily_metrics.csv             # Processed daily metrics
│   └── merged_data.csv               # Merged dataset
├── METHODOLOGY_AND_INSIGHTS.md       # Analysis write-up (methodology, insights, strategies)
├── requirements.txt                  # Python dependencies
└── README.md                         # This file
```

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone or download this repository**

2. **Install required dependencies:**

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

Or using conda:

```bash
conda install pandas numpy matplotlib seaborn scipy jupyter
```

### Running the Analysis

1. **Start Jupyter Notebook:**

```bash
jupyter notebook
```

2. **Open `analysis.ipynb`**

3. **Run all cells:**
   - Click "Kernel" → "Restart & Run All"
   - Or run cells sequentially from top to bottom

4. **Expected runtime:** 2-5 minutes depending on your system

## Analysis Components

### Part A: Data Preparation
- Loads and documents both datasets
- Converts timestamps and aligns data by date
- Engineers key metrics:
  - Daily PnL per trader
  - Win rate
  - Average trade size
  - Trading frequency
  - Long/short ratio
  - Leverage proxy

### Part B: Analysis
Answers four key questions:

1. **Does performance differ between Fear vs Greed days?**
   - Statistical comparison of PnL, win rate, and drawdown

2. **Do traders change behavior based on sentiment?**
   - Analysis of trade frequency, position sizes, leverage, and long/short bias

3. **Trader Segmentation:**
   - High vs low leverage traders
   - Frequent vs infrequent traders
   - Consistent winners vs inconsistent traders

4. **Key Insights (4+ with visualizations):**
   - Sentiment impact on profitability
   - Leverage effects by sentiment
   - Trading frequency optimization
   - Long/short bias patterns

### Part C: Actionable Strategies

**Strategy 1: Leverage Adjustment**
- Reduce leverage 20-30% during Fear periods
- Maintain/increase for consistent winners during Greed

**Strategy 2: Frequency Optimization**
- Reduce trade frequency 30-40% during Fear for frequent traders
- Increase 20-30% during Greed for consistent winners

## Key Metrics

- **211,224 trades** analyzed
- **32 unique trader accounts**
- **246 trading pairs**
- **2+ years** of data (2023-2025)
- **2,644 days** of sentiment data

## Generated Outputs

### Visualizations (in `outputs/charts/`)
- `performance_fear_vs_greed.png` - PnL and win rate comparison
- `drawdown_fear_vs_greed.png` - Drawdown analysis
- `behavior_fear_vs_greed.png` - Behavioral metrics comparison
- `segment_analysis.png` - Trader segment performance
- `insight1_sentiment_profitability.png` - Profitability by sentiment
- `insight2_leverage_sentiment.png` - Leverage impact analysis
- `insight3_frequency_performance.png` - Frequency optimization
- `insight4_long_short_bias.png` - Position bias analysis
- `predictive_model_results.png` - ML model performance and feature importance

### Data Files (in `outputs/`)
- `daily_metrics.csv` - Aggregated daily metrics per trader
- `merged_data.csv` - Complete merged dataset

## Methodology

1. **Data Integration:** Merged sentiment data with trader transactions at daily granularity
2. **Feature Engineering:** Created behavioral and performance metrics
3. **Statistical Analysis:** T-tests to validate performance differences (p < 0.05)
4. **Segmentation:** Grouped traders by leverage, frequency, and win rate
5. **Visualization:** Generated charts to support insights

## Requirements

```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
jupyter>=1.0.0
```

## Limitations

- Analysis limited to 32 accounts; larger sample would strengthen conclusions
- Leverage proxy estimated from position sizes; actual leverage data would be more accurate
- Correlation does not imply causation; sentiment may correlate with other market factors
- Past performance doesn't guarantee future results

## Bonus Work Completed

### Predictive Model ✅
- Built machine learning models (Logistic Regression & Random Forest)
- Predicts next-day trader profitability
- Features: sentiment, rolling averages, behavioral metrics
- Evaluation: accuracy, precision, recall, confusion matrix
- Feature importance analysis identifies key predictors

## Future Enhancements

- Clustering traders into behavioral archetypes
- Backtest strategy recommendations
- Expand to hourly granularity analysis
- Interactive Streamlit dashboard

## Author

Data Science Intern Assignment - Primetrade.ai  
February 2026

## License

This project is for educational and evaluation purposes.
