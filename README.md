# Dr.-Semmelweis-and-the-Discovery-of-Handwashing

In 1847, the Hungarian physician Ignaz Semmelweis made a breakthough discovery: he discovers handwashing. Contaminated hands was a major cause of childbed fever and by enforcing handwashing at his hospital he saved hundreds of lives.  
In this project, we re-analyzed the medical data collected by Dr. Semmelweis to show that handwashing has really reduced the number of women died as a result of childbirth by doing data visulization and statistic analysis.  


## Dependencies
```
pandas
matplotlib
```

### The structure of this notebook is as follows:
1. First, we start at loading and viewing the data.
2. We calculate the proportion of deaths per number of births for the two clinic and store the data into two new dataframe.
3. We plot the proportion_deaths by year for the two clinics in a single plot and find the death rate in clinic 1 is much higher than that of clinic 2.
    -  The only difference between the clinics was that many medical students served at Clinic 1, while mostly midwife students served at Clinic 2. 
    - `DataFrame.plot(x='', y='', ax=)`
4. We dive into the monthly data of Clinic 1 and plot the death_rate by month before and after the day when handwashing was made obligatory. 
5. We calculate and find handwashing reduced the proportion of deaths by around 0.083. (10% -> 2%)
6. We use the boostrap method to calculate the confidence interval then we can get a feeling for the uncertainty around how much handwashing reduces mortalities.
    - `boot_before = before_proportion.sample(frac=1, replace=True)`
    -  Our finding:  Handwashing reduced the proportion of deaths by between 6.7 and 10 percentage points, according to a 95% confidence interval. 
