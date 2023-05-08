# SelfCode: An Annotated Corpus and a Model for Automated Assessment of Self-explanation during Source Code Comprehension

## Abstract
The ability to automatically assess learners' activities is key to user modeling and personalization in adaptive educational systems.
The work presented in this paper opens an opportunity to expand the scope of automated assessment from traditional programming problems to code comprehension tasks. 
In code comprehension tasks, students may be asked to explain critical steps of the code. The ability to automatically assess these self-explanations offers a unique 
opportunity to understand the current state of student knowledge, recognize possible misconceptions, and provide feedback. Annotated datasets are needed to train 
Artificial Intelligence/Machine Learning approaches for the automated assessment of student explanations. To answer this need, we present a novel corpus called 
SelfCode which consists of 1,770 sentence pairs of student and expert self-explanations of JAVA code examples along with semantic similarity judgments provided by 
experts. We also present a baseline automated assessment model which relies on a set of textual features.

## Data Set Example
| Line of Code | Crowd Sourced Explanation | ExpertExplanation | Annotation Score |
| --- | --- | ---| --- |
| int [] arr = { 1, 2, 3}; | Declares the array we want to use for our assignment | We initialize the array of type int to hold the specified numbers. | 4 |
| int num = 15; | variable decleration: declares the number we are trying to divide | We could initialize it to any positive integer greater than 1. | 1 |
|  divisor += 1; | if the loop condition is true, then we increment the divisor by 1 | When the divisor is not a factor of the number, we increment the variable divisor by 1. | 3 |
| int seconds = scan.nextInt(); | Get the number entered by the user. | We read the seconds by calling the nextInt() method because this input is an integer. | 2 |
| System.out.println("Enter an integer: "); | Ask the user to enter an integer. | We prompt the user to enter an integer.| 5 |

## Data Set Stats

| Annotation Label | No. of sentence pairs |
| --- | --- |
| 1 | 529 |
| 2 | 507 |
| 3 | 419 |
| 4 | 253 |
| 5 | 62 |

## Baseline Model Results

Performance of the models with textual features (M1)

| Models | Precision | Recall | F1-score | Accuracy |
| --- | --- | --- | --- | --- |
| Logistic Regression | 0.30 | 0.27 | 0.25 | 36.91% |
| Decision Tree | 0.30 | 0.277 | 0.29 | 33.24% |
| Support Vector Machine | 0.18 | 0.21 | 0.15 | 30.69% |
| Naive Bayes | 0.36 | 0.35 | 0.32 | 37.93% |

Performance of the models with textual features and semantic similarity score from SentenceBERT (M2)

| Models | Precision | Recall | F1-score | Accuracy |
| --- | --- | --- | --- | --- |
| Logistic Regression | 0.37 | 0.37 | 0.36 | 47.31% |
| Decision Tree | 0.32 | 0.33 | 0.32 | 37.25% |
| Support Vector Machine | 0.18 | 0.21 | 0.15 | 30.92% |
| Naive Bayes | 0.43 | 0.41 | 0.40 | 46.40% |

Confusion Matrix for M1 and M2 

![confusion_m1](https://user-images.githubusercontent.com/10882985/230940385-0fc051e0-d261-4207-bb06-69bad4cd7b0c.png "M1 confusion matrix")

![confusion_m2](https://user-images.githubusercontent.com/10882985/230940485-13d9ef1f-46fc-4176-a6f1-060f263bd03b.png "M2 confusion matrix")

# Cite Our Work
If you use the SelfCode data set, please cite [our publication](https://journals.flvc.org/FLAIRS/article/view/133385/137950): 
```bibtex
@article{Chapagain_Risha_Banjade_Oli_Tamang_Brusilovsky_RUs,
    title = {SelfCode: An Annotated Corpus and a Model for Automated Assessment of Self-Explanation During Source Code Comprehension},
    volume = {36},
    url = {https://journals.flvc.org/FLAIRS/article/view/133385},
    number = {1},
    journal = {The International FLAIRS Conference Proceedings},
    author = {Chapagain, Jeevan and Risha, Zak and Banjade, Rabin and Oli, Priti and Tamang, Lasang and Brusilovsky, Peter and Rus, Vasile}
} 
```
