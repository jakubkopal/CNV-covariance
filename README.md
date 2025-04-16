# Code supplement to the CNV covariance study

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![DOI](https://img.shields.io/badge/DOI-10.1101%2F862615-informational
)]([https://doi.org/10.1101/2024.05.21.24307729](https://doi.org/10.1101/2024.05.21.24307729))

This repository contains the code used to process and analyse the data presented in the "A pattern-learning algorithm associates copy number variations with brain structure and behavioral variables in an adolescent cohort" paper. In addition, it also contains associated figures.

## Abstract
<div style="margin-left: 40px;" align="justify">
Our genetic makeup, together with environmental and social influences, shape our brain's development. Yet, the imaging genetics field has struggled to integrate all these modalities to investigate the interplay between genetic blueprint, brain architecture, environment, human health, and daily living skills. Here, we interrogate the Adolescent Brain Cognitive Development (ABCD) cohort to outline the effects of rare high-effect genetic variants on brain architecture and their corresponding implications on cognitive, behavioral, psychosocial, and socioeconomic traits. We design a holistic pattern-learning algorithm that quantitatively dissects the impacts of copy number variations (CNVs) on brain structure and 938 behavioral variables spanning 20 categories in 7,338 adolescents. Our results reveal associations between genetic alterations, higher-order brain networks, and specific parameters of the family well-being, including increased parental and child stress, anxiety and depression, or neighborhood dynamics such as decreased safety. We also find effects extending beyond the impairment of cognitive ability or language capacity which have been previously reported. Our investigation spotlights the interplay between genetic variation and subjective life quality in adolescents and their families.
</div>

## 

<c>![Figure 1](https://github.com/jakubkopal/CNV-covariance/blob/main/figures/fig1.png)</c>


Figure 1

**Genome-wide CNVs impact brain-behavior relationships across distinct modes of population covariation**

<div align="justify">
A) Genome-wide CNV identification in the ABCD population cohort. We investigated 7,657 children from the ABCD database. In total, 5,535 children do not carry any protein-coding CNV, 514 carry a deletion and 1,472 carry a duplication fully encompassing one or more genes. 136 participants carried both deletion and duplication. The ratio of males and females is similar in every group (left plot, inner circle). The age of participants is similar across different CNV groups (right plot). B) CNV characteristics. The most common kind of CNV is a deletion/duplication encompassing a few genes. On average, duplications contain more genes than deletions in the ABCD cohort. C) Partial least squares model links the brain with behavior in one holistic model. We estimate a multivariate relationship structure among 148 brain atlas volume measures and ∼1000 behavior measures spanning 20 categories based on measurements from children without any CNV. The canonical scores represent the latent variable expressions calculated from linear combinations of the original brain and linear combinations of behavior measurements that maximize the covariance between the two sets of variables. k is the number of phenotypes per category. D) CNV status impacts individual expression strengths of brain and behavior patterns. We compared the average brain and behavior scores for CNV carriers with control participants not used to derive model parameters (i.e., controls not seen by the model during training). Stars denote significant differences based on cross-validation testing (cf. Methods). These results reveal that carrying a CNV significantly impacts canonical scores across different modes of brain-behavior covariation, emphasizing the utility of a multivariate holistic framework that cuts across single disciplines.
</div>


## Resources and Scripts
All figures used in the articles are in the `figures` folder. Findings from the article are based on the analysis scripts in the `scripts` folder.

1.   `scripts/a1_parameters_PLS.ipynb` is an analysis script designed to find the optimal number of PLS dimensions.
2.   `scripts/a2_PLS_score_differnce.ipynb` uses cross-validation and permutaiton testing to quantify the differences between controls and CNV carriers.
3.   `scripts/a3_PLS_loadings.ipynb` is an analysis script to investigate and visualize PLS loadings.
4.   `scripts/a4_PLS_scores.ipynb` is an analysis script to investigate and visualzie PLS scores.
5.   `scripts/a5_PLS scores_annotation.ipynb` is an analysis script that quantifies associations between PLS scores and gene annotations.
6.   `scripts/a5_PLS scores_covariates.ipynb` is an analysis script that quantifies associations between PLS scores and covariates.
7.   `scripts/a6_PLS scores_shift.ipynb` is an analysis script to investigate the shift in PLS scores between baseline and follow-up measurements.
