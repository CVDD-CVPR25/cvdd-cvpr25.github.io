---
layout: default
title: Computer Vision for Drug Discovery <br> Where Are We and What is Beyond?
description: Cell line transferability challenge 
---

## Cell line transferability challenge 

### Overview

In this challenge, you will develop machine learning models for learning representations of molecular perturbations in cellular systems using microscopy imaging data.

More details on [kaggle](https://www.kaggle.com/competitions/cell-line-transferability-challenge-cvdd)

### Description

Learning representations of molecular perturbations in cells is a crucial task in drug discovery. Having robust representations that capture how certain perturbations affect cells would allow us to rapidly find compounds that present similar effects. However, experimental and other types of variability unrelated to the perturbation’s biological effect make it a challenging task. Therefore, we present a compound classification task where models will be evaluated both in unseen plates and unseen cell lines. 

### Dataset

The competition will use the publicly available 2020_11_04_CPJUMP1 dataset, see [description](https://github.com/jump-cellpainting/2024_Chandrasekaran_NatureMethods). The dataset contains images generated using chemical and genetic perturbation and 2 cell lines: U2OS and A549 in multiple replicates. Images and corresponding CellProfiler features are available. 

### Task
Develop a method for transfer of information between cell lines using either CellProfiler features or raw images (Deep Learning method). The representations will be evaluated in a set of 24 plates that contain compound-perturbed cells.

In the file metadata_test.csv, one can find the column ID, which identifies each sample for which participants should submit representations and their corresponding plate and well.

The input file should be a csv file and contain a column called ID, which matches the plate and the well from the metadata_test.csv file, and a set of float columns that will be the features. The set of feature columns can have any length and will be used in the given order. There should be only one feature value per column. Features should not have any missing or infinite values.

### Files
metadata_test.csv - Identifier of the samples that should be submitted, along with their corresponfing plates and well positions

sample_submission.csv - A sample submission file in the correct format

Features should not have any missing or infinite values. 

#### Columns

ID - Sample identifier, that corresponds with the plate and well in metadata_test.csv

feature_1 - First feature

…

feature_N - Last feature

#### References
Chandrasekaran, S.N., Cimini, B.A., Goodale, A. et al. Three million images and morphological profiles of cells treated with matched chemical and genetic perturbations. Nat Methods 21, 1114–1121 (2024). https://doi.org/10.1038/s41592-024-02241-6

### Evaluation

The generated representations will be evaluated in a compound classification task using the kNN algorithm in 5-fold cross-validation. Metrics will be calculated using inter and intra cell line matching. Train/test split will be undisclosed but follows plate-wise split. Evaluation will be performed using only compound plates of 2020_11_04_CPJUMP1 dataset and will omit DMSO well but any data can be used to develop and train a method. Participants will also be asked to send a paper describing the methodology (up to 4 pages without citations).

Inter and intra cell line matching:
- Train using U2OS data, evaluate using U2OS data.
- Train using U2OS data, evaluate using A549 data.
- Train using A549 data, evaluate using U2OS data.
- Train using A549 data, evaluate using A549 data.

The evaluation system will be opened on February 15th 2024.

### Outcomes

Teams that will obtain the best results may be invited to collaborate on a joint publication. 

### Timeline:

Start (call for participation): January 20 '25 07:59 AM UTC

Registration deadline: February 22 '25 07:59 AM UTC

Submission deadline: April 1 '25 07:59 AM UTC

Decisions to participants: May 1 '25 07:59 AM UT

## Challenge organizers:

| ![Adriana Borowa](./Ada.png) | **Adriana Borowa** <br> **Ardigen SA** | 
|:-----------------:|:-----------------:|
| ![Ana Sanchez-Fernandez](./Ana.png) | **Ana Sanchez-Fernandez <br> Johannes Kepler University Linz** | 

[back](./)
