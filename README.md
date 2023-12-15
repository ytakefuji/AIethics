# AIethics

This is under review.


# Computational Ethics for Undergraduate Students in Musashino University 

## Introduction

Computational ethics is an important subject that spans across all disciplines in the world. It is not only for ethics researchers and philosophers, but for all citizens of the world.

In the AI era, AI ethics or computational ethics is one of the most important studies for all.

## Fairness, Accountability, and Transparency

In computational ethics, fairness, accountability, and transparency play three important roles.

* **Fairness** refers to the impartial treatment of all individuals, regardless of their race, ethnicity, gender, religion, or other factors.
* **Accountability** means that AI systems should be able to explain their decisions in a way that is understandable to humans.
* **Transparency** means that AI systems should be open to inspection and audit.

## The Need for Computational Ethics

The need for computational ethics is growing as AI systems become more widely used. AI systems can make decisions that have a significant impact on people's lives, and it is important to ensure that these decisions are fair, accountable, and transparent.

## Executives, Scientists, and Engineers Need to Know About Computational Ethics

Executives, scientists, and engineers all need to know about computational ethics. Executives need to be aware of the ethical implications of AI systems and how to ensure that their companies are using AI in a responsible way. Scientists and engineers need to be aware of the potential for bias in AI systems and how to mitigate it.

## This Repository

This repository provides tools and resources for computing fairness in general. It includes code, data, and documentation that can be used to assess the fairness of AI systems.


## Types of bias

* **Cognitive bias** is a mental shortcut that can lead to inaccurate judgments. Some common cognitive biases include:
    * **Confirmation bias** - the tendency to seek out information that confirms our existing beliefs and ignore information that contradicts them.
    * **Anchoring bias** - the tendency to rely too heavily on the first piece of information we receive when making a decision.
    * **Availability bias** - the tendency to judge the likelihood of an event based on how easily examples of it come to mind.
* **Prejudice** is a preconceived opinion or feeling, either favorable or unfavorable. Prejudices can be based on race, ethnicity, gender, religion, or other factors.
* **Contextual bias** is a bias that is influenced by the context in which a decision is made. For example, a person might be more likely to hire a job candidate who went to the same college they did.
* **Unconscious or implicit bias** is a bias that is outside of our conscious awareness. Implicit biases can be formed through our experiences and interactions with the world, and they can affect our thoughts, feelings, and behaviors in ways that we are not aware of.
* **Statistical bias** is a bias that occurs when the sample used to represent a population is not representative of the population as a whole. This can lead to inaccurate conclusions about the population.


Sure, here is the beautified text for GitHub:


## Fairness Metrics

There are many metrics that can be used to measure fairness in machine learning models. These metrics can be divided into two categories: confusion metrics and fairness metrics.

**Confusion metrics** measure the accuracy of a machine learning model. They do not take into account fairness.

**Fairness metrics** measure the fairness of a machine learning model. They do this by comparing the performance of the model on different groups of people.

Some common fairness metrics include:

* **Statistical parity difference** measures the difference in the false positive rates of the model for different groups of people.
* **Disparate impact** measures the difference in the true positive rates of the model for different groups of people.
* **Equality of opportunity difference** measures the difference in the false negative rates of the model for different groups of people.
* **Average odds difference** measures the difference in the average odds of being classified as positive for the model for different groups of people.
* **Average odds error** measures the difference between the average odds of being classified as positive for the model for different groups of people and the average odds of being classified as positive in the population.
* **Class imbalance** measures the difference in the number of positive examples in the training data for different groups of people.
* **KL divergence** measures the difference in the distributions of predictions for different groups of people.
* **Conditional demographic disparity** measures the difference in the distributions of predictions for different groups of people, conditional on a sensitive attribute.
* **Between-group generalized entropy** measures the difference in the entropy of the distributions of predictions for different groups of people.
* **Generalized entropy index** measures the difference in the entropy of the distributions of predictions for different groups of people, normalized by the total entropy.
* **Generalized entropy error** measures the difference between the generalized entropy of the distributions of predictions for different groups of people and the generalized entropy of the predictions in the population.
* **Theil index** measures the difference in the inequality of the distributions of predictions for different groups of people.
* **Consistency score** measures the consistency of the predictions of the model with a fairness constraint.

