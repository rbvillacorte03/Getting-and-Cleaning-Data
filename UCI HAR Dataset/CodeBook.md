##CodeBook

# This CodeBook will describes the variables, the data and transformations
# of the work performed in cleaning up the data sets provided on the
# "Getting and Cleaning Data" Course Project.

# The link for the data:
# http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
# https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

# The Data and Variables
# The UCI HAR Dataset contrains the following:
# 1. Test folder with subfolder of Intertial Signals (body_acc_x_test, body_acc_y_test,
#    body_acc_z_test, body_gyro_x_test, body_gyro_y_test, body_gyro_z_text
#    total_acc_x_test, total_acc_y_test, total_acc_z_test), subject_test, X_test and
#    y_test
# 2. Train folder with subfolder of Intertial Signals (body_acc_x_train, body_acc_y_train,
#    body_acc_z_train, body_gyro_x_train, body_gyro_y_train, body_gyro_z_train
#    total_acc_x_train, total_acc_y_train, total_acc_z_train), subject_train, X_train and
#    y_train
# 3. Activity_lables
# 4. features
# 5. features_info
# 6. README

# Working Process:
# 1. Install packages "data.table", "reshape2", always require to load the packages
#    in order to be able to load the data sets.
# 2. Load data column names: activity_lables and features
# 3. Extract the measurements of mean and standard deviation on the loaded data
# 4. Load and process the following: X_test, y_test and subject_test
# 5. Extract the measurements of mean and standard deviation of X_test, y_test
#    set: features, X_test, y_test and subject_test
# 6. Bind data subject_test into y_test and X_test.
# 7. Load and process X_train and y_train data.
# 8. Extract the measurements on the mean and standard deviation of the loaded data
# 9. Load the activity data
# 10.Bind the data subject_test, y_train and X_train
# 11.Merge test and train data
# 12.Apply mean function to dataset using dcast function
# 13.Use write.table function to create a text file with file name tidy_data.