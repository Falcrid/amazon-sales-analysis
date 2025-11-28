# Amazon Sales Dataset Analysis

## Project Overview
Comprehensive Exploratory Data Analysis, Sentiment Analysis, and Machine Learning project analyzing 1,465 Amazon products across 9 categories. This project demonstrates end-to-end data science workflow from data cleaning to predictive modeling.

## Dataset
- Source: [Kaggle - Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset)
- Products: 1,465
- Categories: 9
- Brands: 437

## Technologies Used
- Python (Pandas, NumPy)
- Data Visualization (Matplotlib, Seaborn)
- Natural Language Processing (TextBlob, WordCloud)
- Machine Learning (Scikit-learn)

## Analysis Performed

### 1. Exploratory Data Analysis
- Rating distribution analysis
- Category-wise product distribution
- Price segmentation (Budget, Mid-Range, Premium, Luxury)

### 2. Brand Analysis
- Top 15 brands by product count
- Brand performance comparison (rating, reviews, discount)

### 3. Sentiment Analysis
- Review sentiment extraction using TextBlob
- Sentiment-Rating correlation analysis
- Word Cloud visualization of common review terms

### 4. Machine Learning
- Models: Linear Regression, Random Forest
- Target: Product Rating prediction
- Features: Price, Discount, Rating Count, Review Sentiment

## Key Findings

| Metric | Value |
|--------|-------|
| Average Discount | 47.7% |
| Average Rating | 4.10/5 |
| Average Sentiment | 0.268 (positive) |
| Best Model R² | 0.188 |

### Top Insights
- Review sentiment shows stronger correlation with rating (0.178) than discount rate (-0.155)
- Luxury products have highest average rating (4.18)
- Rating Count is the best predictor of product rating (29.0%)
- Review Sentiment is the second most important feature (27.1%)

### Brand Performance
- Highest rated brand: AmazonBasics (4.31)
- Most reviewed brand: Redmi (avg 72,249 reviews)
- Lowest discount brand: Redmi (25.7%) - premium positioning

## Model Performance

| Model | MAE | Test R² | CV R² (5-Fold) |
|-------|-----|---------|----------------|
| Linear Regression | 0.205 | 0.100 | 0.050 (+/- 0.117) |
| Random Forest | 0.181 | 0.188 | 0.106 (+/- 0.223) |

**Note:** Cross-validation provides more realistic performance estimates. The variance suggests rating prediction requires additional features (product descriptions, image quality, etc.) for higher accuracy.

## Feature Importance (Random Forest)
1. Rating Count: 29.0%
2. Review Sentiment: 27.1%
3. Discount Percentage: 15.2%
4. Actual Price: 14.7%
5. Discounted Price: 14.0%

## Business Recommendations
- High review count indicates reliable product rating
- Discount rate alone does not guarantee customer satisfaction
- Encourage customer reviews to build product credibility
- Focus on review sentiment for quality monitoring

## Files
- `amazon-sales-analysis.ipynb` - Complete Jupyter notebook with all analysis

## Author
Mert Can Akdogan - [LinkedIn](https://www.linkedin.com/in/mertcanakdogan/)
