# IBM SkillsBuild Summer Internship Project on Data Analytics

<div style="text-align: center;">
    <img src="https://cityandguildsfoundation.org/wp-content/uploads/2022/08/Skillsbuild-logo.jpg" alt="IBM SkillsBuild Logo" style="width: 200px; height: auto;">
</div>

## Project Title: Data Analytics and Visualization for Mental Health using ML

### Duration: 24th June 2024 - 5th August 2024

### Intern: Harsh Kumar Jha

---

## Understanding Mental Health

Mental health encompasses our emotional, psychological, and social well-being. It influences how we think, feel, and behave, and plays a crucial role in how we manage stress, relate to others, and make choices. Mental health is essential throughout all stages of life, from childhood and adolescence to adulthood.

### Importance of Mental Health

Mental health is vital for overall health and well-being. It affects our ability to lead fulfilling lives, maintain relationships, and cope with the stresses of life. The World Health Organization (WHO) emphasizes that mental health is not merely the absence of mental disorders; it is a state of well-being that enables individuals to realize their abilities, cope with the normal stresses of life, work productively, and contribute to their communities.

### Interconnection with Physical Health

Mental and physical health are deeply interconnected. Mental health conditions, such as depression and anxiety, can increase the risk of developing physical health issues, including chronic conditions like diabetes, heart disease, and stroke. Conversely, long-term physical health conditions can contribute to mental health challenges, creating a cycle that affects overall well-being.

### Factors Influencing Mental Health

Several factors contribute to mental health conditions, including:

- **Biological Factors:** Genetics and brain chemistry can predispose individuals to mental health issues.
- **Life Experiences:** Trauma, abuse, and significant life changes can impact mental health.
- **Social and Economic Factors:** Poverty, violence, and social inequality can increase the risk of developing mental health problems.

Understanding these factors is crucial for developing effective prevention and treatment strategies.

---

## Project Overview

This project, completed as part of the IBM SkillsBuild Summer Internship Program in collaboration with CSRBOX, focuses on leveraging data analytics techniques to extract valuable insights from a dataset related to mental health trends. The objective was to develop a comprehensive data analysis pipeline, including data preprocessing, exploratory data analysis (EDA), and visualization.

### Goals and Objectives

- **Analyze Mental Health Trends:** Utilize machine learning algorithms to identify patterns and trends in mental health data.
- **Data Visualization:** Create engaging visual representations of data to communicate findings effectively.
- **Impact Assessment:** Assess the implications of mental health trends on public health and well-being.

### Expected Outcomes

- **Insights into Mental Health:** Provide actionable insights that can inform mental health policies and interventions.
- **Enhanced Awareness:** Raise awareness about the importance of mental health and the factors influencing it through data-driven storytelling.

In conclusion, this project aims to contribute to the broader understanding of mental health issues and support efforts to improve mental health outcomes in communities.

---

## Table of Contents

