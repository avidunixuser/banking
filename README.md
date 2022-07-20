# Portuguese Banking Institution - Marketing Campaign - Subscription of Term Deposit Prediction

## CRISP-DM Framework

- To frame the task, throughout our practical applications we will refer back to a standard process in industry for data projects called CRISP-DM.  
- This process provides a framework for working through a data problem.  
- Your first step in this application will be to read through a brief overview of CRISP-DM

- This application makes use of CRISP-DM framework

<center>
    <img src = images/crispdm.png width = 100%/>
</center>

## Data Set Information:

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

#### Business Understanding

Bank Marketing Data Set
Download: <a href = "https://archive.ics.uci.edu/ml/machine-learning-databases/00222/"> Data Folder </a> , <a href = "https://archive.ics.uci.edu/ml/datasets/bank+marketing#"> Data Set Description</a>

Abstract: The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).

Data Set Characteristics:  Multivariate
Number of Instances: 45211
Area: Business
Attribute Characteristics: Real
Number of Attributes: 17
Date Donated: 2012-02-14
Associated Tasks: Classification
Missing Values? None

#### Source:

[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014

#### There are four datasets:
1) bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010), very close to the data analyzed in [Moro et al., 2014]
2) bank-additional.csv with 10% of the examples (4119), randomly selected from 1), and 20 inputs.
3) bank-full.csv with all examples and 17 inputs, ordered by date (older version of this dataset with less inputs).
4) bank.csv with 10% of the examples and 17 inputs, randomly selected from 3 (older version of this dataset with less inputs).
The smallest datasets are provided to test more computationally demanding machine learning algorithms (e.g., SVM).

#### The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

#### Relevant Papers:

S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014
S. Moro, R. Laureano and P. Cortez. Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology. In P. Novais et al. (Eds.), Proceedings of the European Simulation and Modelling Conference - ESM'2011, pp. 117-121, Guimaraes, Portugal, October, 2011. EUROSIS. [bank.zip]

#### Citation Request:

This dataset is public available for research. The details are described in [Moro et al., 2014].
Please include this citation if you plan to use this database:

[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014

## Data Understanding

#### Attribute Information:
<pre>
1 - age (numeric)
2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired',
                                    'self-employed','services','student','technician','unemployed','unknown')
3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
5 - default: has credit in default? (categorical: 'no','yes','unknown')
6 - housing: has housing loan? (categorical: 'no','yes','unknown')
7 - loan: has personal loan? (categorical: 'no','yes','unknown')
</pre>
#### related with the last contact of the current campaign:
<pre>
8 - contact: contact communication type (categorical: 'cellular','telephone')
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target 
     (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. 
     Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
</pre>
#### other attributes:
<pre>
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
14 - previous: number of contacts performed before this campaign and for this client (numeric)
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')
</pre>
#### social and economic context attributes
<pre>
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)
17 - cons.price.idx: consumer price index - monthly indicator (numeric)
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)
19 - euribor3m: euribor 3 month rate - daily indicator (numeric)
20 - nr.employed: number of employees - quarterly indicator (numeric)
</pre>
#### Output variable (desired target):
<pre>
21 - y - has the client subscribed a term deposit? (binary: 'yes','no')
</pre>
#### The data is clean and there are no NaN values.
<pre>
    - age          45211
    - job          45211
    - marital      45211
    - education    45211
    - default      45211
    - balance      45211
    - housing      45211
    - loan         45211
    - contact      45211
    - day          45211
    - month        45211
    - duration     45211
    - campaign     45211
    - pdays        45211
    - previous     45211
    - poutcome     45211
    - y            45211
</pre>
## Team collaboration - directory structure

#### Instructions
<pre>
- Clone the GitHub repository
- Please run the notebooks in sequence
- At the end of the step 3, there will be 4 model pkl files.

├── data
│    ├── bank_full_raw.csv   
│    ├── bank_curated_data.csv  
|    ├── bank_enriched_data.csv
├── models
|    ├── decision_tree.pkl 
|    ├── kneighbor.pkl
|    ├── linear_regression.pkl
|    ├── support_vector_machine.pkl
├── results
|    ├── model_performance_table.csv
|    ├── model_performance_with_estimators.csv
├── 1. Exploratory Data Analysis.ipynb
│   2. Data Processing.ipynb
|   3. Modeling and Deployment.ipynb
|   4. All_in_PySpark.ipynb
├── presentation
|   ├── PortugueseBank_DataScience_Report.pptx

</pre>

## Data Preparation and Visulalization
<pre>
Input: bank-full-raw.csv
Output: bank_curated_data.csv
Code Used: Python
Packages: Pandas, Numpy, Matplotlib, Seaborn
</pre>
## Data Cleansing and processing
<pre>
Input: bank_curated_data.csv
Output: bank_enriched_data.csv
Code Used: Python
Packages: Pandas, sklearn
</pre>
- LabelCondoding to transform categorical variables
- Estimators (Decision Tree Classifier, Linear Regression Classifier, KNeighbors Classifier, Support Vector Classifier)
- cross_val_score of calculated MSE
- Normalization
- Data Scaling
- Sequential Feature Selection (forward/backwd)
- train_test_split

## Data Modeling and Model Deployment
<pre>
Input: bank_enriched_data.csv
Output: Model

    1) Decision Tree Regression
    2) K-Neighbors Regression
    3) Linear Regression
    4) Support Vector Machine
</pre>

## Process Summary
<pre>
- By performing different ML models, we aimed to get a better result or less error with max accuracy. 

- From the table below, Decision Tree, KNeighbor, Logistrics Regression, and Support Vector Machine algothims were evaluated. 
- Two tables indicate - Decision Tree method is the most optimum in terms of predicting the acceptance of subsciption of term deposite 
  based on the direct marketing campaign efforts.
</pre>
## Features that influenced the prediction

<center>
    <img src = "images/Feature_Importance.png" width = 100%/>
</center>

## Model Score Table

<center>
    <img src = "images/ScoreTable.png" width = 100%/>
</center>

## Confusion metrics

<center>
    <img src = "images/Confusion_metrics.png" width = 100%/>
</center>

## Model perforamance

<center>
    <img src = "images/Performance_with_estimators.png" width = 100%/>
</center>

## Model Performance - Graphical representation

<center>
    <img src = "images/Overall_Performance.png" width = 100%/>
</center>
