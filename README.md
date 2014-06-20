My Course Project
======================

This is my course project for Coursera course [Getting and Cleaning Data](https://www.coursera.org/course/getdata) taught by [Professor Jeffrey Leek](http://www.biostat.jhsph.edu/~jleek/research.html).

This repository includes three items:
----------------------

* An well-commented R script called run_analysis.R that does the analysis and creates the tidy data set by doing the following:

>1.  Merges the training and the test sets to create one data set. 
>2.  Extracts only the measurements on the mean and standard deviation for each measurement.
>3.  Uses descriptive activity names to name the activities in the data set
>4.  Appropriately labels the data set with descriptive variable names.
>5.  Creates a second, independent tidy data set with the average of each variable for each activity and each subject.


* CodeBook.md 

>A markdown file that a code book that describes the variables, the data, and the transformations and work that I performed to clean up the data.

* README.md

>This file. It explains how the scripts work, contents of the repository, and how the contents are connected. 


###Details on the `run_analysis.R` script

The `run_analysis.R` script assumes the contents of the provided zip file have all been placed in the working directory at the outset. The specific files and directories from the provided zip file placed in the working directory:  
a) README.txt;  
b) activity_labels.txt;  
c) features_info.txt;  
d) features.txt;  
e) train directory; and  
f) test directory.


As described in [this post](https://class.coursera.org/getdata-004/forum/thread?thread_id=106) the data in the inertial directory is very raw data and will ultimately be discarded for the tidy data set in later steps and so it has been left out of the merge from the start.

In the raw data the test and the training data sets. are actually divided among three files for each set. As preparation for the merge, steps combining the parts of the test and training data each into its own data frame precedes thse merging the training and test sets.


Additional information
----------------------

The data utilized here represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

[http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

The specific data for this project was provided by the instructors.



