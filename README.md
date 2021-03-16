<img src="http://imgur.com/1ZcRyrc.png" align="left" height="55px">

### General Assembly - Data Science Immersive course

# Predicting UK Gender Pay Gap Statistics Using Company Data and Employee Reviews

## 1. Repository Contents:
- [Project Presentation](Capstone_Project_Presentation.pdf)
- [Indeed Web Scraping](1_indeed_scraping)
- [Companies House API](2_CH_API)
- [Gender Guesser](3_gender_guesser)
- [Combining and Cleaning the Data](4_combining_and_cleaning)
- [EDA](5_EDA)
- [Data Modelling](6_final_models)
  
  
## 2. Project Goal and Data Collection
The gender pay gap is the difference in the average hourly wage of all men and women across a workforce. If women do more of the less well paid jobs within an organisation than men, such as part time work or less senior roles, the gender pay gap is usually bigger.

Using a range of data relating to company information and employee reviews, the aim of this project was to determine which factors best predict whether a company will have better or worse gender pay gap statistics. 

The gender pay gap data came from the UK Government website, which included basic company information and a range of different measures of gender pay gap performance, including the mean gender pay gap - this shows the mean difference in hourly wage as a percentage.

I obtained further company data from the Companies House website using the CH API. I also performed web scraping to gather employee review data from the job posting website, indeed.com.


## 3. Data Modelling and Insights
A range of models were applied to the data, using a number of different scenarios. For example, by using both continuoius or categorical dependent variables, with 2 and 3 categories tried. Additionally, various different models were used such as Logistic, Support Vector Machines, K Nearest Neighbours, Random Forest and Decision Tree. 
