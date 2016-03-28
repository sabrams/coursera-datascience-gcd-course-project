The "UCI HAR Dataset" contains, at its root directory, contains the following

* activity_labels.txt - a mapping of activity names for activity numbers, where numbers are used in test and train data
* features.txt - a description of the features being recorded and analized
* features_info.txt - additional data about how the feature data was obtained
* README.txt - intro to the project and data

In each of the test and train directories, there are the following

* X_{test|train}.txt - feature data, each row is data recorded for a partular subject
* subject_{test|train}.txt - shows which subject belongs to corresponding row in X_{test|train}.txt
* y_test.txt - show which activity belongs to corresponding row in X_{test|train}.txt
* Inertial Signals directory - shows additional data out of scope for current project

Please see the README.txt at the root directory for more detailed information about initial data.

The run_analysis.R file:

1. creates mapping data frames (for activity and feature enrichment)
2. loads test data and enriches with activity/feature names
3. loads training data and enriches with activity/feature names
4. merges test and training data
5. groups by subject/activity and computes mean of each feature per group

