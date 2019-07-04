# Code Book

The R-script with name `run_analysis.R` performs the data preparation as described in the project's definition.

- **Download and unzip dataset**
      - First check if files exists.
      - If not download the `.zip` file
      - Unzip the file to the folder `UCI HAR Dataset`.
      
- **Assign each data to variables**
      - `features` holds `features.txt` with 561 rows, 2 columns
      - `activity_labels` holds `activity_labels.txt` with 6 rows, 2 columns
      - `subject_test` holds `test/subject_test.txt` with 2947 rows, 1 column
      - `X_test` holds `test/X_test.txt` with 2947 rows, 561 columns
      - `y_test` holds `test/y_test.txt` with 2947 rows, 1 columns
      - `subject_train` holds `train/subject_train.txt` with 7352 rows, 1 column
      - `X_train` holds `/train/X_train.txt` with 7352 rows, 561 columns
      - `y_train` holds `/train/y_train.txt` with 7352 rows, 1 column
- **Merges the training and the test sets to create one data set**
      -`Dataset` is created by merging data `X_test`, `X_train`,`y_test`, `y_train`, `subject_test` and `subject_train` with 10299 rows, 563 columns
- **Extracts only the measurements on the mean and standard deviation for each measurement**
      - `TidyData` (10299 rows, 88 columns) is created by subsetting `Dataset`, selecting only columns: `subject`, `code` and the measurements on the `mean` and `std`.
- **Uses descriptive activity names to name the activities in the data set**
      - Entire numbers in `code` column of the `TidyData` replaced with corresponding `activity` taken from second column of the  `activity_labels` variable.
- **Appropriately labels the data set with descriptive variable names**
      - `code` column renamed into `activities`
      - All `Acc` in column’s name replaced by `Accelerometer`
      - All `Gyro` in column’s name replaced by `Gyroscope`
      - All `BodyBody` in column’s name replaced by `Body`
      - All `Mag` in column’s name replaced by `Magnitude`
      - All start with character `f` in column’s name replaced by `Frequency`
      - All start with character `t` in column’s name replaced by `Time`
      
- **From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject**
      - `TidyData2` (180 rows, 88 columns) is created by sumarizing `TidyData` taking the means of each variable for each activity and each subject, after groupped by subject and activity.
      - Export `TidyData2` into `TidyData.txt` file.

