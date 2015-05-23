<<<<<<< HEAD
# Getting-and-Cleaning-Data-Project 
=======
# Getting-and-Cleaning-Data-Project 
>>>>>>> fbd624b1f5bd75a9bc279dff5002d8f5b1d551f5

## Instructions of the project
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.  

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

 You should create one R script called run_analysis.R that does the following. 
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement. 
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names. 
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


===============
## The steps that are taken by run_analysis.R are: 

Install and load the following  the libraries
* library(plyr)
* library(dplyr)
* library(reshape2)

Followed by:
* read the files into tables
* get headers to put into data table in the next step
* read data into table and assign header
* read as table for handling using either cbind/rbind or dplyr
* merge data together
* find col number that contains "mean" and "std"
* pull out the columns with indexed numbers that contain "mean" and "std"
* create a new dataframe that has subjectID, activityID, and those with "mean" and "std"
* add in column with activity description by matching the activity labels
* Read all activities and their names and label the aproppriate columns, use dplyr inner_join to merge 2 tables with their common column = activityID
* because for wide format, the header has variables that is very non-intuitive and non-descriptive, thus, next is to convert them to long format. use melt from library (reshape)
* convert it to wide format and average the variables.
* Create a file with the new tidy dataset


The result is a clean data named "tidy_data_ave_variable.txt"
Thanks. 
