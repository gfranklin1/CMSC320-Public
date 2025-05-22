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

**Grade**: 50/50

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

**Grade**: 32/32

---

### Homework 4: **Machine Learning Project**  
**Description:**  
- Built models to predict **professor ratings** on **PlanetTerp** using **indirect features** (not actual ratings).  
- **Key Tasks**:  
  - **Data Gathering**:  
    - Collected professor, review, and grade data via **PlanetTerp API**.  
    - Merged professor review texts, grade distributions, and course data for 805 professors.  
  - **Feature Engineering**:  
    - Extracted **sentiment features** using **BERT sentiment analysis** (`bert_mean`, `bert_std`, etc.).  
    - Calculated **word count statistics** from reviews (`wc_mean`, `wc_std`).  
    - Created **grade-based features** (e.g., percentage of As, Bs, GPA average).  
    - Applied **TF-IDF vectorization** and **Truncated SVD** for textual review embeddings (20 components).  
  - **Exploratory Data Analysis**:  
    - Visualized review counts, professor rating distributions, and grade distributions.  
    - Generated **word clouds** for positive and negative sentiment vocabularies.  
  - **Modeling**:  
    - Trained and tuned 3 models:
      - **K-Nearest Neighbors (KNN)**  
      - **Random Forest (RF)**  
      - **Gradient Boosting (GB)**  
    - **Hyperparameter tuning** via **GridSearchCV** (10-fold cross-validation).  
  - **Model Evaluation**:  
    - Evaluated with **MSE** and **$R^2$** on test data.  
    - Best Model: **Random Forest** with test $R^2 = 0.902$.  
  - **Visualization**:  
    - Created scatter plots of predicted vs. actual ratings for all models.  
    - Compared models’ MSE and $R^2$ using barplots made using **Seaborn**.

**Code Features**:  
- Modularized feature creation for sentiment, grades, word counts, and TF-IDF embeddings.  
- Robust API handling with concurrency for data retrieval.  
- Clear modeling pipeline with hyperparameter optimization and scaling for KNN.  
- Visualization tailored for presentation.  

**Grade**: 125/100
- 25 points of extra credit

---

### Homework 5: **Image Classification Project**
**Description:**
- Investigated how external environmental and emotional factors influence student attendance in Professor Morawski’s Spring 2025 CMSC320 class.
- **Key Tasks**:
  - **Data Integration**:
    - Combined attendance records from two class sections (202 and 69 students) with **weather data** (OpenMeteo API), **Spotify top songs** (Kaggle), and **moon illumination** (World Weather Repository).
    - Extracted features: daily precipitation, wind speed, temperature, Spotify valence/energy scores, moon phase and illumination, and days until the next exam.
  - **Time Series Analysis**:
    - Applied **Augmented Dickey-Fuller test** to assess stationarity.
    - Performed **STL decomposition** to separate attendance into trend, seasonal, and residual components.
    - Fit **SARIMA and SARIMAX** models to forecast future attendance and evaluate predictors.
    - Forecast showed normalized attendance would hit near-zero levels by **May 19, 2025** (after the semester).
  - **Statistical Modeling**:
    - Modeled attendance against weather and lunar factors using **SARIMAX** and **OLS regression**.
    - Weather and music mood were statistically insignificant (p > 0.7).
    - **Moon illumination initially had a p = 0.047**, but varying tests and a low \$R^2\$ of 0.05 suggested it was a likely false positive.
   
**Code Features**:
- STL decomposition and SARIMA forecasting pipeline using `statsmodels`.
- Multi-source data merging and feature engineering (`pandas`, `numpy`).
- Statistical testing and model diagnostics (ADF, \$R^2\$, p-values).
- Visualizations using `Seaborn` and `Matplotlib`.

**Grade**: 110/100
- 10 points of extra credit

---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