The choice of which fairness metric to use depends on the specific application. For example, if the goal is to ensure that the model does not discriminate against a particular group of people, then a metric such as statistical parity difference or disparate impact might be appropriate. If the goal is to ensure that the model has the same accuracy for all groups of people, then a metric such as equality of opportunity difference or average odds difference might be appropriate.

It is important to note that no single fairness metric is perfect. Each metric has its own strengths and weaknesses. It is important to choose a metric that is appropriate for the specific application and that takes into account the specific biases that the model is trying to mitigate.


# Exercises

<b>
1.** Confusion matrix 
</b>

With breast cancer screening datasets between 1994-2009 and 2007-2013, use two sites for calculating confusion matrix and discuss false-positive and accuracy, sensitivity and specificity for comparison between two periods.

https://tools.bcsc-scc.org/dataexplorer/

https://www.bcsc-research.org/statistics/diagnostic-performance-benchmarks/diagnostic-mammography-sensitivity-specificity

Hint: pick 'Exam' for "Count by" and 'Screening mammogram classification' for "Screening mammography performance and cancer rates" for 1994-2009. Calculate false-positive and accuracy for 2007-2013.

<b>
2.* Theil Index computing
</b>

Use fetch_adult dataset with the following command which contains sex column which is one of X columns and annual-income as y column. Calculate the Theil index for Male and Female respectively and discuss fairness.

from aif360.sklearn.datasets import fetch_adult

X, y, sample_weight = fetch_adult()

<b>
3.* Theil Index computing
</b>

Calcurate the Theil index on poor and rich using the same data in the previous problem. Discuss how income difference between poor and rich can influence the Theil index.


<b>
4.** Fairness metrics computing
</b>

Use Logistic-regression and RandomForestClassifier to compare and compute fairness metrics such as disparate impact, average odds error, average_odds_difference, equal_opportunity_difference, between_group_generalized_entropy_error, conditional_demographic_disparity, theil_index, consistency_score, KL_divergence, statistical_parity_difference, and class_imbalance respectively.

Hints: Use fetch_adult dataset with the following command.

from aif360.sklearn.datasets import fetch_adult


<b>
5.*** Reweighing Technology for Fairness
</b>

In the previous problem, Logistic-regression is used to predict fairness. Use reweighing technology with Logistic-regression whether it can improve the fairness of the model. Discuss the result with the same fairness matrics for comparison.
Reweighing technology involves weighting the data. This can help to reduce bias in model.

<b>
6.* Show why machine learning models are unable to attain flawless accuracy when utilizing traditional benchmark datasets. Your answer should be substantiated with evidence from scholarly, peer-reviewed articles.

</b>

Hints: Search for articles or web sites.

<b>
7.* Demonstrate and illustrate the application of a heuristic approach by setting specific seed values to address issues of reproducibility.
   
</b>

Hints: Find a good example over the Internet.

<b>
8.** Download the program for cartpole control with reinforcement learning. Replace the value at line 403 from 50 to 250. Ensure that the program produces the same result every time it is run by removing any reproducibility issues. Save the DQN neural network and the plotted figure. 
</b>

Hints: reinforcement_q_learning.py is downloadable: https://raw.githubusercontent.com/pytorch/tutorials/main/intermediate_source/reinforcement_q_learning.py

<b>
9.** Draw a graph based on Bayesian theory to calculate the probability of detecting someone is positive.
</b>

Assume that the probability of individual with disease is 0.065 and non-infected population probability is 0.935.

Assume the true positive rate of testing is 0.991 and the false positive rate is 0.0005. Formulate the probability of detecting someone is positive: P(x,y) where x and y are the false positive rate and the true positive rate respectively.

Hint: no hint


<b>
10.** Why has the hazardous asbestos material been used in the world, despite its known health risks?
</b>

Hint: no hint

<b>
11.* Example: A healthcare provider utilizes a blood test to determine whether or not patients will have a disease. 
The results are the following:
A total of 1,000 individuals had their blood tested.
Four hundred twenty-seven individuals had positive findings, and 573 individuals had negative findings.
Out of the 427 individuals who had positive findings, 369 of them had the disease.
Out of the 573 individuals who had negative findings, 558 did not have the disease.
Let’s calculate the sensitivity, specificity. We first can start with a 2X2 Table. The information above allows us to enter the values in the table below. Notice that values in blue cells were not provided, but we can get them based on the numbers above and the utilization of total cells. 
The provider found that a total of 384 individuals actually had the disease, but how accurate was the blood test?

</b>

Hint: no hint
