# Student Performance Dashboard (Power BI)
*Student performance visualization for Prediction using Power BI*


Below is an exported PDF of the dashboard. Viewers may download the file *(StudentPerformancePortfolio.pbix)* attached to this repository to interact with the dashboard for free using Power BI Desktop!

<img width="983" height="551" alt="portfoliopdf" src="https://github.com/user-attachments/assets/90fcb16d-fa31-4286-8c95-b8eff217e6eb" />

*PDF version available in files*

# Project Overview
"Predictive dashboard to identify high-risk students based on test scores to aid early intervention" <br> <br>
***Objective***
- Student Improvement
- Equity in Education
- Improving Retention/Graduation Rates
<br>

***Summary of Data*** <br>
- **Synthetic data** of 100 students with Race/Ethnicity anonymized
- Risk indicators are **Math/Reading/Writing Scores, Test Prep Course, Lunch Type, and Parental Education**.
- Data has been standardized and anonymized prior
- Original CSV file attached in [this repository](Student_Data.csv)
<br>

# Key Metrics
Visualizations represented on the dashboard and their purpose
- **High Risk Students by Race/Ethnicity** -> Identify disparities and equity issues.
- **Average Score of High Risk Students by Gender** -> Detecting patterns for direct academic support.
- **Students with Highest Risk Level** -> Focusing support resources on the most at-risk students.
- **% High Risk and Target High Risk** -> Current percentage of students classified as high risk and a Goal metric for creating an improvement plan.
<br>

# Predictive Model Methodology 
### Risk Score Formula (DAX Query)
<img width="382" height="124" alt="riskscoredaxquery" src="https://github.com/user-attachments/assets/8eeec957-37e8-405d-bce4-f25222d655f8" />
<br>

*This query calculates each student's Risk Score*
- **Math/Reading/WritingRisk**: if the student's test scores are above 65, add 1 point; if not, 0.
- **TestRisk**: if the student's 'Test Prep Course' is "None", add 1 point; if not, 0.
- **LunchRisk**: if the student's 'Lunch Type' is "Free/Reduced", add 1 point; if not, 0.
- **ParentRisk**: if the student's 'Parental Education' is "High School", add 1 point; if not, 0.
<br>

### Risk Level Threshold (DAX Query)
<img width="245" height="71" alt="riskelvel" src="https://github.com/user-attachments/assets/64c92d5b-b662-4fe0-bb68-27cf01cdd468" />
<br>

*This query categorizes the Risk Score into Levels*
- Students with a Risk Score of 4 or higher are labeled as "High" risk.
- Students with a Risk Score of 3 or less are labeled as "Medium/Low" risk.
<br>

### High Risk % and Target % (DAX)
<img width="390" height="56" alt="high risk%" src="https://github.com/user-attachments/assets/ccc578f6-3525-4627-8d07-d98a4cbf6e4c" />

*This query finds the % of students that are at risk from the population*
<br>

# Key Insights
- High Risk percentage is currently at 24%; the target is 20%.
- Racial/Ethnic Group C & D have the highest share of % in high-risk students (29.17%), which is more than 3 times Group B & E (8.33%), indicating a potential support gap.
- Male students of the high-risk group show a low average score in math (59.55), along with female students (57.83). Yet, Non-Binary students of the same high-risk group have the highest average math score (84.00). This may be due to a heavy outlier or sample size; however, it still indicates a potential resource gap in math.
- Non-Binary students of the high-risk group show a low score on average reading score (54.00), indicating a potential support gap.
- Multiple high-risk students have their primary teacher as Ms. Patel or Mrs. Kim.
<br>

# Improvement Plan

