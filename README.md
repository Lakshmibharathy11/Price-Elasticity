### Price Elasticity Prediction Project Report

#### 1. **Introduction**

The objective of this project was to predict price elasticity for various Stock Keeping Units (SKUs) using linear regression. Price elasticity is a measure of how sensitive the quantity demanded of a product is to a change in its price. The dataset used for this analysis was obtained from Kaggle and contained information on SKUs, prices, and sales data. The project involved performing basic data cleaning, filtering SKUs with good price variation, and then applying a linear regression model to predict price elasticity.

#### 2. **Data Preprocessing and Cleaning**

The first step in this project was to clean and preprocess the scanner dataset. This involved:

- **Removing Missing Values**: Any missing or incomplete data was removed to ensure the accuracy of the regression analysis.
- **Filtering Relevant SKUs**: We focused on SKUs with good price variation. This was done by calculating the price variability across the dataset and filtering out the SKUs that showed insufficient variation in their pricing.
  
After cleaning the data, the focus shifted to predicting price elasticity for the selected SKUs.

#### 3. **Linear Regression Model**

The linear regression model was implemented using Python in a Jupyter notebook. The process was as follows:

1. **Single SKU Analysis (SKU EGB8E)**:
   Initially, the linear regression model was applied to SKU "EGB8E" to check the performance and assess the suitability of the model. The results were promising, with an R-squared value of 0.56, indicating a moderate fit of the model to the data. The p-value for the regression coefficients was less than 0.05, suggesting that the model's parameters were statistically significant.

2. **Regression for All SKUs**:
   After the initial analysis, the linear regression model was extended to all SKUs in the dataset. Each SKU showed different R-squared and p-values. The p-value for each regression indicated whether the relationship between price and sales was statistically significant. The R-squared values varied, with some SKUs showing stronger relationships than others.

3. **Filtering Top 10 SKUs**:
   To ensure the analysis focused on the most relevant SKUs, we applied filters based on p-values and R-squared. The filtering criteria were:
   - **P-value < 0.05**: Ensured that the regression results were statistically significant.
   - **R-squared > 0.04**: Ensured that there was a reasonable fit between price and sales for the SKU.

   After filtering, the top 10 SKUs with the best price variation and statistically significant relationships were selected for further analysis.

#### 4. **Exporting Results for Power BI Dashboard**

To visualize and present the results, the linear regression parameters for each SKU were exported to a CSV file. This included the coefficients, p-values, and R-squared values. The final cleaned dataset was also exported in CSV format.

These CSV files were then uploaded into Power BI to create a dynamic dashboard.

#### 5. **Power BI Dashboard**

The Power BI dashboard was created to visualize the results of the linear regression model. Key steps included:

- **Data Import**: The exported CSV files were imported into Power BI.
- **DAX Formulas**: Data Analysis Expressions (DAX) formulas were used to apply the linear regression model to the data within Power BI. This enabled dynamic calculations of price elasticity and provided real-time insights based on the regression coefficients and p-values.
- **Visualization**: The dashboard included various visual elements, such as:
  - A bar chart displaying the top 10 SKUs with the highest price elasticity.
  - A scatter plot to show the relationship between price and sales for each SKU.
  - A table with detailed regression results, including p-values, R-squared values, and regression coefficients.

#### 6. **Results**

The analysis yielded the following results:

- **SKU EGB8E** showed a strong relationship between price and sales, with an R-squared of 0.56. This indicates that approximately 56% of the variation in sales can be explained by the price changes for this SKU.
- **Top 10 SKUs** were selected based on statistical significance and R-squared values. These SKUs had a strong price-demand relationship, making them ideal candidates for further pricing and elasticity analysis.

#### 7. **Conclusion**

This project successfully predicted price elasticity for various SKUs using linear regression. The use of Python for data preprocessing and Power BI for visualization provided an effective workflow for analyzing and presenting the results. The filtered top 10 SKUs with strong price elasticity can now be used to make data-driven pricing decisions, which can ultimately optimize revenue and improve sales strategies.

#### 8. **Future Work**

In the future, this analysis can be expanded by:
- Implementing more advanced machine learning models for price elasticity prediction.
- Including additional variables (e.g., competitor pricing, promotional discounts) in the model to enhance its predictive power.
- Automating the process of SKU selection and filtering based on dynamic changes in the dataset.
