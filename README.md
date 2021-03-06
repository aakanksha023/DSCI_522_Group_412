# DSCI_522_Group_412

# Proposal: Credit application predictor

Author(s): Clark Alistair, Dimri Aakanksha, Jiang Yue

Demo of a data analysis project for DSCI 522 (Data Science workflows); a course in the Master of Data Science program at the University of British Columbia.

## Motivation and Research question

As the number of credit card applications increases dramatically these days, it would alleviate the burden of personals of financial institutions, if a well-trained algorithm can predict credit card application results. The purpose of our analysis is to answer the question: **"Given certain personal features, will the person’s credit card application be approved or not?"**

## Description of the Data

The Credit approval dataset is taken from the archives of the machine learning repository of University of California, Irvine (UCI). A quick review of the dataset, shows that all of the values in the dataset have been converted to meaningless symbols to protect the confidentiality of the data. However, to make the analysis intuitive and easy to understand, we gave the variables working names based on the type of data. **Note:** This is an important limitation of our analysis that doesn't affect prediction accuracy, but makes it difficult to interpret the EDA and feature importances of our model.

More information about the dataset can be found [here](http://archive.ics.uci.edu/ml/datasets/credit+approval).

## Analysis Approach

For our analysis we took the following steps:

- Complete exploratory analysis by creating several data visualizations to understand the underlying data and relationships between variables
- Perform data transformations like appropriate handling of missing values, standardising numerical features, encoding categorical features etc.
- Apply predictive classification models to answer the research question, including Random Forests, XGBoost, and LGBM.

## Final Report
The final report can be found [here](https://github.com/UBC-MDS/DSCI_522_Group_412/blob/master/doc/Report_final.md).

## Usage

There are two ways to run this analysis:

#### 1. Use Docker

*Note: the following instructions depend on running this in a unix shell (e.g., terminal or Git Bash). Windows users may have to use Git Bash, set Docker to use Linux containers, and have shared their drives with Docker.*

To replicate the analysis, please follow the instruction:

1. Install [Docker](https://www.docker.com/get-started)
2. Clone this GitHub repository
3. Download the docker image using the following command at the command line/terminal:

```
docker pull yuejiang001/dsci_522_group_412_credit_predictor:v1.0
```

4. To replicate the analysis, navigate to the root directory of this project using the command line/terminal, and run the following command:

```
docker run --rm -v /$(pwd):/home/DSCI_522_Group_412 yuejiang001/dsci_522_group_412_credit_predictor:v1.0 make -C 'home/DSCI_522_Group_412' all
```

5. To reset this repository to a clean state, with no intermediate or results files, run the following command at the command line/terminal from the root directory of this project:

```
docker run --rm -v /$(pwd):/home/DSCI_522_Group_412 yuejiang001/dsci_522_group_412_credit_predictor:v1.0 make -C 'home/DSCI_522_Group_412' clean
```

#### 2. Without using Docker

To replicate the analysis, clone this GitHub repository, install the dependencies listed below, and run the following commands at the command line/terminal from the root directory of this project:

```
make all
```

To reset this repository to a clean state, run the following command at the command line/terminal from the root directory of this project:

```
make clean
```

Full scripts of this analysis can be found [here](https://github.com/UBC-MDS/DSCI_522_Group_412/tree/master/src).

## Dependencies
Python 3.7.3 and Python packages:

- docopt==0.6.2     
- requests==2.22.0     
- pandas==0.24.2  
- numpy==1.17.2
- scikit-learn==0.22.1 
- lightgbm==2.3.2
- altair==3.2.0
- xgboost==0.90
- matplotlib==3.1.1

R version 3.6.1 and R packages:    
- knitr==1.27.2
- tidyverse==1.2.1
- GGally==1.4.0
- cowplot==1.0.0

GNU make 3.81

## Dependency diagram
![Dependency diagram](Makefile.png)

## References
**Data Source:**    
Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

