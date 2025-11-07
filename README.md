<h1>EDA</h1>

1.  **Data Inspection and Structure:**
    * Load the dataset and check its dimensions (rows, columns).
    * Examine the first few rows (`df.head()`).
    * Verify column names and data types (`df.info()`).

2.  **Missing Value Analysis:**
    * Calculate the count and **percentage of missing values** for every column.
    * Decide on a handling strategy (imputation, creation of 'Missing' category, or dropping the column).

3.  **Data Cleaning:**
    * Identify and remove **duplicate rows**.
    * Address data type inconsistencies (e.g., converting 'object' dates to `datetime`).

4.  **Univariate Analysis (Single Features):**
    * **Numerical:** Compute descriptive statistics (`df.describe()`). Visualize distributions using **Histograms** or KDE plots to check for **skewness**. Use **Box Plots** to detect **outliers**.
    * **Categorical:** Compute frequency counts (`value_counts()`). Visualize with **Bar Charts** and check for **imbalance** and **high cardinality**.

5.  **Bivariate and Multivariate Analysis (Relationships):**
    * **Numerical-Numerical:** Calculate and visualize the **Correlation Matrix** using a **Heatmap** to identify multicollinearity.
    * **Categorical-Numerical (Target):** Use **Box Plots** or **ANOVA** to assess how the numerical target's distribution changes across categories.
    * **Feature-Target Correlation:** Analyze how each feature relates to the target variable $Y$.

6.  **Feature Engineering and Transformation Decisions:**
    * Apply domain knowledge to **create new features** or combine existing ones.
    * Decide on the final plan for **Imputation** (median/mode), **Encoding** (One-Hot/Ordinal), and **Scaling** (Standard/MinMax) based on the findings, typically set up in a `ColumnTransformer`.
