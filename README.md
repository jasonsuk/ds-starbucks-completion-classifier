# Starbucks Capstone Project

## Table of contents

1. [Project Motivation](#motivation)
2. [Results](#results)
3. [Installation](#installation)
4. [File description](#files)
5. [Debugging](#debug)
6. [Licensing, Authors, Acknowledgement](#others)

<br>

## Project motivation

<a id="motivation"></a>

In this project, we would like to explore how customers interact with offers sent by Starbucks and build a machine learning classifier to predict if a practicular offer should be sent or not to customers with different characteristics.

The intention is to save time and costs involved in decision making and communication by channel. Ultimately, the model is designed to improve offer completion and customer experience by sending the right offer to the right customers, which therefore will lead to better business performance.

<br>

## Results

<a id="results"></a>

The results are discussed at my personal post <a href="https://sukjh87.medium.com/a-10-minute-guide-to-understanding-and-predicting-behaviors-of-customers-using-the-starbucks-533425134e96">here</a>.

<br>

## Installation

<a id="installation"></a>

The code here basically run on the Anaconda distribution of Python (version 3.\*).

To install the Python packages used for this project, type the below in the command line, preferably in a virtual environment using conda:

    conda install -c conda-forge pandas numpy matploblib seaborn scikit-learn tqdm pickleshare

**Note:**

    tqdm: to use progressbar (wrapping interables)
    pickleshare: to save/load ML models in/from pickle file

<br>

## File description

<a id="files"></a>

The main notebook is named as `Starbucks_Capstone_notebook.ipynb` to show codes related to the project questions.

Two folders are to contain data used for the analysis.

-   `data` :

    -   json files: the original raw data (there are three)
    -   csv files: clean data saved and used for explatory analysis and modeling. `starbucks_merged.csv` is the final dataset wrangled and used for model building.

-   `models` : models trained and stored in pickle files

    | File Name            | Classifier    | Accuracy |  F1-score  |
    | -------------------- | ------------- | -------- | ---------- |
    | dtree.pkl            | Decision tree |  83.36%  |  0.82/0.84 |
    | clf_randomforest.pkl | Random forest |  83.20%  |  0.82/0.84 |    
    | logreg.pkl           | Logistic reg. |  77.89%  |  0.77/0.79 |
    | clf_linearsvc.pkl    | SVM           |  71.86%  |  0.72/0.72 |

    <br>
    <b>NOTE</b> : the performance may vary 1-2% 

    For this dataset, a classifier model built with decision tree performed the best with the accuracy of 83% and f1-score of 82% and similar performance was observed with random forest.

    On the other hand, support vector classifier (linear without kernel) did not produce a good result despite computationally expensive operations.

<br>

## Debugging

<a id="debug"></a>

No bug found yet when running the notebook.

<br>

## Licensing, Authors, Acknowledgement

<a id="others"></a>

This capstone project is completed as part of [Udacity's Data Scientist Nano Degree](https://www.udacity.com/course/data-scientist-nanodegree--nd025) program. The data and core project objectives are initially provided by the course. However, the choice of the business questions and data analysis / machine learning methods is at the discretion of the project owner.
