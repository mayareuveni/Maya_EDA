# Supermarket Sales Data Analysis (EDA)

## Project Overview
This project presents a comprehensive Exploratory Data Analysis (EDA) of a supermarket chain dataset, encompassing 1,000 transactions across 3 distinct branches. The primary objective is to decode consumer behavior, analyze purchasing patterns, and identify the store's core growth engines using statistical and data science methodologies.

---

## Tools & Technologies Used
* Language: Python
* Environment: Jupyter Notebook / Google Colab
* Libraries:
  * pandas (Data manipulation and analysis)
  * numpy (Numerical computing)
  * matplotlib.pyplot (Data visualization)
  * seaborn (Statistical data visualization)
  * scipy.stats (Hypothesis testing and statistical functions)

---

## Dataset Information
* Source File: supermarket_sales.csv
* Dimensions: 1,000 rows x 17 columns
* Key Features Analyzed: invoice_id, branch, customer_type, gender_customer, product_line, unit_cost, quantity, revenue, date, payment_method, rating.

---

## Project Structure & Methodology
The analysis follows a structured, step-by-step Data Science workflow:

1. Data Loading & Initial Inspection: Understanding the DataFrame structure, data types, and base metrics.
2. Data Cleaning & Validation: Verifying the integrity of the data. The dataset was found to contain zero missing values and zero duplicate records.
3. Cardinality & Variance Analysis: Evaluating the uniqueness of columns. Identified and explained the redundancy of zero-variance columns (e.g., gross margin percentage).
4. Univariate Analysis:
   * Numerical: Analyzed the central tendencies and positive skewness of the 'revenue' variable. Conducted a comparative Outlier Detection analysis using three distinct methods (3-STD, 3-MAD, 1.5-IQR).
   * Categorical: Examined the 'product_line' distribution, calculating frequencies and establishing the required categories to cover 80% of the data.
5. Correlations & Relationships (Bivariate Analysis):
   * Numerical-Numerical: Investigated the linear relationship between 'unit_cost' and 'revenue' comparing Pearson, Spearman, and Kendall correlation coefficients.
   * Categorical-Categorical: Applied continuous variable discretization (Binning) and calculated Cramér's V to test the association between membership status and total expenditure.
6. Data Visualization Dashboard: Generated a comprehensive suite of charts (Scatterplots, Histograms, Barcharts, Boxplots, Violin Plots, Piecharts, Pairplots, and Heatmaps) to extract visual business intelligence.
7. Index Analysis: Evaluated the properties of the default Pandas RangeIndex and discussed its implications.
8. Insights & Data Storytelling: Summarized the findings into actionable business conclusions and highlighted potential biases within the dataset.
9. Advanced Investigation (Bonus): 
   * Feature Engineering: Extracted 'day_of_week' and 'is_weekend' features from the raw date column to analyze time dependence.
   * Hypothesis Testing: Conducted an Independent Two-Sample T-Test to statistically validate the difference in spending between Members and Normal customers.

---

## Key Business Insights
1. Ineffective Loyalty Program: Statistical testing (Cramér's V = 0 and T-Test P-value = 0.534) proved there is no significant difference in spending habits between Members and Normal customers. The loyalty program fails at upselling.
2. Balanced Payment Preferences: The market share of payment methods is split almost equally into thirds (Ewallet: 34.5%, Cash: 34.4%, Credit card: 31.1%), indicating high adoption of digital payments alongside traditional cash.
3. Uniform Department Sales: Revenue is distributed almost entirely uniformly across all 6 product departments and between genders, meaning no single demographic or product line disproportionately drives the store's success.
4. Weekend Purchasing Peaks: Engineered temporal features revealed that weekend days (Saturday and Sunday) consistently yield the highest average transaction revenue.

---

## Data Risks & Limitations
* Time/Selection Bias: The dataset is limited to a 3-month window (January to March 2019). This ignores critical retail seasonality (e.g., holidays, summer breaks) and limits the ability to forecast long-term annual trends.
* Lack of Variance: The complete absence of missing values, returns, or data entry errors suggests the dataset is highly curated or synthetic, lacking the typical noise found in real-world retail data environments.

---

## Instructions for Execution
1. Ensure the 'supermarket_sales.csv' dataset is located in the same directory as the notebook file.
2. Install the required dependencies (pandas, numpy, matplotlib, seaborn, scipy).
3. Run the notebook cells sequentially from top to bottom to reproduce the analysis and visualizations.