- [Introduction](#introduction)
- [Dataset Description](#dataset-description)
- [Methodology](#methodology)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Key Insights](#key-insights)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)

---

## Introduction

In this project, I applied various data analytics techniques to analyze dataset which appears to contain a variety of features related to text analysis, sentiment analysis, and psychological indicators, likely derived from posts or text data. Some features include readability indices such as Automated Readability Index (ARI), Coleman Liau Index, and Flesch-Kincaid Grade Level, as well as sentiment analysis scores like sentiment compound, negative, neutral, and positive scores. Additionally, there are features related to psychological aspects such as economic stress, isolation, substance use, and domestic stress. The dataset seems to cover a wide range of linguistic, psychological, and behavioural attributes, potentially suitable for analyzing mental health-related topics in online communities or text data.The goal was to uncover trends, patterns, and correlations that could drive better decision-making for Mental health parameters.

---

## Dataset Description

The dataset used in this project was provided by [Dataset link](https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset). It contains [300k rows and 17 columns] and includes features such as [insert key features here].

**Sample Data Snapshot:**

| Timestamp           | Gender | Country       | Occupation | self_employed | family_history | treatment | Days_Indoors | Growing_Stress | Changes_Habits | Mental_Health_History | Mood_Swings | Coping_Struggles | Work_Interest | Social_Weakness | mental_health_interview | care_options |
|---------------------|--------|---------------|------------|---------------|----------------|-----------|--------------|----------------|----------------|-----------------------|-------------|------------------|---------------|-----------------|-------------------------|--------------|
| 8/27/2014 11:29     | Female | United States | Corporate  | No            | No             | Yes       | 1-14 days    | Yes            | No             | Yes                   | Medium      | No               | No            | Yes             | No                      | Not sure     |
| 8/27/2014 11:31     | Female | United States | Corporate  | No            | Yes            | Yes       | 1-14 days    | Yes            | No             | Yes                   | Medium      | No               | No            | Yes             | No                      | No           |
| 8/27/2014 11:32     | Female | United States | Corporate  | No            | Yes            | Yes       | 1-14 days    | Yes            | No             | Yes                   | Medium      | No               | No            | Yes             | No                      | Yes          |
| 8/27/2014 11:37     | Female | United States | Corporate  | No            | Yes            | Yes       | 1-14 days    | Yes            | No             | Yes                   | Medium      | No               | No            | Yes             | Maybe                   | Yes          |
| 8/27/2014 11:43     | Female | United States | Corporate  | No            | Yes            | Yes       | 1-14 days    | Yes            | No             | Yes                   | Medium      | No               | No            | Yes             | No                      | Yes          |


## Data Overview

This dataset contains a comprehensive overview of mental health aspects in different occupations. Below are some key statistics and information regarding the dataset:

### Dataset Information
The dataset contains 292,364 entries with the following columns:

| Column                   | Non-Null Count   | Dtype |
|--------------------------|------------------|-------|
| `Timestamp`              | 292,364 non-null | object|
| `Gender`                 | 292,364 non-null | object|
| `Country`                | 292,364 non-null | object|
| `Occupation`             | 292,364 non-null | object|
| `self_employed`          | 287,162 non-null | object|
| `family_history`         | 292,364 non-null | object|
| `treatment`              | 292,364 non-null | object|
| `Days_Indoors`           | 292,364 non-null | object|
| `Growing_Stress`         | 292,364 non-null | object|
| `Changes_Habits`         | 292,364 non-null | object|
| `Mental_Health_History`  | 292,364 non-null | object|
| `Mood_Swings`            | 292,364 non-null | object|
| `Coping_Struggles`       | 292,364 non-null | object|
| `Work_Interest`          | 292,364 non-null | object|
| `Social_Weakness`        | 292,364 non-null | object|
| `mental_health_interview`| 292,364 non-null | object|
| `care_options`           | 292,364 non-null | object|

**Note:** The column `self_employed` contains some missing values.
## Dataset Statistics

### Summary Statistics

The dataset contains 292,364 entries with the following statistics:

| Column                   | Count   | Unique | Top            | Frequency |
|--------------------------|---------|--------|----------------|-----------|
| `Timestamp`              | 292,364 | 580    | 8/27/2014 11:43 | 2,384     |
| `Gender`                 | 292,364 | 2      | Male           | 239,850   |
| `Country`                | 292,364 | 35     | United States  | 171,308   |
| `Occupation`             | 292,364 | 5      | Housewife      | 66,351    |
| `self_employed`          | 287,162 | 2      | No             | 257,994   |
| `family_history`         | 292,364 | 2      | No             | 176,832   |
| `treatment`              | 292,364 | 2      | Yes            | 147,606   |
| `Days_Indoors`           | 292,364 | 5      | 1-14 days      | 63,548    |
| `Growing_Stress`         | 292,364 | 3      | Maybe          | 99,985    |
| `Changes_Habits`         | 292,364 | 3      | Yes            | 109,523   |
| `Mental_Health_History`  | 292,364 | 3      | No             | 104,018   |
| `Mood_Swings`            | 292,364 | 3      | Medium         | 101,064   |
| `Coping_Struggles`       | 292,364 | 2      | No             | 154,328   |
| `Work_Interest`          | 292,364 | 3      | No             | 105,843   |
| `Social_Weakness`        | 292,364 | 3      | Maybe          | 103,393   |
| `mental_health_interview`| 292,364 | 3      | No             | 232,166   |
| `care_options`           | 292,364 | 3      | No             | 118,886   |

### Unique Values in Each Column

| Column                   | Unique Values |
|--------------------------|---------------|
| `Timestamp`              | 580           |
| `Gender`                 | 2             |
| `Country`                | 35            |
| `Occupation`             | 5             |
| `self_employed`          | 2             |
| `family_history`         | 2             |
| `treatment`              | 2             |
| `Days_Indoors`           | 5             |
| `Growing_Stress`         | 3             |
| `Changes_Habits`         | 3             |
| `Mental_Health_History`  | 3             |
| `Mood_Swings`            | 3             |
| `Coping_Struggles`       | 2             |
| `Work_Interest`          | 3             |
| `Social_Weakness`        | 3             |
| `mental_health_interview`| 3             |
| `care_options`           | 3             |

### Duplicate and Missing Values

- **Total number of observations:** 292,364
- **Unique number of observations:** 290,051
- **Number of duplicate observations:** 2,313

#### Missing Values

| Column                   | Missing Values |
|--------------------------|----------------|
| `Timestamp`              | 0              |
| `Gender`                 | 0              |
| `Country`                | 0              |
| `Occupation`             | 0              |
| `self_employed`          | 5,202          |
| `family_history`         | 0              |
| `treatment`              | 0              |
| `Days_Indoors`           | 0              |
| `Growing_Stress`         | 0              |
| `Changes_Habits`         | 0              |
| `Mental_Health_History`  | 0              |
| `Mood_Swings`            | 0              |
| `Coping_Struggles`       | 0              |
| `Work_Interest`          | 0              |
| `Social_Weakness`        | 0              |
| `mental_health_interview`| 0              |
| `care_options`           | 0              |

### Insights

- **Handling Duplicates:** Removed 2,313 duplicate entries to ensure data integrity and accuracy. This step is crucial for maintaining the quality of the dataset and preventing potential biases in the analysis.
  
- **Addressing Missing Values:** Replaced missing values in the `self_employed` column with the mode to maintain consistency and improve model performance. Handling missing data effectively helps in generating more reliable and robust predictive models.

---

## Methodology

1. **Data Preprocessing:**
    * Handling missing values
    * Data normalization and scaling
    * Feature engineering

2. **Exploratory Data Analysis (EDA):**
    * Understanding data distribution
    * Identifying correlations
    * Outlier detection

3. **Data Visualization:**
    * Bar charts, histograms, and box plots
    * Heatmaps and scatter plots
    * Interactive visualizations using Plotly and Seaborn

---

## Exploratory Data Analysis (EDA)

### 1. Distribution of Mental Health Survey Respondents by Country

![Distribution of Feature](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/1_Distribution_of_Mental_Health_Survey_Respondents_by_Country.png)

The distribution plot indicates a high concentration of survey respondents from the United States and the United Kingdom, accounting for approximately 70% of the dataset.

### 2. Gender Distribution

![Gender Distribution](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/2_Gender_Distribution_&_Count.png) 

The pie chart shows that about 82% of the respondents are male, highlighting a significant gender imbalance in the dataset.

### 3. Growing Stress by Gender and stress 

![Growing Stress by Gender](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/3_Stress_Levels.png) 

The bar chart depicts the growing stress levels categorized by gender, revealing differences in stress experiences across genders.This pie chart illustrates the distribution of responses regarding growing stress, with 34% indicating mental health issues, another 34% not experiencing issues, and the remaining respondents unsure.

### 4. Growing Stress by Days Indoors

![Growing Stress by Days Indoors](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/4_Stress_by_days_indoors.png)

The bar plot visualizes how days spent indoors correlate with growing stress, providing insights into the relationship between indoor activity and stress levels.

### 5. Growing Stress by Occupation

![Growing Stress by Occupation](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/5_Growing_Stress_by_Occupations.png)

This visualization shows the variation of growing stress across different occupations, aiding in understanding occupational stress factors.

### 7. Growing Stress by Work Interest

![Growing Stress by Work Interest](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/6_Stress_by_Work_Interest.png) 

The count plot examines the relationship between growing stress and work interest, showing how work-related stress impacts mental health.

### 7. Growing Stress by Changes in Habits

![Growing Stress by Changes in Habits](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/7_Stress_by_Changes_Habits.png)

This count plot reveals the impact of changes in habits on growing stress, offering insights into how lifestyle modifications affect mental health.

### 8. Family History and Treatment

![Family History and Treatment](hkjhacode/IBM-SkillsBuild-Internship-Project/Plots/8_Family_History_&_Treatment.png) 

The pie charts show that 39% of respondents have a family history of mental health issues, while 50% have sought treatment. This suggests that both genetic factors and treatment-seeking behavior play significant roles in mental health.

---

## Key Insights

1. **Insight 1:** The high concentration of respondents from the United States and the United Kingdom suggests a potential bias in the dataset that may affect the generalizability of the findings.

2. **Insight 2:** The gender imbalance, with approximately 82% male respondents, could influence the interpretation of gender-specific mental health issues and stress experiences.

3. **Insight 3:** A substantial portion of respondents report growing stress, with a notable correlation between stress levels and days spent indoors, as well as variations by occupation.

4. **Insight 4:** The willingness to seek treatment despite having a family history of mental health issues indicates a proactive approach to mental health care among respondents.

---

## Conclusion

In this project, the application of data analytics techniques has provided valuable insights into mental health trends among respondents. The visualizations created offer a clear understanding of data trends, correlations, and anomalies, enabling better comprehension of mental health dynamics and informing potential interventions.

---

## Future Work

Future work could involve:

* **Expanding the dataset** to include more diverse geographical regions and demographics to improve generalizability.
* **Analyzing longitudinal data** to track changes in mental health over time and assess the impact of interventions.
* **Integrating qualitative data** to complement quantitative findings and provide a deeper understanding of mental health experiences.

---

## Acknowledgments

I would like to thank my collaborator [Saurav Bisht](https://github.com/Saurav0129) for his contributions throughout this project. Special thanks to IBM SkillsBuild and CSRBOX for providing this invaluable opportunity.

---

## Contact

**Harsh Kumar Jha**  
B.Tech in Artificial Intelligence & Data Science  
[LinkedIn Profile](https://www.linkedin.com/in/harshkumarjha/) | [GitHub Profile](https://github.com/hkjhacode) <!--| [Portfolio]() -->

**Saurav Bisht**  
B.Tech in Artificial Intelligence & Data Science  
[LinkedIn Profile](https://www.linkedin.com) | [GitHub Profile](https://github.com/Saurav0129) <!--| [Portfolio]() -->
