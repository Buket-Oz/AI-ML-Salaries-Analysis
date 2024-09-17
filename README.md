# AI/ML Salary Analysis for 2020-2024

## Objective

This project aims to analyze global salary trends for AI/ML professionals between 2020 and 2024. Through exploratory data analysis, regression, clustering, and geospatial analysis, we uncover patterns related to job title, experience level, company size, and geographical location.

## Data

- **Source**: The dataset used in this project is sourced from [Kaggle: AI/ML Salaries](https://www.kaggle.com/datasets/cedricaubin/ai-ml-salaries).
- **Description**: The dataset includes salary data from 2020 to 2024, with over 10,000 records. It captures information such as job title, experience level, company size, salary in USD, work mode (on-site, hybrid, fully remote), and geographical details.
  
### Data Limitations:
- The dataset is heavily skewed toward full-time employees (99%) and the USA (over 8,000 entries), which may limit the generalizability of some findings.
- Self-reported salaries may introduce bias or inaccuracies, especially in terms of location-based salary expectations.
- Small companies are underrepresented, and there is limited data for non-full-time employment types.

## Tools and Libraries

- **pandas**: Data manipulation and analysis.
- **numpy**: Numerical computations.
- **seaborn**: Statistical data visualization.
- **matplotlib**: General data visualization.
- **scikit-learn**: For regression and clustering (used for linear regression, K-Means clustering).
- **statsmodels**: For advanced statistical analysis and regression models.

## Data Cleaning Process

### Initial Data
- The original dataset contains **18,057 rows** and **11 columns**.

### Missing Values
- **No missing values** were found in the dataset.

### Duplicates
- **7,380 duplicate rows** were identified and removed, reducing the dataset to **10,676 rows**.

### Mixed Data Types
- Each column was checked for mixed data types to ensure consistency.
- **Result**: No mixed data types were found.

### Data Type Conversion
- All object columns were converted to the **category** type to improve memory efficiency.

### Outliers Detection and Removal
- Upon inspection, outliers were identified where individuals were recorded with unusually high salaries (above $650,000). These entries were considered outliers and removed from the dataset.
- A separate dataset of individuals earning **above $650,000** was created and exported for further analysis.

### Dropped Columns
- The **salary** and **salary_currency** columns were dropped, as the dataset already includes salaries converted to USD in the **salary_in_usd** column.

### Further Outlier Removal for Specific Analysis
- For certain analyses, extreme salary values were removed again to provide a more balanced view of average salaries. This was particularly useful for **geographical analyses**, where removing outliers helped ensure a clearer comparison of salaries across different countries.

### Final Cleaned Dataset
- After the cleaning process, the final dataset contains **10,658 rows** and is ready for analysis.

### Subsetting for Regression Analysis
- Since the majority of the data comes from the **USA (84%)** and **Full-time employees (99%)**, a subset of the data was created for regression analysis using only full-time workers in the USA. Out of **10,658 rows**, **8,812 rows** were used for regression analysis, focusing on this key subset of the data.



## Key Questions and Answers

# a. Demographic Analysis:
1. **What are the salary trends across different experience levels (Entry, Mid, Senior, Executive)?**
Senior and executive roles consistently command the highest salaries, reflecting the demand for experienced professionals in the AI/ML industry.
However, the regression analysis explained only 12% of the variation, indicating that while experience plays a role, many other factors, such as company size and location, significantly influence salary.

2. **What are the most popular and hihest-paid job titles?**
   - The most popular job titles across all years are Data Scientist, Data Analyst, and Data Engineer.
   - In terms of compensation, Machine Learning roles, such as Head of Machine Learning and Machine Learning Manager, rank among the highest-paid positions in 2024.

3. **What are the most common job titles in the dataset?**
   - Data Scientist, Data Analyst, and Data Engineer are the most common job titles.
  
4. **How does company size affect salary?**
Medium and large companies offer higher salaries, but there is significant salary variation within each group.
The data reveals that medium and large companies dominate the dataset, with limited data available for smaller companies, making direct comparisons more challenging.
  
# b. Geographical Analysis:

**Which countries have the highest and lowest average salaries for AI/ML professionals?**
The top 10 countries in average salary for 2023-2024 include Japan, Egypt, New Zealand, the USA, Saudi Arabia, Canada, Australia, Israel, France, and the Czech Republic. 
However, it's important to note that the dataset contains limited data from most of these countries, with the USA being the only country with a substantial amount of data. 
Lower-paying countries include Turkey, Pakistan, India, Thailand, Malaysia, Slovenia, Portugal, Hungary, and several South American nations.
Further analysis should consider the cost of living index to adjust salary comparisons across countries, as this can provide a more accurate reflection of real purchasing power in different regions.

# c. Temporal Analysis:
**How have salaries in certain roles evolved over the years (2020-2024)?**
Salaries for roles like Machine Learning Engineer and Data Engineer have generally increased over time, while some roles, such as Data Analyst, have seen a slight decrease in 2024 compared to previous years.

**Are there any notable trends in the remote work ratio over time?**
The proportion of remote work increased significantly during the COVID-19 pandemic but has since declined, with 2024 showing fewer remote roles than 2023. This may reflect a shift back towards on-site or hybrid work arrangements in the post-pandemic era.

**Are there any notable trends in the job titles over time?**
The demand for machine learning roles has surged in recent years, particularly in 2024, where machine learning-related roles dominate the top of the salary rankings.

## Insights and Recommendations

- **Salary Benchmarking**: Companies can use this analysis to benchmark salaries based on experience level, company size, and geographical location to remain competitive.
- **Recruitment and Forecasting**: The analysis highlights the demand for machine learning roles and the higher salaries they command, making them key focus areas for recruitment strategies.

## Tableau Dashboard

The full Tableau dashboard with interactive visualizations can be accessed [here](https://public.tableau.com/app/profile/buket.oztekin/viz/AIMLSalariesAnalysis/AIMLSalariesStoryboard).

## Resources and Project Structure

The repository is structured as follows:

- **01 Project Management**: Contains the project brief and overview.
- **02 Data**: Divided into 'Original Data' and 'Prepared Data'.
- **03 Scripts**: Contains the Jupyter notebooks with the project code, including data cleaning, analysis, and visualizations.
- **04 Analysis**: Includes visualizations.
- **05 Sent to Client**: Contains the final deliverables, including the Tableau Dashboard.

---

