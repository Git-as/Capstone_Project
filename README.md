<img src="http://imgur.com/1ZcRyrc.png" align="left" height="55px">

### General Assembly - Data Science Immersive Course - Capstone Project Presented to Cohort

# Predicting UK Gender Pay Gap Statistics Using Company Data and Employee Reviews

## 1. Repository Contents

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

Further company data was obtained from the Companies House website using the CH API. I also performed web scraping to gather employee review data from the job posting website, indeed.com.


## 3. Data Modelling and Insights

A range of models were applied to the data, using a number of different scenarios. For example, by using both continuous or categorical dependent variables, with 2 and 3 categories tried. Various different models were used including Linear, Logistic, Support Vector Machines, K Nearest Neighbours, Random Forest and Decision Tree.

The favoured model with the best outcome was the Logistic regression model, using 2 categories - below median gender pay gap and above median gender pay gap. 

The final model score was 0.66, which was above the bassline score of 0.5. All the models attampted gave scores between 0.61 and 0.66 - K Nearest Neighbours yielded the worst model score and the remaining scores were around 0.63. 


### Location
The Midlands had many towns with high positive coefficients, this means that the model predicts below median gender pay gap scores for towns in this area - in other words, there is a lower rate of inequality in the Midlands.

Interestingly, London had a coefficient of -0.2 which means that the model predicts above median scores for companies in London, and the gender pay gap scores in london show a higher rate of inequality. This is generally the case in the areas surrounding London as well, as can be seen on the right.

<a href="https://imgur.com/rNxlttL"><img src="https://imgur.com/rNxlttL.png" title="source: imgur.com" /></a>

### Sector
The 2018 educational enrollment rates (all levels) split by gender were reviewed, for each sector in order to determine any links This information was obtained from: stats.oecd.org/. Some of the sectors could not be isolated from the educational database, therefore no conclusion was reached as to whether or not they impact gender pay gap.

<a href="https://imgur.com/G225Ury"><img src="https://imgur.com/G225Ury.png" title="source: imgur.com" /></a>

However it does demonstrate that educational enrollment rates play a part in gender pay gap - since those with higher male enrollments tended to have above median scores meaning that the model predicted these sectors to have gender pay gap scores above median, meaning that males are paid more the females. 

<a href="https://imgur.com/ihYWal6"><img src="https://imgur.com/ihYWal6.png" title="source: imgur.com" /></a>

### Behavioural Insights
Natural Language Processing (NLP) was applied to all the text fields in the review - the header, main text, review pros and review cons. Interestingly, only the review cons improved the model score so this is the only field out of the reeview text that was included in the final model. 

The ‘review cons’ themes that were most associated with below median gender pay gap were:
* Negative Culture, e.g. ‘blame culture’, ‘high stress’, ‘poor communication’
* Long hours, e.g. ‘nights long’, ‘early starts’, ‘hours stressful’
* Poor Management, e.g. ‘working conditions’, ‘bad management’

The ‘review cons’ themes that were most associated with above median gender pay gap were:
* Career Progression, e.g. ‘Career Progression’, ‘lack progression’, 
* Poor Pay, e.g. ‘Minimum Wage’, ‘Low Pay’
* Long Hours, e.g. ‘Job long’, ‘times long’, ‘working weekends’
* Poor Management, e.g. ‘Terrible Management’, ‘awful management’

Whilst it is not known whether the reviews were written by a male or female, it is interesting that a lack of career progression and poor pay are themes associated with above median gender pay gap.

<a href="https://imgur.com/pbZcMZ4"><img src="https://imgur.com/pbZcMZ4.png" title="source: imgur.com" /></a>

### Proportion of Female Officers
A higher proportion of female officers was associated with below median gender pay gap. This also aligns with the heat map shown above, that suggested the proportion of female officers was correlated to the mean gender pay gap.

<a href="https://imgur.com/NS5X2HJ"><img src="https://imgur.com/NS5X2HJ.png" title="source: imgur.com" /></a>

