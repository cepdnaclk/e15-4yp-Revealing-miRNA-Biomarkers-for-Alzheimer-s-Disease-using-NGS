---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: e15-4yp-Revealing-miRNA-Biomarkers-for-Alzheimer-s-Disease-using-NGS
title: Revealing miRNA Biomarkers for Alzheimer's Disease using Next Generation Sequencing data
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
4. [Results and Analysis](#results-and-analysis)
5. [Conclusion](#conclusion)
6. [Publications](#publications)
7. [Links](#links)

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
* From all the samples, find sequences which are common.
* Build a reference dataset using those common sequences.
* Apply logarithmic transformation
* Calculate the logarithmic difference between each sample and reference dataset.
* Form a subset by taking sequences which has a difference<2.
* Perform linear regression.
* Calculate the mid value
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

Following Figure shows a summary of different methods used andthe results obtained in previous studies. According to this diagram, only 4 studies haveused machine learning algorithms and only 5 studies have used statistical methods intheir studies. Out of the results obtained from above mentioned 9 studies, 7 miRNAswere identified as common for those 9 studies.

![Figure 02](https://github.com/cepdnaclk/e15-4yp-Revealing-miRNA-Biomarkers-for-Alzheimer-s-Disease-using-NGS/blob/main/docs/Related_venn_diagram.png)


## Methodology

Data collection

We used a data set available in National Center for Biotechnology Information (NCBI) database under the access number
GSE46579. It includes 70 samples with 22 control and 48 AD
and 2652 miRNAs.

Preprocessing

The Next Generation Sequencing data preprocessing was
done using the Galaxy platform. Galaxy is a web-based, 
opensource platform for scientific data analysis. First, the quality
report of sequencing data was generated using the FastQC
tool. Then, using the tool Trim Galore, data trimming was
performed. The package Trim Galore allows both quality
trimming and adapter trimming at once. Low-quality reads and
adapters were removed from sequence read in the trimming
procedure. Trimming increases the quality of sequences. Next,
the data filtering procedure was performed using the Filter
FASTQ tool. Short read sequences and low-quality sequences
were removed in filtering. After that, the NGS reads were
mapped against a reference genome (h38) using Bowtie2.
Bowtie2 tool aligns sequences to the long reference sequences.
Then, the reads were mapped against the hsa.gff3 miRNA
precursor sequences from the miRBase database (v22) and
the number of read counts of each miRNA was found using
the htseq-count tool. This preprocessing procedure was done
for every sample using the galaxy platform and then the
summarized dataset was created with miRNA read counts of
each sample. For the analysis purposes we used a data set with
highly abundant miRNAs. To do that we considered miRNAs
with read counts less than 50 across all samples of AD and
control separately, as lowly abundant and removed them from
the data set. Considering the mean distribution of the data
set, we normalized the data set using quantile normalization
technique instead of general normalization technique.

Statistical Analysis

Normalized data set obtained from the previous stage was
further analyzed with significance value and fold change to
reduce the number of features. We calculated the pValues for
each miRNA using Wilicoxon-Mann-Whitney (WMW) test.
Generally, fold change is a technique which is used to get
an idea of how much change occurs going from one value
to another. In this project we tried to get fold change values
(log2) for each miRNA, to check the significant changes of
each miRNA across AD and control samples. We used cut
off values for pValues and fold changes values as 0.05 and
1 respectively, to obtain the highly expressed set of miRNAs.
For each of those filtered features, we calculated the AUC
values. Using those AUC values, another set of features were
filtered out. Features with AUC score less than or equal to 0.5
were ignored as they don’t make a significant impact on the
classification of the data set.

Feature Selection

Initially we used two different methods as PCA and Random
Forest for selecting the best set of features. For the data
set we obtained from the previous stage, we separately did
PCA analysis and Random Forest analysis. Univariate feature
selection method was used to decide how many features we
needed to select from each. Features which have a significant
relationship with the class value were identified from this
univariate feature selection method. Next, the set of overlapped
miRNAs from those two methods was identified as the best set
of features which could be obtained from this part of feature
selection. In the next part of the feature selection stage, we
used correlation coefficient. As the correlation coefficient, we
used Pearson correlation coefficient (Figure 1).

![Figure 01](https://github.com/cepdnaclk/e15-4yp-Revealing-miRNA-Biomarkers-for-Alzheimer-s-Disease-using-NGS/blob/main/docs/Feature_Selection.png)

Classification

Classification accuracy was used to see how accurate our
predictions were. A set of machine learning algorithms were
modelled for the initial data set and out of those the most
accurate algorithms were identified. Those each pre-identified
algorithms were used for obtaining the classification accuracy
of the final data set with biomarker miRNAs.

Validation

For validating the results we used Human MiRNA Disease
Database version 3.2 (HMDD v3.2). HMDD contains a large
set of miRNAs and related diseases collected from the literature. There are 35547 miRNA-disease associations in version
3.2 and it includes 1206 miRNAs, 893 diseases from 19280
related publications.


## Results and Analysis

At the end of the preprocessing stage, a data set with
513 highly abundant miRNAs was obtained after removing
miRNAs with less than 50 read counts across all samples.
Considering the cut-off significance value as 0.05 and fold
change (log2) as 1, the number of features were reduced up to 228.
With the AUC analysis we further reduced the number of
miRNAs and at the end of the statistical analysis, we identified
219 miRNAs as a set of highly expressed miRNAs. From the
univariate feature selection method, we identified 50 miRNAs
which have a significance relationship with class value. We
identified 14 common miRNAs from two sets of miRNAs
selected from PCA and random forest analysis. 
They are hsa-miR-186-5p, hsa-miR-144-3p, hsa-miR-151a-3p,
hsa-miR-99b-5p, hsa-miR-98, hsa-miR-148a-3p, hsa-let-7g-5p, 
hsa-let-7f-5p, hsa-let-7a-5p, hsa-miR-30d-5p, hsa-miR-15a-5p,
hsa-miR-589-5p, hsa-miR-144-5p, and hsa-let-7f-5p.
We used heat maps for making a judgement on the correlation of each features obtained from previously mentioned two
methods. Figure 2 and Figure 3 show how different features obtained from PCA and Random Forest analysis, are correlated.
With the help of the heat maps, we decided to use 36 less
correlated features for further analysis using correlation coefficients. Out of the different machine learning algorithms which
we modelled for our initial data set, we identified the three
most accurate algorithms namely, Support Vector Machine,
Logistic Regression and Random Forest. For the data set with
the 36 miRNAs, we calculated classification accuracy using
those three models by varying the correlation coefficients. For
each model we identified a correlation coefficient which gave
the highest accuracy. Fig. 4 shows the plots with correlation
coefficient against the classification accuracy of three models The three correlation coefficients were 0.9975, 0.5875 and
0.5300 for SVM, Logistic Regression and Random Forest
respectively. Using those 3 correlation coefficients, three sub
sets of miRNAs were obtained from the earlier used 36. As we
calculated classification accuracy for the previously mentioned
three subsets, we identified 11 miRNAs which provided the
highest classification accuracy. They are, hsa-miR-4781-3p, brain-miR-112, hsa-let-7a-5p,
hsa-miR-148b-5p, hsa-miR-29b-3p, brain-miR-431, hsa-miR-378a-5p, hsa-miR-548h-5p, hsa-miR-3909, 
hsa-miR-625-5p, and hsa-miR-24-3p.



## Conclusion

In this report we have discussed about how to detect miRNA biomarkers for Alzheimer’s disease using next generation sequencing. Initially we have discussed about the need of a solution to identify Alzheimer’s disease in the early stage. Then we have mentioned about the literature review we have done. When we were doing the literature review, we have identified several miRNA biomarkers in different studies which used NGS. In these studies there were some limitations.
   In our approach so far, initially we have taken samples from participants with AD and control. Then samples were preprocessed and statistically analyzed. Significance values were calculated using Wilcoxon-Mann-Whitney (WMW) test. Also we have used ROC analysis. Using this procedure, here we have identified a set of significant miRNAs for AD. Using PCA, Random Forests and Correlation coefficient we identified 25 biomarker miRNAs for AD. In the next phase we validated the the result using HMDD v3.2. 
 Leidinger et al., who have carried out a different method to find biomarkers using the same data set, have stated that they have obtained an accuracy of 93.3\% where we obtained an accuracy of 95.24\%. Addition to that we evaluated the results with specificity, sensitivity and AUC values as discussed previously. In addition to diagnosis of AD patients with the final set of biomarkers, the followed methodology can be used to identify different cures for other neurological diseases including AD, by effortlessly analyzing various data sets.

## Publications
1. [Semester 7 report](./)
2. [Semester 7 slides](./)
3. [Semester 8 report](./)
4. [Semester 8 slides](./)
5. Author 1, Author 2 and Author 3 "Research paper title" (2021). [PDF](./).


## Links

[//]: # ( NOTE: EDIT THIS LINKS WITH YOUR REPO DETAILS )

- [Project Repository](https://github.com/cepdnaclk/
e15-4yp-Revealing-miRNA-Biomarkers-for-Alzheimer-s-Disease-using-NGS )
- [Project Page](https://cepdnaclk.github.io/
e15-4yp-Revealing-miRNA-Biomarkers-for-Alzheimer-s-Disease-using-NGS )
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

[//]: # "Please refer this to learn more about Markdown syntax"
[//]: # "https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet"
