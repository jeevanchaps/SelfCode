# SelfCode: An Annotated Corpus and a Model for Automated Assessment of Self-explanation during Source Code Comprehension

## Abstract
The ability to automatically assess learners' activities is key to user modeling and personalization in adaptive educational systems.
The work presented in this paper opens an opportunity to expand the scope of automated assessment from traditional programming problems to code comprehension tasks. 
In code comprehension tasks, students may be asked to explain critical steps of the code. The ability to automatically assess these self-explanations offers a unique 
opportunity to understand the current state of student knowledge, recognize possible misconceptions, and provide feedback. Annotated datasets are needed to train 
Artificial Intelligence/Machine Learning approaches for the automated assessment of student explanations. To answer this need, we present a novel corpus called 
SelfCode which consists of 1,771 sentence pairs of student and expert self-explanations of JAVA code examples along with semantic similarity judgments provided by 
experts. We also present a baseline automated assessment model which relies on a set of textual features.

## Data Set Example
| Student Explanation | ExpertExplanation | Annotation Score |
| --- | --- | ---|
| Declares the array we want to use for our assignment | We initialize the array of type int to hold the specified numbers. | 4 |
| variable decleration: declares the number we are trying to divide | We could initialize it to any positive integer greater than 1. | 1 |
| if the loop condition is true, then we increment the divisor by 1 | When the divisor is not a factor of the number, we increment the variable divisor by 1. | 3 |
| Get the number entered by the user. | We read the seconds by calling the nextInt() method because this input is an integer. | 2 |
| Ask the user to enter an integer. | We prompt the user to enter an integer.| 5 |

## Data Set Stats

| Annotation Label | No. of sentence pairs |
| --- | --- |
| 1 | 529 |
| 2 | 507 |
| 3 | 419 |
| 4 | 256 |
| 5 | 62 |