### Company Size
Smaller companies were associated with above median pay and larger companies with below median. This would suggest that larger companies are better at providing more equal pay to men and women.

Eight companies did not provide this information and are listed as ‘Not Provided’. However, the ‘Not Provided’ companies also have a high positive coefficient which implies that those who didn’t include the company size tended to have below median gender pay gap stats.

<a href="https://imgur.com/irHMRUV"><img src="https://imgur.com/irHMRUV.png" title="source: imgur.com" /></a>

### Responsible Person Assigned
Companies that assigned a responsible person to their gender pay gap report were associated with lower gender pay gap (below median results) than those who did not list a responsible person.

This is unsurprising if you assume that those who did not provide a responsible person do not have a dedicated person to take ownership of gender pay gap within their organisation.

<a href="https://imgur.com/GiNqWFZ"><img src="https://imgur.com/GiNqWFZ.png" title="source: imgur.com" /></a>


## 4. Conclusion

* The final model applied which yielded the highest score of 0.66 was the logistic regression model. This was above the bassline accuracy score of 0.5. 
* Sector, Location and Review Cons were the most influential predictors of whether the mean pay gap would be above or below median. 
* Construction and Information and Communication were sectors that the model predicted would be associated with above median pay gap, meaning men typically paid more than women. The majority of individuals enrolling in courses related to these fields were male. 
* The Midlands typically had a lower pay gap compared to the South of England. This could be because certain sectors are more predominant in certain areas or there may be cultural and social differences. 
* Reviews indicating a lack of career progression or low salary are linked with an above median gender pay gap. These are 'cons' that you would expect for companies that have poor gender pay gap where many women may feel that there are limited career progression options and salary is considered as low. 
* Size, Proportion of Female Officers and whether or not the company had an assigned responsible person were also important features.

## 5. Key Takeaways

* A model score of 0.66 means that this model has some predictive power in identifying whether a company will have a greater or smaller gender pay gap. It also highlights the key areas of focus for improving this statistic, for example that cities in the South of England and smaller companies need to be acting more to achieve gender pay gap. 
* The results relating to company sector indicate that changes need to be made to encourage gender equality from an early age to impact the gender balance in educational enrollment. 
* When performing the NLP, it was interesting to discover that of the full employee reviews, including the review pros or main body of text did not improve the model score and that it was only the review cons which improved the model score. This could be because the cons are more concise than the main body of text, so the individual words have more value. It may also be that the review cons give more of a truthful insight into the company environment than review pros sections. 

## 6. Key Learnings

### Challenges 
* At the start of the project, it was difficult to find the company information I needed and I wasn't sure if everything I wanted to look at would be available in Companies House. After a lot of extensive research of websites that provide free information on companies, I ended up finding all the information desired on companies house and the government gender pay gap dataset. 
* Using the Companies House API turned out to be more challenging than expected, there was no guideance on how to use the API for Python, so I had to scroll through forums to piece together the different steps I needed to do to access the information. 
* There were many different options in terms of models to try - for example which target variable to use, whether to make this a continuous or categorical variable, which predictor variables to include, which parameters to apply for NLP. There were so many different combinations of the above variables that could have been applied and I had to be strategic with the time I had in order to try and get the best model. 

### Milestones 
* The challenges I had with the API taught me a lot as I had to go through and do a lot of research to understand why it wasnt working and make sure I understood clearly each line of code for all the solutions attempted.
* The project was also a great way to learn more about NLP and how the parameters affect the results. 
* My greatest achievement from this project, was my determination and ability to find solutions when it at times felt impossible. Seeing a problem and brainstorming until I found a solution that worked also strengthened my ability to know how and where to look online to find solutions. 

<b>Please find below the links for three useful and interesting articles to understand more about gender pay gap issues:</b>
1) ig.ft.com/gender-pay-gap-UK/
2) mckinsey.com/featured-insights/diversity-and-inclusion/women-in-the-workplace
3) indeed.com/lead/women-in-tech-report
