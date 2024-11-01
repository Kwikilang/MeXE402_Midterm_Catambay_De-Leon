# Methodology

## Step 1: Data Acquisition
The dataset was obtained from the World Happiness Report and loaded into a Pandas DataFrame from a provided Google Drive link.

## Step 2: Data Exploration
The first five rows of the dataset were displayed using `data.head(5)` to understand its structure and contents.

## Step 3: Data Cleaning

- **Handling Missing Values:** Rows with missing values were removed using `data.dropna(inplace=True)`.
- **Outlier Detection:** Numeric columns were selected to identify outliers. The Interquartile Range (IQR) was calculated to find and remove outliers:
  - Q1 = 25th percentile
  - Q3 = 75th percentile
  - Outliers were defined as values below `Q1 - 1.5 * IQR` or above `Q3 + 1.5 * IQR`.

## Step 4: Data Normalization
Numeric columns were normalized using `StandardScaler` to bring all features to the same scale.

## Step 5: Defining Variables

- **Independent Variables (X):** Features included:
  - Economy (GDP per Capita)
  - Family
  - Health (Life Expectancy)
  - Freedom
  - Generosity
  - Trust (Government Corruption)
- **Dependent Variable (y):** The target variable was Happiness Score.

## Step 6: Data Splitting
The dataset was split into training (80%) and testing (20%) sets using `train_test_split`.

## Step 7: Model Development
A Linear Regression model was instantiated using `LinearRegression()` from Scikit-Learn and trained on the training data.

## Step 8: Prediction and Evaluation
Predictions were made on the test set using the trained model. Model performance was evaluated using:
  - Mean Squared Error (MSE)
  - R-squared (R²)
  - Adjusted R-squared (adjusted for the number of predictors).

## Step 9: Coefficient Analysis
Coefficients of the model were extracted and displayed to assess the influence of each predictor.

## Step 10: Visualization
A scatter plot of actual vs. predicted happiness scores was created to visually assess model performance.

# Results

## Summary of Findings

### Model Performance Metrics:
- **Mean Squared Error (MSE):** A measure of the average squared difference between actual and predicted happiness scores.
- **R-squared (R²):** Indicates the proportion of variance in happiness scores explained by the model.
- **Adjusted R-squared:** Adjusted for the number of predictors in the model.

| Metric                 | Value              |
|------------------------|--------------------|
| Mean Squared Error     | 0.21559633639006698 |
| R-squared              | 0.7536856181426417  |
| Adjusted R-squared     | 0.6759021291350549  |

### Coefficient Analysis:
The coefficients for each predictor variable were presented in a table, indicating the strength and direction of their relationship with the happiness score.

| Predictor                   | Coefficient |
|-----------------------------|-------------|
| Economy (GDP per Capita)    | 0.249006    |
| Family                      | 0.313336    |
| Health (Life Expectancy)    | 0.344104    |
| Freedom                     | 0.151745    |
| Generosity                  | 0.102022    |
| Trust (Government Corruption) | 0.104049 |

### Visual Representation:
A scatter plot showing the relationship between actual and predicted happiness scores.

# Discussion

## Reflection on Results
The linear regression model provided insights into how socioeconomic factors influence happiness. The positive coefficients for predictors like GDP per capita, family support, and health suggest that these factors play a significant role in increasing happiness levels.

The R-squared value indicates a strong correlation between the predictors and the happiness score, suggesting that the model explains a substantial portion of the variance in happiness across different countries.

## Comparison of Regression Methods
While this analysis used linear regression, it is also essential to consider alternative methods, such as:
- **Logistic Regression:** Suitable for binary outcomes (e.g., happy/unhappy) rather than continuous scores.
- **Polynomial Regression:** Could capture non-linear relationships among variables.

The choice of method depends on the specific research question and data characteristics.

## Limitations

### Assumptions of Linear Regression
The model assumes a linear relationship between the predictors and the dependent variable, which may not always hold true.

### Potential Multicollinearity
There may be correlation between independent variables, which could distort coefficient estimates and interpretations.

### Outliers
While outliers were removed, their influence may still linger if not addressed properly.

### External Factors
The model does not account for unobserved variables or external factors that could influence happiness, such as political stability or cultural differences.

# Conclusion
The analysis effectively demonstrated the significance of economic and social factors in determining happiness levels across different countries. By using linear regression, the study provided valuable insights that could inform policies aimed at improving well-being. Future work could explore advanced modeling techniques and a broader range of factors to enhance the understanding of happiness determinants.
