
# Cleaning and Visualizing Survey Data in Power BI
## Introduction
In this power Bi Project, we'll walk through the process of cleaning and visualizing survey data collected from data professional around the world with 630 respondent answering various questions. The dataset contains responses from data professionals and covers various aspects of their roles, skills, and preferences.


## Problem Statement

### Columns 
##### Unique ID- Unique Identifiers
         Email- Anonymous
         Date Taken (America/New_York) -Date of Survey Taken
         Time Taken (America/New_York)- Time of Survey Taken
         Time Spent - Duration of Taking Survey.
         Q1 - Which Title Best Fits your Current Role?
         Q2 - Did you switch careers into Data?
         Q3 - Current Yearly Salary (in USD)
         Average Salary
         Q4 - What Industry do you work in?
         Q5 - Favorite Programming Language.
         Q6 - How Happy are you in your Current Position with the following? (Salary)
         Q6 - How Happy are you in your Current Position with the following? (Work/Life Balance)
         Q6 - How Happy are you in your Current Position with the following? (Coworkers)
         Q6 - How Happy are you in your Current Position with the following? (Management)
         Q6 - How Happy are you in your Current Position with the following? (Management)
         Q6 - How Happy are you in your Current Position with the following? (Learning New Things)
         Q7 - How difficult was it for you to break into Data?
         Q8 - If you were to look for a new job today, what would be the most important thing to you?
         Q9 - Male/Female?
         Q11 - Which Country do you live in?
         Q12 - Highest Level of Education
         Q13 - Ethnicity

###Questions
-Number of Survey respondent
-Age of respondent 
- Avearge Salary
Analyze the spread of respondent.

### Steps 

- Step 1 :Importing Data
   - Open Power BI Desktop.
   - Go to "Home" tab and select "Get Data".
   - Choose the appropriate data source (Data Professional Survey.CSV) and import the survey data.

2. Data Cleaning
   - The first was to use the first row as promoted headers.
   - Change the Unique ID column into a text datatypes(categorical datatypes)
   - Remove the columns(browser to referral column) that won't be used in the analysis and remove personal information.
   - Filter Columns and remove rows with others to be reduce ambiguity from data.
   - Handle missing values by either removing or imputing them.
   - I find the average salary by dividing the range of salary divided by 2.
   - Standardize categorical variables (e.g., job titles, programming languages) for consistency i.e favorite programme language,
   - Check for duplicate entries and eliminate them if necessary.

3. Data Transformation
   - Create calculated columns i.e Current Age,Count of Survey Takers = COUNT('Data Professional Survey'[Unique ID]), and measures
   (Summarization) i.e Q6 - How Happy are you in your Current Position with the following? (Coworkers),Q6 - How Happy are you in your Current Position with the following? (Learning New Things),Q6 - How Happy are you in your Current Position with the following? (Management),Q6 - How Happy are you in your Current Position with the following? (Salary),Q6 - How Happy are you in your Current Position with the following? (Salary),Q6 - How Happy are you in your Current Position with the following? (Work/Life Balance)
   - Perform any necessary data transformations, such as grouping, filtering, or splitting columns.
   - Normalize data required for analysis.
   - **Calculated Columns:**
     - Age Group: 
       ```
       Count of Survey Takers = 
       COUNT('Data Professional Survey'[Unique ID])
       ```
   - **Measures:**
     - Average Years of Experience:
       ```
       Avg Years of Experience = AVERAGE('Survey Data'[Years of Experience])
       ```


Visualization
   - Create different types of visualizations to explore the survey data.
   - Examples of visualizations include:
   Following DAX expression was written to find count of test takers,
 
         Count of Test Takers = COUNT(Unique ID])
    
 A card visual was used to represent this total.

 Following DAX expression was written to find count of test takers,
 
         Average Age of Test Takers = Average(Current Age)
    
 A card visual was used to represent this Average Age.


 A gauge visual was used to represent this Work-life Balance of survey takers.

 Following DAX expression was written to find % of Work-life Balance of survey takers,
 
         Work-life Balance of survey takers = Average of Q6 - How Happy are you in your Current Position with the following? (Work/Life Balance) and the minimum and maximum of this value on both axes.
 

  A gauge visual was used to represent this Happiness of current salary of survey takers.

  Following DAX expression was written to find Happiness of current salary of survey takers,
 
         Hapiness of current salary of survey takers = Average of Q6 - How Happy are you in your Current Position with the following? (Salary) Minimum of Q6 - How Happy are you in your Current Position with the following? (Salary) and Maximum of Max of Q6 - How Happy are you in your Current Position with the following? (Salary) on both axes.
  A pie chart was used to shpw proportion
  Pie charts for displaying proportions of categorical variables.(Average current salary of Female vs Male)

  A Bar chart visual was used to show average salary by job title
   Bar charts for comparing categorical data.

   A stacked Column chart was used to plot the most favorite programming language vs Which Title Best Fits your Current Role.

     - Heatmaps for visualizing correlations between variables.i.e Q11 - Which Country do you live in vs Count of Survey Takers
 
### Insights from the Survey dataset
   - The number of Survey is 630
   - The Average Age of Survey respondent is 29.87
   - Average Salary of Female is higher than Male.
   - Pthyon programming Language is the most popular accross roles.
   - Most of the Survey respondent is from United States of America totally 261 of the 630.

### Sharing and Collaboration
   - I will consider publishing the report to Power BI Service for wider distribution and accessibility.
### Limitations:
- Sample Size: Small sample sizes (<1000) can lead to biased or skewed results and reduce statistical power. 

- Representativeness: Limited sample representativeness may hinder generalizability and subgroup analysis.
More exploration should be carried out to discover more pattern and Trends



### Recommendations:

-  Increase Sample Size: Aim for larger samples to improve representativeness and statistical power.
-  Stratified Sampling: Use a more broad sampling method to ensure representation across diverse subgroups.

