# Human Activity Recognition Data Analysis

This R program analyzes the Human Activity Recognition (HAR) dataset to create a tidy dataset with aggregated means of selected variables. The analysis involves merging, cleaning, and summarizing the original data to provide insights into human activity patterns.

## Usage

1. **Download the Dataset:**

   - Before running the program, ensure you have the HAR dataset by downloading the ZIP file from the provided link.

     ```R
     library(dplyr)

     filename <- "Coursera_Week4_FinalAssignment.zip"

     if (!file.exists(filename)) {
       fileURL <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
       download.file(fileURL, filename, method = "curl")
     }

     if (!file.exists("UCI HAR Dataset")) {
       unzip(filename)
     }
     ```

2. **Run the Analysis:**

   - Execute the main analysis script to process and clean the data, creating a tidy dataset.

     ```R
     # Load required libraries and functions
     library(dplyr)

     # ... (rest of your code)
     ```

3. **Output:**
   - The resulting tidy dataset will be saved in a file named `tidy_data.txt`.

## Code Book

### Variables

1. **subject:**

   - Identifier for the subject who performed the activity.

2. **activity:**

   - Descriptive name for the activity performed by the subject.

3. **Other Variables:**
   - Various variables representing mean and standard deviation measurements. See the original `features.txt` file for detailed information on these variables.

### Transformations

- The following transformations were applied to enhance variable names for better readability:
  - `Acc` → `Accelerometer`
  - `Gyro` → `Gyroscope`
  - `BodyBody` → `Body`
  - `Mag` → `Magnitude`
  - `^t` → `Time`
  - `^f` → `Frequency`
  - `tBody` → `TimeBody`
  - `-mean()` → `Mean`
  - `-std()` → `STD`
  - `-freq()` → `Frequency`
  - `angle` → `Angle`
  - `gravity` → `Gravity`

## Output

The final tidy dataset is stored in the file `tidy_data.txt`. This file contains the aggregated means of selected variables grouped by subject and activity.
