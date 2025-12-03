# A/B Testing Analysis: Control vs Test Campaign

## Project Overview
This project performs a complete **A/B testing analysis** on a marketing campaign dataset, comparing a control group with a test (treatment) group. The aim is to evaluate which campaign performs better in terms of key metrics such as **Conversion Rate**, **Cost per Click**, **Cost per Purchase**, and **Click-through Rate**.

---

## Dataset
The dataset consists of two CSV files:
- `control_group.csv` : Control campaign data
- `test_group.csv` : Test campaign data

Each file contains the following columns:
- `Campaign Name`  
- `Date`  
- `Spend [USD]`  
- `# of Impressions`  
- `Reach`  
- `# of Website Clicks`  
- `# of Searches`  
- `# of View Content`  
- `# of Add to Cart`  
- `# of Purchase`  

---

## Data Processing
1. Loaded control and test datasets separately and combined them into a single DataFrame for easier analysis.  
2. Converted columns to **correct data types** (`numeric`, `datetime`).  
3. Calculated **derived metrics**:
   - **Conversion Rate (CR)** = Purchases / Website Clicks  
   - **Cost per Click (CPC)** = Spend / Website Clicks  
   - **Cost per Purchase (CPP)** = Spend / Purchases  
   - **Click-through Rate (CTR)** = Website Clicks / Impressions  

4. Handled missing values and divide-by-zero scenarios.

---

## Exploratory Data Analysis (EDA)
- Displayed dataset info and summary statistics (`.info()`, `.describe()`).  
- Visualized **daily trends** for each metric using **line plots**.  
- Compared **average metrics** between control and test groups using **bar charts**.  
- Checked for **outliers** using boxplots and ensured robust metrics.

---

## Statistical Analysis
### 1. Normality Test
- **Shapiro-Wilk test** was used to check if metrics are normally distributed.  
- Null hypothesis (H0): Data is normally distributed  
- p-value < 0.05 → reject H0 → not normal

### 2. Homogeneity of Variance
- **Levene’s test** used to check equal variances between control & test groups.  
- Null hypothesis (H0): Variances are equal  
- p-value < 0.05 → reject H0 → variances unequal

### 3. A/B Testing
- **T-test** (parametric) and **Mann-Whitney U test** (non-parametric) were performed.  
- Compared metrics between control and test groups to determine statistical significance.  
- Key results:
  - **Conversion Rate:** No significant difference  
  - **Cost per Click:** No significant difference  
  - **Cost per Purchase:** No significant difference  
  - **Click-through Rate:** Significant difference; test group performed better

---

## Conclusion
- The **test campaign** significantly outperformed the control campaign in terms of **Click-through Rate**.  
- Other metrics did not show statistically significant differences.  
- Recommendations for marketing strategy:
  - Focus on the test campaign for improving CTR  
  - Monitor other metrics and gather more data for stronger conclusions

---

## Tools & Libraries
- **Python 3**  
- **Pandas & NumPy**: Data manipulation  
- **Matplotlib & Seaborn**: Data visualization  
- **SciPy**: Statistical tests (Shapiro, Levene, T-test, Mann-Whitney)  

---

## Author
**Aamir Shahzad**

