# Student Performance Dashboard (Power BI)
*Student performance visualization using Power BI*


Below is an exported PDF of the dashboard. Viewers may download the file *(StudentPerformancePortfolio(PwrBI).pbix)* attached to this repository to interact with the dashboard for free using Power BI Desktop!


<img width="987" height="558" alt="studentperformancepdf" src="https://github.com/user-attachments/assets/7b84aecd-2206-4643-8b65-936cebdf7288" />

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
<br>

# Key Metrics
Visualizations represented on the dashboard and their purpose
- **Risk Level by Race/Ethnicity** -> Identify disparities and equity issues.
- **Average Score by Gender** -> Detecting patterns for direct academic support.
- **Students with Highest Risk Level** -> Focusing support resources on the most at-risk students.
- **Total Risk %** -> Current percentage of students classified at high risk.
- **Target % Reduction** -> Goal metric for creating an improvement plan.
<br><br>

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

### Risk Level (DAX Query)
<img width="245" height="71" alt="riskelvel" src="https://github.com/user-attachments/assets/64c92d5b-b662-4fe0-bb68-27cf01cdd468" />
<br>

*This query categorizes the Risk Score into Levels*
- Students with a Risk Score of 4 or higher are labeled as "High" risk.
- Students with a Risk Score of 3 or less are labeled as "Medium/Low" risk.
