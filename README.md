# Arvato Customers Analysis
## by Eduardo Burgoa

## Table of Contents

1. [Project Motivation](#project-motivation)
2. [Installation](#installation)
3. [File Descriptions](#file-descriptions)
4. [Results](#results)
5. [Acknowledgements](#acknowledgements)


## Project Motivation

Arvato Financial Solutions is one of the main divisions of Arvato, an internationally active services company subsidiary of Bertelsmann. The company offers financial services related to payments and cash flow like risk assessment or fraud management by means of predictive analytics and leading-edge platforms.

The purpose of the analysis is to gain more understanding of Arvato customers compared to Germany population. There are two main objectives:
- The first objective is to obtain customer segments of Arvato customers and analyse how customers are similar to or differ the general population at large.
- The second objective is to create a model to classify which targets of a mail campaign will be become customers.

For the first objective, obtaining customer segments, is perfect for unsupervised learning. We will use a clustering algorithm.

The second objective, the classification task. We will use supervised learning to do job. The main metric to evaluate will be ROC-AUC. This is a good metric for classification problems with class imbalance like the case (only 1,2% of samples are from positive class).


## Installation

To run this project you have to use an instance of Jupyter Notebook with python 3. 
The python libraries used in this project are:

- numpy
- pandas
- matplotlib
- sklearn
- imbalanced-learn


## File Descriptions

- **README.md**. This is the file you are reading at his moment. Its purpose is explaining the motivation of the project and helping to use it.
- **Arvato Project Workbook.ipynb**. This file is the notebook where the analyis is implemented. The notebook is oganised as follows: 
    - Part 0: Get to Know the Data
    - Part 1: Customer Segmentation Report
    - Part 2: Supervised Learning Model
    - Part 3: Kaggle Competition
    

## Conclusions

These are the main conclusions of the project:

- The dataset was challenging because it was big with 891.211 rows and 366 features. Dimensionality reduction using PCA or SelectKBest was of great help in such a dataset.

- There are some algorithms that simply does not scale well for big datasets (SVC and KNeighborsClassifier) and there are others that scale very well but its AUC scoring is not good enough (LinearSVC and SGDClassifier). In this case ensemble methods had the best performance.

- This was a highly imbalance dataset and there are some resampling techniques like SMOTE which help to improve performance.

- The final VotingClassifier model achieved a  0.80374 on the Kaggle competition.

A blog post explaining the process could be found [here](https://medium.com/@eduardo.burgoa/data-science-for-marketing-step-by-step-guide-30c1875d0bcd)



## Acknowledgements
- The dataset has been provided by Arvato Financial Solutions. This dataset was not published in thsi repository in accordance to Arvato terms and conditions.

