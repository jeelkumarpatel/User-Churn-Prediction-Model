# Project Description

Waze’s free navigation app makes it easier for drivers around the world to get to where they want to go. Waze’s community of map editors, beta testers, translators, partners, and users helps make each drive better and safer. Waze partners with cities, transportation authorities, broadcasters, businesses, and first responders to help as many people as possible travel more efficiently and safely. 

I have built a user churn prediction model for Waze.

Attributes:  
 0   ID                      
 1   label                    
 2   sessions                 
 3   drives                   
 4   total_sessions           
 5   n_days_after_onboarding  
 6   total_navigations_fav1   
 7   total_navigations_fav2   
 8   driven_km_drives         
 9   duration_minutes_drives  
 10  activity_days            
 11  driving_days             
 12  device                   

Key insights from EDA:  
1) The more times users used the app, the less likely they were to churn. While 40% of the users who didn't use the app at all last month churned, nobody who used the app 30 days churned.  
2) Distance driven per driving day had a positive correlation with user churn. The farther a user drove on each driving day, the more likely they were to churn.  
3) Number of driving days had a negative correlation with churn. Users who drove more days of the last month were less likely to churn.  
4) Users of all tenures from brand new to ~10 years were relatively evenly represented in the data.  
5) Several variables had highly improbable or perhaps even impossible outlying values, such as: driven_km_drives, activity_days and driving_days.

Model used: Binomial Logistic Regression
Activity_days was by far the most important feature in the model. It had a negative correlation with user churn.  

In EDA, user churn rate increased as the values in km_per_driving_day increased. In the model, distance driven per day was the second-least-important variable.  
