Getting and Cleaning Data Course Project
========================================

The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set using R.

## About the dataset

This work is based on the "Human Activity Recognition Using Smartphones Dataset" Version 1.0 : http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Files in the project

The project contains the following files:

* `./datasets/UCI HAR Dataset`: Human Activity Recognition Using Smartphones Dataset Version 1.0.
* `README.md`: description of the steps for perfoming the dataset analysis. 
* `CodeBook.md`: indicate all the variables and summaries calculated, along with units, and any other relevant information.
* `run_analysis.R`: R scripts performing the analysis on the dataset.

## Run the analysis of the dataset

In order to perfom the analysis of the "Human Activity Recognition Using Smartphones Dataset" you need to run the `run_analysis.R` R script. For that you need to call the function `Analysis()`. The analysis will perform the following steps:

1. Merges the training and the test sets to create one data set.
1. Extracts only the measurements on the mean and standard deviation for each measurement.
1. Uses descriptive activity names to name the activities in the data set
1. Appropriately labels the data set with descriptive variable names.
1. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

### Additional libraries

The script uses `dplyr` library

```r
library(dplyr)
```

### Fast getting started

All you need to do is to run the `run_analysis.R` script.

```r
source("run_analysis.R")
RunAnalysis()
```
The scripts writes a `tidy.txt` which is the result of the cleaning of the initial Human Activity Recognition Using Smartphones Dataset. The output file containis 180 rows and 68 columns. The description of the data in the file can be found in the [CodeBook.md](https://github.com/shikhardhwaj/Importing-and-Cleaning-of-SmartPhone-Data/blob/master/CodeBook.md) file.

### Detailed analysis steps

The `run_analysis.R` script performs the following analysis steps

####Firstly files are read then labels are merged.After that subject Id's are read and merged.Training and testing data are combined.Then training and testing experimental files are read and combined.Then combined data is cleaned.Only mean value columns are kept .Data is grouped and summarised with mean function.Result we have is tidyData .We write it to tidy.txt.