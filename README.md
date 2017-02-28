# Inferential-Statistics-Exercises
Three data sets(human body temperature, resume call backs, and hospital readmissions) were examined as part of the Springboard Data Science Intensive program.

Exercise 1 is a study of Human Body Temperature.  Filename: sliderule_dsi_inferential_statistics_exercise_1.
Other files required to run the notebook:  Normal_distribution_curve.jpg, thermowarsfunnies2.jpg

Data set was created by Allen Shoemaker of Calvin College in 1996 to be used for educational purposes.  It is comprised of 130 observations, half male and half female, of body temperature and heart rate.  More information can be found here: https://ww2.amstat.org/publications/jse/v4n2/datasets.shoemaker.html
Summary of Data Analysis:
  Data was checked for normality using several methods: visual inspection of distribution plot, D-Agostino and Pearson's statistical test,   and a linear regression.
  Data was checked for correlation between body temperature and heart rate.
  A one sample t-test was performed to compare the mean of the data sample to the "known" mean of 98.6 degrees Fahrenheit.
  A determination was made of what the range of "normal" temperature should be considered based on the data set.
  The mean temperatures of males and females was compared and found to be different.
  The t-test for two independent samples was calculated to determine if the difference in means is due to chance or is "real".
  Finally, it was determined whether or not the difference in means is statistically significant.
A summary of the findings, conclusions, and recommendations are at the end of the notebook.
The slideshow presentation software has some bugs so the slideshow presentation currently is not complete.  

Exercise 2 is a study of racial discrimination. Filename: sliderule_dsi_inferential_statistics_exercise_2
The Data was taken from a field study that occured between 2000 and 2002. Approximately 5000 resumes were submitted in response to 1300 job advertisements.  Each employer received 4 resumes: two were high quality resumes and two were low quality resumes.  "Black" sounding names and "white" sounding names were randomly assigned to the resumes. Email responses and callbacks were recorded.
Summary of Data Analysis:
  Proportion hypothesis testing was done on the difference in email response and callbacks based on race. The testing was repeated for about eight other measures such as volunteer work, special skills, computer skills, honors awards, gender, military service, employment holes, and quality of the resume.
  Additional analysis was done to investigate the influence of level of education, number of previous jobs held, years of experience, and the zipcode of the applicant.  The zipcode reflected the percentage of "blacks" that resided in the neighborhood of the applicant and it was plotted against percentage of callbacks to check for a correlation.
  The results are summarized at the end of the notebook.

Exercise 3 is a study of Hospital Readmission Rates.  Filename: sliderule_dsi_inferential_statistics_exercise_3
Another file was used as a scratch pad for investigation.  It's called:  HospitalReadmitDataExplore
Springboard provided a scatterplot and Preliminary Analysis for us to evaluate.  I disagreed with their conclusions. Directly underneath the Preliminary Report are my comments.  
Here is a summary of my analysis:
  Although some cleanup work had been done on the data, I found some null data that needed to be deleted.  Then I created a few more columns of data with calculations I made from the given data.  I calculated the observed(I called it the "actual") readmission rate, the actual readmission ratio, and the raw number of expected readmissions.  I also took the log of the actual readmission rates.
  Next, I looked at the distributions of the key data: actual, predicted, and expected readmission rates and the readmission ratios.  I observed that the readmission rates distributions appeared to be bimodal.  After reading the information on the cms site and understanding that there are five different treatment measures, I stratified the data and realized that the distribution is actually multi-modal.
  I recreated the same scatterplot as was given at the start of the exercise.  I observed that there is no cear correlation between number of discharges and excess readmission ratio based on the fact that the data was a big cluster with no obvious trends.  
  I created a linear regression plot using seaborn setting the hue as the treatment groups.  It showed that the correlations are different for the different treatment groups.
  I also investigated several other plots to better understand the data.
  I did some statistical analyses.  I found the mean and confidence intervals for the actual readmission rates and the expected readmission rates.  I noticed that the confidence intervals did not even overlap for 4 out of the 5 groups and barely overlapped for the fifth.  I did a difference in means hypothesis test to prove that the probability of the actual (observed) means differing from the expected means is very low indicating that the "expected" means as calculated by the government are not reasonable.  Just to be thorough, I also did a chi-squared hypothesis test on the difference between the raw number of readmissions versus the expected number of readmissions.  I got the same result, very low p-values, indicating the values for the expected number of readmissions is not reasonable.
  I wanted to identify the top and bottom 5% performers.  Because the data for several of the treatment groups is skewed and not symmeterical, my first attempt resulted in numbers that did not make sense.  So I used the log of the data for three of the groups and the results were better. My approach and thinking is based on my knowledge of what is considered "average" for school performance and in psycho/educational testing.  I decided that the best approach is to identify the hospitals whose readmission rates differ from the mean by more than one standard deviation.  
  After identifying the top and bottom 5% performers, I compared the number of discharges(which related to hospital capacity) for these hospitals.  The ranges overlap indicating that it is not reasonable to make a blanket conclusion that small hospitals are poor performers across the board.  For several of the treatment groups, the smaller hospitals outperformed the larger hospitals.  It was only for the hip and knee replacement group that the larger hospitals clearly performed better.  However, even in this case, smaller hospitals were included in the list of top 5%.
  At the end of the notebook, I summarize my findings and make recommendations.
  
