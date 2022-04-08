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

Decision Making Given a Target Failure Rate:


Advantages of Reliability Growth Analysis:  
One advantage of reliability growth analysis is that it can be used to predict potential failures in the future. This is very important, as the developers then know what to expect and that they should be prepared for these types of failures to occur. Reliability growth analysis also allows for us to assess how reliable a system is over time, and how many failures/errors occur throughout the process. 

Disadvantages of Reliability Growth Analysis:  
One disadvantage of the reliability growth analysis is that when a failure/error is fixed, it could introduce more potential failures and thus the graph would not be able to model that accurately as it will not know what changes were made that introduced new failures. Another disadvantage is that a software can be used in multiple different ways, and the failures that occur in one way might not be present in another. Thus, this creates a lot of complications with trying to create one accurate model to depict the failures over time.

# Assessment Using Reliability Demonstration Chart 
We evaluated the acceptance of the system using different MTTFMin values. The first one shown is the original MTTFMin value that we decided to use. This was calculated using the total number of failures and the total execution time. The formula used was total execution time/total number of failures.    
This is the chart of MTTFMin (using SRTAT):  
![MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/MTTFMin%20Graph.png)

This is the chart of the double of MTTFMin (using SRTAT):  
![Double MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Double%20MTTFMin%20Graph.png)

This is the chart of the half of MTTFMin(using SRTAT):  
![Half MTTFMin](https://github.com/seng438-winter-2022/seng438-a5-Sun2129/blob/main/Graph%20Pictures/Half%20MTTFMin%20Graph.png)

Advantages of Reliability Demonstration Chart:

Disadvantages of Reliability Demonstration Chart:

# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques
A key difference between these two techniques is that both the methods used the same data to produce a different output/graph to convey the information. A similarity between the two is that they both are based on inter failure times and the target failure rate, or the MTTF. Another difference is that the reliability growth analysis relies on failure count as well, whereas the demonstration chart does not. One more similarity is that they are both modelling the reliability of a system over time, with respect to its failures

# How the team work/effort was divided and managed
We worked together in the lab for both part 1 and part 2. Since some members could not run the necessary tools for part 1 we did a screen share so that everyone could get involved. In part 1, one person would be screen sharing them using the C-SFRAT program while the other remaining members would then be analyzing the models and noting any necessary observations. Part 2 had a similar format as well where one person screen shared and used the Excel Sheet.  The other individuals for part 2 analyzed the models, noting any necessary observations, and ensured every part had the correct models made. Lastly we checked to see if both parts were correct in the lab and made changes if we felt any needed to be made for the accuracy of the lab altogether. 

# Difficulties encountered, challenges overcome, and lessons learned
From the time we started the assignment to the completion, we encountered tons of difficulties. We were provided with contradicting messages for when we would have the demo. This resulted in an increased level of stress as we scrambled to get the applications working in order to perform the assignment. A difficulty we ran into was that the tools provided don’t run on mac devices, which was an issue that set our group back, as we have members with mac devices. The tools/applications being used in the lab were outdated, which was another difficulty in the assignment. The CASRE application, for example, was last updated in 1991 and for some reason it wouldn’t allow us to open the failure-dataset.dat file. We spend hours just trying to open the dataset. During and after the demo, while interacting with TAs and communicating with other groups, we kept hearing conflicting messages about what tools worked, what tools did not and what we should use instead. We also found the answers provided when asking questions were vague and inadequate. Additionally, we noticed that the terminologies used in the class by the prof and in his notes differed from what were  used in the assignment.The next difficulty encountered was with the use of EXCEL for part 2. We found that the information provided for this part, as well as the instructions given in the manual was insufficient to completing part 2. This is strengthened by the fact that we were approached by several groups, who were also encountering the same problems as well. The assignment handout wasn’t exactly clear as to what data was needed in the columns. And the behaviour we got  from the graph contradicted what we had learnt in class. In the end, we were able to resolve most of the difficulties we faced. We had some sections of the assignment completed for our demo and presented that to the TA and as well as gave him an action plan on our next step. We were not able to resolve the mac issue. We got laplace working on the CASRE application. We were able to schedule a zoom meeting with Yousef, which helped with resolving issues we had, clarifying conflicting messages, and guiding us towards completing the lab. We learnt that starting in labs as early as possible is crucial, as the possibility of encountering issues is high, and those issues can significantly impact your progress and increase stress level. Our knowledge and understanding of laplace was strengthened.

# Comments/feedback on the lab itself
The Lab document itself was extremely confusing. There were several key terminology issues as some terms were different from the ones used in the lab from the notes. The Programs/Tools are outdated and cannot be used within the lab for Part 1 and was not accessible for Mac, so individuals had to watch a screen share to see how the program ran and worked. When asked about using other tools, there was no clear alternative to use as a replacement for C-SFRAT. There were also some difficulties when obtaining certain models as well. Using the Excel sheet was confusing and we had to have the TA show us how to use it which took a whole day as both the TA and our group were confused as to why our data was not producing the correct models as there was not a lot of information on steps on how to do it. The actual Excel sheet needs to be edited as it was in a Protected View therefore not allowing for us to change it as initially intended for the lab.

