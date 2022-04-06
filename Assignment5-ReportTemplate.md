**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:       | 6  |
|-----------------|---|
| Student Names:  | Sanchit Kumar  |
|                 | Aninda Shome  |
|                 | Isaiah Asaolu  |
|                 | Ibrahim Asad  |

# Introduction

The Purpose of this lab is the analysis of integration testing for a hypothetical system when providing its failure data using various reliability assessment tools such as Reliability growth testing and Reliability assessment. This was done using Reliability Demonstration Chart (RDC). We used C-SFRAT and Excel to analyze the test data to create various models to get the failure rate, MTTF, and reliability of SUT. 

# Assessment Using Reliability Growth Testing 
When deciding the best models to use to represent our data, we had to pick between a multitude of different models that ranged from accurately describing our data to being incredibly incorrect in terms of the representation. As a result, we used the log likelihood when doing model comparison as we believed that it affected other factors that determine the best model to use such as AIC, BIC, SSE, and PSSE. While doing this comparison, we kept all of the metric weights of AIC, BIC, SSE, and PSSE to 1. This was a part of the result of the model comparison (using C-SFRAT):
![log likelihood](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/LogLikelihoodTable.png)
We found that the models with the largest log likelihood (or the numbers closest to 0) were the models that best represented our data. These 4 models had log likelihoods that were the closest to 0. So, we picked model DW3(F) and IFRGSB(E, F) as the best models to represent our data because they have a log likelihood of -57.100 and -59.147 respectively.

This is a picture of the two best models overlaid on the failure rate of the failure data set provided. As can be seen, these two models match the original failure rate data provided quite well. This is the resulting picture (using C-SFRAT):
![failure rate](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/FailureRate.png)  

We also overlaid the two best models on the failure intensity of the failure data set provided. Once again, these two models match the original failure intensity data provided quite well. This is the resulting picture (using C-SFRAT):
![failure intensity](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/FailureIntensity.png)  

Lastly, this is the reliability plot of the data set provided. We chose a subset of the original data (0-18) to portray the expected reliability of the data provided. This subset was chosen based off of the laplace test that was conducted. This is the resulting picture (using C-SFRAT):
![reliability](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Reliability.png)  

A laplace test was conducted on the failure data provided. This is the resulting picture (using CASRE):
![laplace](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Laplace.png)    
As every x value with a Laplace test value lower than -2 is a relevant part of the dataset, we believe that the relevant subset of this data is from 0-18 test interval number.


# Assessment Using Reliability Demonstration Chart 

# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the team work/effort was divided and managed

# 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
