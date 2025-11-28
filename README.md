# Amazon Sales Data Analysis and Rating Prediction

This repository contains a comprehensive exploratory data analysis (EDA) and machine learning project focused on Amazon sales data. The goal of this project was to go beyond simple visualizations and apply rigorous statistical testing to understand what truly drives customer satisfaction and product ratings in the e-commerce space.

The analysis answers key business questions regarding pricing strategies, the impact of discounts on perceived quality, and the relationship between review sentiment and numerical ratings.

## Project Overview

Using a dataset of over 1,400 Amazon products (predominantly electronics and accessories), I conducted a detailed analysis to identify patterns in sales and customer feedback. The project is structured into three main phases: data cleaning, statistical hypothesis testing, and predictive modeling.

## Methodology

### 1. Data Cleaning and Preparation
The raw dataset required significant preprocessing to be usable for analysis:
- Removed currency symbols and percentage signs to convert price and discount columns into floating-point numbers.
- Handled missing values in ratings and review counts using median imputation to maintain distribution integrity.
- Extracted main categories and sub-categories from hierarchical string data.

### 2. Statistical Analysis
I used several statistical tests to validate assumptions and find significant relationships, rather than relying solely on visual interpretation:
- **Shapiro-Wilk Test:** Confirmed that key variables (Price, Rating, Discount) do not follow a normal distribution.
- **Kruskal-Wallis Test:** Used to determine that there are statistically significant differences in ratings between different product categories and price segments.
- **Spearman Correlation:** Selected over Pearson due to the non-normal distribution of data. This revealed a statistically significant negative correlation between discount percentage and product rating.

### 3. Machine Learning & Predictive Modeling
To predict product ratings based on available features, I implemented and compared three regression models:
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor

After evaluating performance using R-squared and RMSE metrics, the **Random Forest Regressor** proved to be the most effective model. I further optimized it using GridSearchCV for hyperparameter tuning (optimizing `n_estimators`, `max_depth`, and `min_samples_split`).

## Key Business Insights

The analysis yielded several actionable insights for sales strategy:

* **The Discount Paradox:** Contrary to the expectation that lower prices yield happier customers, there is a weak negative correlation between discount percentage and ratings. Heavily discounted products tend to receive lower ratings, potentially due to quality issues or "too good to be true" customer expectations.
* **Engagement Drivers:** The strongest predictors for a product's rating are not its price, but the volume of reviews (`rating_count`) and the sentiment of the review text.
* **Category Performance:** Niche categories like "Office Products" outperform broader categories like "Home & Kitchen" in average customer satisfaction.
* **Price Segments:** Products in the "Luxury" price segment show more consistent and higher ratings compared to "Budget" items.

## Technologies Used

* **Python** (Data Analysis & Modeling)
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Visualization)
* **SciPy** (Statistical Testing)
* **TextBlob** (Sentiment Analysis / NLP)
* **Scikit-learn** (Machine Learning & Grid Search)

## How to Run

1.  Clone the repository.
2.  Install the required dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy textblob scikit-learn wordcloud
    ```
3.  Run the Jupyter Notebook or the Python script to reproduce the analysis and visualizations.

---

**Author:** Mert Can Akdogan
*Sales Analytics & Data Analysis*
