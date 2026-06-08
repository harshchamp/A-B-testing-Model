# A/B Testing Model

A comprehensive statistical analysis project for mobile game A/B testing using Python and Jupyter Notebook. This project analyzes user retention and engagement metrics across different game configurations.

## Overview

This project performs in-depth A/B testing analysis on the Cookie Cats mobile game dataset. It compares two different gate placements (gate_30 vs gate_40) to determine their impact on user retention and engagement metrics. The analysis includes data exploration, statistical testing, and visualization of key performance indicators.

## Project Structure

- **AB_Testing.ipynb** - Main Jupyter notebook containing comprehensive A/B testing analysis and visualizations

## Dataset

The project uses the **Cookie Cats** dataset from Kaggle, which contains mobile game user engagement data.

**Data Source:** [Mobile Games A/B Testing](https://www.kaggle.com/datasets/yufengsui/mobile-games-ab-testing)

**File:** `cookie_cats.csv` (90,189 user records)

### Data Overview

| Column | Type | Description |
|--------|------|-------------|
| userid | Integer | Unique user identifier |
| version | String | Game version (gate_30 or gate_40) |
| sum_gamerounds | Integer | Total number of game rounds played |
| retention_1 | Boolean | User retained after 1 day |
| retention_7 | Boolean | User retained after 7 days |

### Dataset Statistics

- **Total Records:** 90,189 unique users
- **No Missing Values:** Dataset is complete with no null entries
- **No Duplicates:** All user IDs are unique
- **Date Range:** Mobile game engagement data from a test period

## Key Features

- **Comparative Analysis:** Gate_30 vs Gate_40 user engagement comparison
- **Retention Metrics:** 1-day and 7-day user retention tracking
- **Engagement Analysis:** Player round frequency and engagement patterns
- **Data Visualization:** Distribution plots, boxplots, and comparative charts
- **Statistical Testing:** Hypothesis testing for A/B test validation
- **Descriptive Statistics:** Comprehensive statistical summaries by version and retention status

## Technologies Used

- **Python 3** - Programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Static data visualization
- **Seaborn** - Statistical data visualization
- **Kagglehub** - Dataset loading from Kaggle
- **Jupyter Notebook** - Interactive development environment

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Required packages: pandas, numpy, matplotlib, seaborn, kagglehub

### Installation

1. Clone this repository
2. Install required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn kagglehub jupyter
   ```

3. Set up Kaggle API credentials for dataset access:
   - Visit https://www.kaggle.com/settings/account
   - Create an API token
   - Place the token in `~/.kaggle/kaggle.json`

### Usage

1. Open the Jupyter notebook:
   ```bash
   jupyter notebook AB_Testing.ipynb
   ```

2. Run the cells in order to:
   - Load the Cookie Cats dataset
   - Explore data structure and quality
   - Generate visualizations
   - Perform statistical analysis
   - Compare retention metrics between versions

## Analysis Sections

### 1. Data Loading
- Loads `cookie_cats.csv` from Kaggle using kagglehub
- Dataset contains 90,189 mobile game user records

### 2. Data Exploration
- Missing values check: No missing data
- Duplicate user ID check: No duplicates found
- DataFrame structure and shape: (90189, 5)
- Data types and memory usage

### 3. Descriptive Statistics
- **sum_gamerounds Statistics:**
  - Mean: 51.87 rounds
  - Median: 16 rounds
  - Std Dev: 195.05 rounds
  - Range: 0 to 49,854 rounds

### 4. Visualization
- Frequency distribution histogram of game rounds
- Boxplot showing distribution and outliers
- Segmented analysis by version and retention status

### 5. Segment Analysis

**Gate_30 + Retained after 1 day (n=20,034):**
- Mean rounds: 94.41
- Median rounds: 48
- Std Dev: 135.04

**Gate_40 + Retained after 1 day (n=20,119):**
- Mean rounds: 95.38
- Median rounds: 49
- Std Dev: 137.89

## Key Insights

1. **User Engagement:** Players who are retained show significantly higher engagement (94-95 average rounds) compared to overall average (51.87)

2. **Version Comparison:** Gate_30 and Gate_40 show similar engagement patterns for retained users, suggesting both gate placements have comparable impact on highly engaged users

3. **Distribution:** The data shows a right-skewed distribution with most players having lower round counts but some highly engaged outliers

4. **Data Quality:** High-quality dataset with no missing values or duplicates, suitable for reliable statistical analysis

## Test Methodology

The A/B testing framework includes:
- **Control Group:** Gate_30 placement
- **Treatment Group:** Gate_40 placement
- **Metrics:** User retention at 1-day and 7-day intervals
- **Engagement:** Number of game rounds played
- **Sample Size:** ~45,000 users per group

## Statistical Considerations

- Large sample size allows for robust statistical conclusions
- Retention as primary metric (binary classification)
- Game rounds as secondary metric (continuous variable)
- Proper stratification by version and retention status

## Visualizations Included

1. **Frequency Distribution Plot** - Player engagement distribution with xlim constraint
2. **Boxplot** - Outlier identification and distribution shape
3. **Segmented Statistics** - Comparative analysis by version and retention

## Notes

- Dataset is sourced from Kaggle's mobile games A/B testing collection
- Analysis focuses on understanding user retention and engagement patterns
- Results can inform game design decisions regarding feature gate placement
- The notebook is designed to run in Google Colab or local Jupyter environments

## Files in Repository

- `AB_Testing.ipynb` - Main analysis notebook (355 KB)
- `README.md` - This documentation

## Contributing

Contributions are welcome! Feel free to:
- Suggest additional statistical analyses
- Improve visualizations
- Add hypothesis testing frameworks
- Contribute new insights and findings

## License

This project is open source and available under the MIT License.

## References

- Kaggle Dataset: [Mobile Games A/B Testing](https://www.kaggle.com/datasets/yufengsui/mobile-games-ab-testing)
- A/B Testing Best Practices
- Statistical Hypothesis Testing

## Contact

For questions or suggestions, please reach out through GitHub Issues.
