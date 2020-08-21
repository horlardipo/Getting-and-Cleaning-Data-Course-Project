The run_analysis.R script shows the process of data preparation and the codes for the 5 questions in the asignment

Dataset download
Dataset downloaded and extracted under the folder called UCI HAR Dataset and file extraction

Create Data frames from the file

dataSubjectTest  - dim(dataSubjectTest)
                    [1] 2947    1
dataSubjectTrain -  dim(dataSubjectTrain)
                    [1] 7352    1
dataActivityTest  - dim(dataActivityTest)
                    [1] 2947    1
                    
dataActivityTrain - dim(dataActivityTrain)
                    [1] 7352    1
                    
dataFeaturesTest  - dim(dataFeaturesTest)
                  [1] 2947  561
dataFeaturesTrain - dim(dataFeaturesTrain)
[1] 7352  561



1. Merges the training and the test sets to create one data set
The rbind and cbind function was used to merge the data to create one data set

2. Extracts only the measurements on the mean and standard deviation for each measurement
Data is created using the grep (search) command by subsetting Data, selecting only columns: subject, code and the measurements on the 
mean and standard deviation (std) for each measurement

3. Uses descriptive activity names to name the activities in the data set
Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of the activities variable

4: Appropriately labels the data set with descriptive variable names.
Columns of "Data" replaced with corresponding activity taken from second column of the activities variable

5: From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Final Data (data2) is created into a table
