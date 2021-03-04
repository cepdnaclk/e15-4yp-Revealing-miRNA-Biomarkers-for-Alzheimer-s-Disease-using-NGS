---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: eYY-4yp-project-template
title:
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# Project Title

#### Team

- e15362, Hasini Thilakarathna, [email](mailto:hasinithilakarathna4@gmail.com)
- e15345, Vidwa Sripadi, [email](mailto:vidwasripadi@gmail.com)
- e15081, Imalsha Dinuwanthi, [email](mailto:imalshadinu@gmail.com)

#### Supervisors

- Dr. Damayanthi Herath, [email](mailto:damayanthiherath@eng.pdn.ac.lk)
- Prof. Roshan Ragel, [email](mailto:rosahnr@eng.pdn.ac.lk)

#### Table of content

1. [Abstract](#abstract)
2. [Related works](#related-works)
3. [Methodology](#methodology)
4. [Experiment Setup and Implementation](#experiment-setup-and-implementation)
5. [Results and Analysis](#results-and-analysis)
6. [Conclusion](#conclusion)
7. [Publications](#publications)
8. [Links](#links)

---

## Abstract

Alzheimer’s disease is recognized as one of the
common diseases found among older people, which still has no
successful cure. In this study, our goal is to determine the best set
of miRNA biomarkers which are highly differentially expressed
in Alzheimer’s disease. Using statistical analysis followed by
machine learning techniques, we establish 25 microRNAs as
biomarkers for AD. Furthermore, we provide an analysis of the
selected 25 microRNAs with area under the receiver operating
curve and classification algorithms.

## Related works


Sample selection

When detecting biomarkers for Alzheimer’s disease, initially we have to select a sample for
performing analysis. Mostly blood samples are used due to the high availability. Different
types of blood samples including whole blood [5–9], serum [10–13] and plasma [14, 15]
are used by many previous researchers where they have tried to find miRNA biomarkers.
If we use brain samples it would give most accurate results than blood samples since
AD is most prominently active in brain [16]. We would be able to give more accurate
results if both blood and brain samples are used. Samples can be taken from participants
generally as, AD and controls [6, 7, 10, 14] and also they can be taken considering the
different stages as severe, moderate, mild AD and controls [12]. Another approach in
collecting samples is taking then from participants with HC, MCI and AD [11]. The
number of samples used when developing a diagnosis method can be identified as one of
the main factors which could affect the final results. Next generation sequencing platform
is the most trending method used for gathering samples for various disease diagnosis
researches. Many techniques like Illumina sequencing technique [5, 6, 8, 10, 12, 3] are
introduced for working with NGS data. Preprocessing the raw sequence counts can be
done using a bioinformatic pipeline, which gives the read counts for each miRNA as the
final outcome.


Normalization

Normalization of sequencing read counts can be performed using several normalization
methods. Quantile normalization is one way that we can do normalization when we are
having a high dimensional dataset. It excludes selected samples to minimize noise [5, 6].
Mean normalized read counts also can be used to filter out the miRNAs. Also we can
follow a stepwise procedure to do normalization as below [12].
• From all the samples, find sequences which are common.
• Build a reference dataset using those common sequences.
• Apply logarithmic transformation
• Calculate the logarithmic difference between each sample and reference dataset.
• Form a subset by taking sequences which has a difference<2.
• Perform linear regression.
• Calculate the mid value
Looking at the results obtained from the study which used the above normalization
method, it can conclude that this type of step wise normalization method can be used
for obtaining the best set of miRNAs. Data visualization can be used for selecting which
normalization method is best suit for a given dataset.


Statistical Analysis

Initial detection of miRNA can be done by initially calculating a significance value(p
value). P value is a value between 0 and 1, which shows the level of statistical significance.
If a p value is less than the significance level (0.05), it is considered as a nominally
significant p value and we can select those miRNA as the most impacting miRNAs.

WMW test [10, 13], Wald test and Fisher’s exact test [7] can be used to calculate the p
values and these p values can be adjusted for multiple testing using an approach like
Benjamini-Hochberg approach [5, 6]. Other than that, t test and kruskal test can also
be used to calculate significance values [14].


Validation of samples

Validation of the samples makes it easier for the next steps in the investigation and
also it makes the final results more accurate. After the statistical analysis process,
for validating the obtained samples, quantitative real time-polymerase chain reaction
(qRT-PCR) method is used by many researchers. It analyzes the expression of single
miRNAs by applying the method on previously used samples for sequencing [6, 8–13].
But in a previous study [6], they have additionally included patients with AD and also
patients with other neurological disorders in the validation step, to analyze the the set
of miRNAs they obtained in the previous step. After the validation is carried out, the
miRNAs can be further filtered out to obtain the most significant miRNAs [12].


Receiver operating characteristic curves

Receiver operating characteristic curve analysis is used to evaluate the performance or
accuracy of a classification model. ROC is a plot of sensitivity against specificity for
selected samples. It is also used to initially detect the dysregulation of miRNAs and
to discriminate between AD and NC sample groups. The area under the curve is the
degree of separability. If the AUC is high, that means that particular miRNA is better
to distinguish patients with AD and control.


Feature selection and Classification

If we use a classification model without using feature selection, it will take more run time
due to the huge size with redundant features. Therefore it is required to apply some
feature selection method to reduce those redundant features. Hierarchical clustering
is a feature selection method which can be used to statistically analyze the dataset
[5, 6, 8, 9, 11]. It will build clusters of miRNAs having similar patterns. Principal
Component Analysis is another approach which can be used for the feature selection
[5, 9, 11]. Machine learning classifier models are used to predict whether a sample belongs
to AD or control. AdaboostM1, J48 decision tree, random forest and support vector 
machines and radial basis SVM are some machine learning approaches that can be used
for building prediction models. In a previously done study, they have built a separate
model by performing 7-way cross validation using 7 randomly picked partitions of 5
positive and 5 negative samples each for the feature selection.


Summary

According to the review we have done, we identified how we can use miRNAs to diagnosis
AD and what are the miRNA diagnostic biomarkers which can be found in AD patients.
In each study, for filtering out the candidate miRNA, step wise procedures including
initial detection and statistical analysis have performed. When consider about previous
studies, there are several limitations. The most common limitation of most of the research
is they used a limited number of the cohort to their experiments. It is hard to find a large
number of Alzheimer’s disease patients to do massive experiments. But we can obtain
better results if we expand the cohort size. In many studies, samples with analyzed
dementia and controls have used. But not discussing about the possibility to discover
pre-clinical biomarkers for Alzheimer disease is a limitation of most of the previous
studies. A model which was built in a one previously done study [11], does not develop
to anticipate movement from HC to MCI or MCI to AD. Also, this model was incapable
of applying for late-stage AD findings. In another study [13], they have mentioned that
they were unable to recognize a mechanism to identify the variation of miRNAs in serum
samples. Considering all the drawbacks, limitations and also the developments found in
the previous studies, in this research, we are focusing on finding a more accurate solution
for detecting AD biomarkers.


## Methodology

## Experiment Setup and Implementation

## Results and Analysis

## Conclusion

## Publications
1. [Semester 7 report](./)
2. [Semester 7 slides](./)
3. [Semester 8 report](./)
4. [Semester 8 slides](./)
5. Author 1, Author 2 and Author 3 "Research paper title" (2021). [PDF](./).


## Links

[//]: # ( NOTE: EDIT THIS LINKS WITH YOUR REPO DETAILS )

- [Project Repository](https://github.com/cepdnaclk/repository-name)
- [Project Page](https://cepdnaclk.github.io/repository-name)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

[//]: # "Please refer this to learn more about Markdown syntax"
[//]: # "https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet"
