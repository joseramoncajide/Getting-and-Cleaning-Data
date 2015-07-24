# Introduction

About the `run_analysis.R` script.

* First, data is merged using the `rbind()` function. 
* Then, only those columns with the mean and standard deviation measures are taken from the whole dataset. 
* After extracting these columns, they are given the correct names, taken from `features.txt`.
* We take the activity names and IDs from `activity_labels.txt` and they are substituted in the dataset.
* On the whole dataset, those columns with vague column names are corrected.
* Finally, we generate a new dataset with all the average measures for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called `tidy_data.txt`.

# Variables

* `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` contain the original data.
* `x_data`, `y_data` and `subject_data` merge the previous datasets.
* `features` contains the correct names for the `x_data` dataset, which are applied to the column names stored in `mean_and_std_features`, a numeric vector used to extract the desired data.
* `all_data` merges `x_data`, `y_data` and `subject_data` in a new dataset.
* `averages_data` contains the relevant averages which will be later stored in the `.txt` file.
