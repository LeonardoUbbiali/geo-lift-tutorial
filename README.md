# GeoLift tutorial

The code is a code template of the [GeoLift package](https://facebookincubator.github.io/GeoLift/) built by the Facebook Marketing Science team. 

## Objectives
* Simplify the setup and analysis for R and Geoexperiment newbies
* allow the user to import data from Google Sheets (classic use case for marketers)

The code  is divided in 3 sections

1.   R environment setup
2.   Pre-test power analysis
3.   Geo-experiment results analysis

**Disclaimer** The notebook is intended to be a simplification of the official [GeoLift package walkthorugh](https://facebookincubator.github.io/GeoLift/docs/GettingStarted/Walkthrough)

Data and code are adapted from the official Walkthrough built  with the scope of making it for people new both to R and quasi-experimental concepts typical of Synthetic Control Methods 

## Section breakdown

### 1. R Environment setup
In this section we install and load the packages required
If you don't have R installed follow this [link](https://cran.r-project.org/mirrors.html)

**Requirements**
* R environment (RStudio or a Notebook[jupyter,colab])
* R version > 4.0.0 


### 2. Pre-test power analysis
In this section we load the pre-intervention data from Google Sheets (time-series data before the launch of the campaingn) 
The schema of the dataset must have this 3 columns

| Column      | Description | Example     |
| :---        |    :----:   |          ---: |
| geo         | the granular area you are testing on (i.e. city,state,zipcode,dma)       | new york   |
| [target_metric]   | the target metric of your test (i.e. signups,revenue,orders)        |  2323     |
| date   | the date in 'YYYY-MM-DD' format        |  2021-01-17      |

With the loaded data we run the Power Analysis of the test to:
* find the optimal number of test locations
* select the best split of test and control groups
* define the best test duration
* define the Minimum Detectable Effect to obtain significant result

### 2. Geo-experiment results analysis

In this section we load the full dataset from Google Sheets (time-series dataset containing both pre and post campaign launch data) 
The schema of the dataset must be the same of the data loaded in the previous section

With the loaded data we run the Power Analysis of the test to:
*  analyze the results of the test 
*  explore the test results to visualize the impact (if any)

