## CodeBook.md
+Original files

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  CodeBook.md
Original files

The experiments have been carried out for 30 volunteers, 19-48 years old.  Each participant performed 6 activities
(Walking, Walking_Upstairs,Walking_downstairs, Sitting, Standing and Laying) wearing a smartphone, Galaxy SII, on the waist.
The embedded acceleraometer and gyroscope captured 3-axial linear accelerations and 3-axial angular velocity at a constant
rate of 50Hz.
The sensor signals were preprocessed with noise filters and sampled in fixed width sliding windows of 2.56 sec and 50% 
overlap.

+ Data Files
The following folders/files are available:
test
train
activity labels
features / features_info

# The Transformations
+ Merging train and test datasets
+ Extract the mean and Std. deviation for each measurement
+ Use desciptive activity names to name activities in the dataset
+ Appropriately label the dataset
+ Create a second, independent tidy_data dataset with the average of each variable for each activity and ech subject.

# Code implements these steps:
+ Before running the code, install.packages("reshape2"); install.packages("data.table")
+ Load both test and train data
+ Load the features and activity labels
+ Extract the mean and std. deviation column names and data
+ Process the data first for the test data and repeat the process for the train data.
+ Merge the test and train data
+ Apply mean function to dataset using dcast function from 'reshape2'
+ Save data as the second independent dataset 'tidy_data' using write.table


