# Vintage Insights: Harnessing Machine Learning to Predict Wine Sales & Quality

## **Project Overview**

This project focuses on preparing and analyzing a dataset of wine sales and quality, ultimately transforming raw data into a refined format ready for predictive modeling. The goal is to understand how various factors like alcohol content, residual sugar, and other features influence the wine's sales performance. By addressing data quality issues like missing values, outliers, and skewed distributions, the dataset is made suitable for building a robust machine learning model.

## **Business Case**

Wine sales are influenced by numerous factors such as quality, region, grape variety, and production methods. Understanding these variables helps businesses make data-driven decisions for inventory management, marketing strategies, and predicting future sales. The business case here is to predict wine sales quality based on available features to optimize marketing campaigns, reduce waste, and forecast demand.

## **Steps Taken to Solve the Problem**

### 1. **Initial Data Exploration**
   - **Identify Missing Values**: The dataset was first checked for missing values, which included attributes like "ResidualSugar," "Chlorides," and "FreeSulfurDioxide." **"STARS"** had a significant number of missing values, which required further attention.
   - **Outlier Detection**: Potential outliers were identified using standard statistical methods (z-scores).
   - **Skewness Assessment**: The distributions of key variables, such as Alcohol, ResidualSugar, and STARS, were examined to detect skewness.

### 2. **Data Cleaning & Preparation**
   - **Handling Missing Values**: The missing values were addressed by imputation (for most columns) or exclusion, particularly for **"STARS,"** which had 3359 missing values.
   - **Outlier Treatment**: Outliers were detected and removed, ensuring they didn’t distort subsequent analyses.
   - **Normalization**: Several features, such as ResidualSugar, were transformed using mathematical techniques (Log and Box-Cox transformations) to better fit machine learning assumptions and ensure feature scaling.
   - **Feature Engineering**: New variables were created (like `Log_ResidualSugar` and `BoxCox_STARS`), and unnecessary columns were dropped to enhance model relevance and interpretability.

### 3. **Exploratory Data Analysis (EDA) Post-Preparation**
   - **Correlation Analysis**: After data adjustments, correlations between key variables were assessed to identify the most impactful features for the target variable (wine sales).
   - **Data Visualization**: Pairplots, histograms, and heatmaps were generated to visualize relationships between features and better understand the impact of transformations.
   - **Distribution of Key Variables**: The transformed data distributions showed normalized trends in features like ResidualSugar and STARS, improving the data's fitness for modeling.

### 4. **Comparison of Pre- and Post-Preparation Analysis**
   - **Correlation Insights**: The pre- and post-transformation correlation matrices revealed shifts in relationships between variables, particularly a positive correlation between **BoxCox_STARS** and **TARGET** after transformation, compared to a negative correlation in the original data.
   - **Data Normalization**: Post-transformation data (like **Log_ResidualSugar**) showed more symmetrical distributions, which are better suited for modeling.

### 5. **Final Adjustments for Machine Learning**
   - The dataset was adjusted for machine learning by normalizing distributions, handling missing values, and introducing new variables, creating a refined version that minimizes potential data quality issues and is ready for predictive modeling.

## **Business Recommendations**

1. **Targeted Marketing Based on Key Variables**: Based on the feature transformations and correlations, businesses can target specific wine types that are most likely to perform well in certain markets. For instance, wines with moderate levels of residual sugar or higher alcohol content might perform better, depending on regional preferences.
   
2. **Quality Control Focus**: By focusing on features like **BoxCox_STARS** and **Alcohol**, companies can monitor wine production processes more closely and focus on producing wines that align with customer preferences.

3. **Optimize Inventory Management**: Predictive models trained on this prepared dataset can help forecast future demand, enabling better inventory management and reducing both overstock and understock situations.

4. **Enhancing Predictive Models**: With the current dataset now ready, further feature engineering or external data (such as regional preferences or economic factors) could further enhance prediction accuracy.

## **Key Recommendations for Future Work**
- **Model Training**: With the refined dataset, you can proceed with model selection, including linear regression, random forests, or gradient boosting methods to predict wine sales based on the cleaned data.
- **Cross-Validation**: Ensure that model performance is validated through cross-validation techniques to minimize overfitting and assess generalization.
- **Fine-Tuning Hyperparameters**: Use grid search or random search methods to find the optimal hyperparameters for the model, further improving prediction accuracy.

## **Conclusion**

The dataset has been thoroughly explored, cleaned, and transformed into a suitable format for machine learning tasks. By addressing missing values, outliers, and skewed distributions, the data is now ready for predictive modeling. The refined dataset provides valuable insights into key factors influencing wine quality and sales, offering businesses a data-driven approach to enhance marketing, inventory management, and demand forecasting strategies.
