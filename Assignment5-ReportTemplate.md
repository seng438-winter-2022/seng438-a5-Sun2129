**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:       | 6  |
|-----------------|---|
| Student Names:  | Sanchit Kumar  |
|                 | Aninda Shome  |
|                 | Isaiah Asaolu  |
|                 | Ibrahim Asad  |

# Introduction

The Purpose of this lab is the analysis of integration testing for a hypothetical system when providing its failure data using various reliability assessment tools such as Reliability growth testing and Reliability assessment. In the first part of the lab, we first used C-SFRAT and CASRE to input and analyze the test data provided to get the laplace test and the best models that fit the failure data provided. Through these programs, we were able to create a failure rate graph, a failure intensity graph, and a reliabilty growth graph. In the second part of the lab, we used a different technique to determine the reliabilty of the same data set provided in the first part. This time, it was done by using a Reliability Demonstration Chart (RDC) to determine if the failure data was acceptable for a program. Through this excel sheet, we determined the MTTF and reliabilty of the SUT. Altogether, we were able to gain familiarity with and use various tools to conduct reliability testing on a SUT.

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
We evaluated the acceptance of the system using different MTTFMin values. The first one shown is the original MTTFMin value that we decided to use. This was calculated using the total number of failures and the total execution time. The formula used was total execution time/total number of failures.  
This is the chart of MTTFMin (using SRTAT):
![MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/MTTFMin%20Graph.png)

This is the chart of the double of MTTFMin (using SRTAT):
![Double MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Double%20MTTFMin%20Graph.png)

This is the chart of the half of MTTFMin(using SRTAT):
![Half MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Half%20MTTFMin%20Graph.png)
# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the team work/effort was divided and managed

We worked together in the lab for both part 1 and part 2. Since some members could not run the necessary tools for part 1 we did a screen share so that everyone could get involved. In part 1, one person would be screen sharing them using the C-SFRAT program while the other remaining members would then be analyzing the models and noting any necessary observations. Part 2 had a similar format as well where one person screen shared and used the Excel Sheet.  The other individuals for part 2 analyzed the models, noting any necessary observations, and ensured every part had the correct models made. Lastly we checked to see if both parts were correct in the lab and made changes if we felt any needed to be made for the accuracy of the lab altogether. 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself


