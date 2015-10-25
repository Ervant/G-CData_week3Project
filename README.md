# G-CData_week3Project
Project for Getting and Cleaning Data Course

This script does the following:

1) Merges the training and the test sets to create one data set.
2) Extracts only the measurements on the mean and standard deviation for each measurement. 
3) Uses descriptive activity names to name the activities in the data set
4) Appropriately labels the data set with descriptive variable names. 
5) From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

How?

First, it sets the workind directory and loads the reshape2 and dplyr libraries.

Then, it reads all .txt files and creates labels for each table

Third, the script rbinds the subject id's and activity id's to both the test and training datasets.

Fourth, it rbinds these two datasets and to create 'my_Data' dataframe.

In order to keep the means and std. deviations, I use 'grep' to keep the columns that include these as well as the id columns.

It merges the activity id data with the mean and std. deviations to get a dataset with properly labeled columns

It melts and casts (using 'merge' and 'dcast') to  create a table with the mean values only using activity id and activity type as well as subject id and writes it to my 'clean_data' file
