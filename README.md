# Getting and Cleaning Data Course Project

### Course project for the Getting and Cleaning Data Coursera course.
### Dataset

The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

### Files

- `CodeBook.md` a code book that contains informations about the variables, the data, and any transformations or work that I performed to clean up the data.
- `run_analysis.R` R script that does the following:
      - Download the dataset.
      - Merges the training and the test sets to create one data set.
      - Extracts only the measurements on the mean and standard deviation for each measurement.
      - Uses descriptive activity names to name the activities in the data set.
      - Appropriately labels the data set with descriptive variable names.
      - From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
- `TidyData.txt` is the exported final data after going through all the sequences described above.# Getting-and-Cleaning-Data-Final
