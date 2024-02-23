This Repository contains all the Files required for the Course assignment submission for getting and cleaning data

Goal of the Project
1) A tidy data set
2) A link to a Github repository with your script for performing the analysis
3) A code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.
4) Analysis R Script


Dataset:
Human Activity Recognition Using Smartphones

Variables Used:
features: contains column names from features.txt"
activityLabels: contains column names from activity_labels.txt
Xtrain: contains column names from X_train.txt 
ytrain: contains column names from y_train.txt
subjectTrain: contains column names from subject_train.txt
Xtest: contains column names from X_test.txt
ytest: contains column names from y_test.txt
subjectTest: contains column names from subject_test.txt 
XData: row bind train data of X
yData: row bind train data of y
subjectData: row bind data of subject

Files:
CodeBook.md a code book that describes the variables, the data, and any transformations or work that I performed to clean up the data

run_analysis.R performs the data preparation and then followed by various steps required to produce final output
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
FinalTidyData.txt is the exported final data after going through all the sequences described above.

some notes on run_analysis.R

 Merges the training and the test data sets to create one data set (such as): Load and read the input raw sets; merge three pairs data set (e.g.: X_train.txt, X_test.txt; y_train.txt, y_test.txt; subject_train.txt, subject_text.txt) into three single data set via "rbind" function.

Extracts only the measurements on the mean and standard deviation for each measurement. This step is mainly done by the "grep" function by providing the key search patterns "-mean()|-std()".


Label column renamed to Activity
All Acc in column’s name replaced by Accelerometer
All Gyro in column’s name replaced by Gyroscope
All BodyBody in column’s name replaced by Body
All Mag in column’s name replaced by Magnitude
All start with character f in column’s name replaced by Frequency
All start with character t in column’s name replaced by Time

RENAMED FilterdData to TidyDataSet


FinalTidyDataSet (180 rows, 81 columns) is created by sumarizing TidyData taking the means of each variable for each activity and each subject, after groupped by subject and activity.
Export FinalTidyDataSet into FinalTidyData.txt file.

