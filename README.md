<img src="http://imgur.com/1ZcRyrc.png" align="left" height="55px">

### General Assembly - Data Science Immersive Course - Capstone Project Presented to Cohort

# Predicting UK Gender Pay Gap Statistics Using Company Data and Employee Reviews

## 1. Repository Contents:
- [Project Presentation](Capstone_Project_Presentation.pdf)
- [Indeed Web Scraping](1_indeed_scraping.ipynb)
- [Companies House API](2_CH_API.ipynb)
- [Gender Guesser](3_gender_guesser.ipynb)
- [Combining and Cleaning the Data](4_combining_and_cleaning.ipynb)
- [EDA](5_EDA.ipynb)
- [Data Modelling](6_final_models)
  
  
## 2. Project Goal and Data Collection
The gender pay gap is the difference in the average hourly wage of all men and women across a workforce. If women do more of the less well paid jobs within an organisation than men, such as part time work or less senior roles, the gender pay gap is usually bigger.

Using a range of data relating to company information and employee reviews, the aim of this project was to determine which factors best predict whether a company will have better or worse gender pay gap statistics. 

The gender pay gap data came from the UK Government website, which included basic company information and a range of different measures of gender pay gap performance, including the mean gender pay gap - this shows the mean difference in male and female hourly wage as a percentage.

I obtained further company data from the Companies House website using the CH API. I also performed web scraping to gather employee review data from the job posting website, indeed.com.


## 3. Data Modelling and Insights
A range of models were applied to the data, using a number of different scenarios. For example, by using both continuous or categorical dependent variables, with 2 and 3 categories tried. Various different models were used including Linear, Logistic, Support Vector Machines, K Nearest Neighbours, Random Forest and Decision Tree.

The favoured model with the best outcome was the Logistic regression model, using 2 categories - below median gender pay gap and above median gender pay gap.

### Sector Insights
Construction and Information and Communication were sectors that the model predicted would be associated with above median pay gap, meaning men typically paid more than women. 
The majority of individuals enrolling in courses related to these fields were male. 

<a href="https://imgur.com/ihYWal6"><img src="https://imgur.com/ihYWal6.png" title="source: imgur.com" /></a>


### Geographical Insights
The Midlands typically had a lower pay gap compared to the South of England.

<a href="https://imgur.com/rNxlttL"><img src="https://imgur.com/rNxlttL.png" title="source: imgur.com" /></a>

### Behavioural Insights
Reviews indicating a lack of career progression or low salary are linked with an above median gender pay gap.

<a href="https://imgur.com/pbZcMZ4"><img src="https://imgur.com/pbZcMZ4.png" title="source: imgur.com" /></a>
