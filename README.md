# CMSC320 - Introduction to Data Science

Welcome to my repository for ```CMSC320 - Introduction to Data Science``` at the ```University of Maryland, College Park```. This repository includes a summary and the grade received for the homeworks and projects that I completed throughout this course. Due to university policies, the code for these projects is not publicly available. If you are an employer or have a legitimate request to view the code, please contact me directly.

## Assignments 

### Homework 1: **Pandas & SQL**
**Description:**  
This assignment focused on exploring and analyzing datasets using Pandas and SQL. Key topics covered include:
- Reading and manipulating datasets with **Pandas** (`read_csv`, filtering, grouping, replacing values).
- Performing exploratory data analysis (EDA) with descriptive statistics and visualization (`hist`, `median`, `value_counts`).
- Writing **SQL queries** to extract insights from databases (`JOIN`, `GROUP BY`, `ORDER BY`, `AVG`).
- Cleaning and transforming data, including handling missing values and removing unwanted text.
- Running queries in **pandas with SQLite** to analyze real-world datasets.

**Grade:** 
- Pandas: 99/100
  - On Question 10, I mistakenly did not print the head of the dataframe after removing the URL scheme/protocol.
- SQL: 100/100

---

### Homework 2: **Data Exploration**  
**Description:**  
- Analyzed survey data from 473 students to investigate the relationship between **religiosity** and moral judgments using Python (`pandas`, `matplotlib`, `seaborn`, `scipy`).  
- **Key Tasks**:  
  - **Data Cleaning**:  
    - Merged datasets from 4 classes (2023–2025) with varying question phrasing.  
    - Handled missing data (3.28\%) via mode imputation and age outlier removal (17–30 range).  
    - Standardized categorical variables (e.g., "Famale" → "Female", ordinal encoding for responses).  
  - **Statistical Analysis**:  
    - Applied **Kruskal-Wallis tests** (Bonferroni-corrected $\alpha = 0.00357$) to 14 moral dilemmas.  
    - Identified 2 significant questions (Q7: family duty, Q12: LGBTQ donation) with $p < 0.001$.  
    - Performed **post-hoc Dunn tests** to pinpoint differences between religiosity groups.  
  - **Visualization**:  
    - Created stacked bar charts to show response distributions by religiosity (`Matplotlib`/`Seaborn`).  
    - Highlighted ideological divides: non-religious groups favored autonomy/progressivism, religious groups prioritized tradition.  
  - **Interpretation**:  
    - Linked statistical results to broader societal values (e.g., family unity vs. individual rights).  
**Code Features**:  
- Modular functions for data loading (`load_and_fix_data`), cleaning (`clean_data`), and analysis (`run_kruskal_with_bonferroni`).  
- Automated visualization pipeline (`plot_question`) with publication-ready formatting.  

**Grade**: 

---

### Homework 3: **Data Exploration Pt. 2**
**Description:**  
- Extended analysis of moral judgment surveys with additional focus on **demographic correlations** and **experimental biases**.  
- **Key Tasks**:  
  - **Data Integration**:  
    - Merged datasets from 4 classes (2023–2025) while handling inconsistencies (e.g., priming questions, gender-swapped dilemmas).  
    - Binned survey timestamps into "Morning", "Afternoon", "Evening", and "Night" categories.  
  - **Political Belief Analysis**:  
    - Visualized alignment between student/parent political views using **dual heatmaps** (Matplotlib/Seaborn).  
    - Found 38.3% of students identified as "Mildly liberal" vs. 2.4% "Strongly conservative".  
  - **Experimental Bias Testing**:  
    - **Priming Effect**: Used **chi-squared tests** (Bonferroni-corrected) to show *no significant impact* of compassion priming on responses.  
    - **Gender Swap**: Analyzed gender-reversed dilemmas (Q1/Q3) and found *no statistically significant differences* in judgments.  
  - **Advanced Statistical Testing**:  
    - Re-ran **Kruskal-Wallis tests** to confirm religiosity’s strong influence on Q7 (family duty) and Q12 (LGBTQ donation).  
    - Tested for differences between **graduate/undergraduate students** and **time-of-day responses** – *no significant effects found*.  

**Code Features**:  
- Chi-squared contingency table generation, and automated statistical testing.  
- Dynamic heatmap visualization for political belief comparisons (`plot_political_comparison`).  

**Grade**: 

---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
