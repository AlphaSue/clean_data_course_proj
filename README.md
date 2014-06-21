My Course Project
======================

This is my course project for Coursera course [Getting and Cleaning Data](https://www.coursera.org/course/getdata) taught by [Professor Jeffrey Leek](http://www.biostat.jhsph.edu/~jleek/research.html).

This repository includes three items:
----------------------

* An well-commented R script called `run_analysis.R` that does the analysis and creates the tidy data set. 

>Details of the `run_analysis.R` script are provided below this accounting of the repository. 


* CodeBook.md 

>A markdown file that a code book that describes the variables, the data, and the transformations and work that I performed to clean up the data.

* README.md

>This file. It explains how the scripts work, contents of the repository, and how the contents are connected. 



###Details on the `run_analysis.R` script

The `run_analysis.R` script is a well-commented R script that does the analysis and creates the tidy data set by doing the following:

>1.  Merges the training and the test sets to create one data set. 
>2.  Extracts only the measurements on the mean and standard deviation for each measurement.
>3.  Uses descriptive activity names to name the activities in the data set
>4.  Appropriately labels the data set with descriptive variable names.
>5.  Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The `run_analysis.R` script assumes the contents of the provided zip file have all been placed in the working directory at the outset. The specific files and directories from the instructor-provided zip file placed in the working directory:  
a) README.txt;  
b) activity_labels.txt;  
c) features_info.txt;  
d) features.txt;  
e) train directory; and  
f) test directory.

####Step #1 information

As described in [this post](https://class.coursera.org/getdata-004/forum/thread?thread_id=106) the data in the inertial directory is very raw data and will ultimately be discarded for the tidy data set in later steps, and so it has been left out of the merge from the start.

In the raw data the test and the training data sets are actually divided among three files for each set. As preparation for the merge, steps combining the parts of the test and training data each into its own data frame precedes thse merging the training and test sets. During the combining the columns for subject ids and activity are added and converted from the interger values created during reading of the table to factor variables since the number differences don't correspond to quantitative differences.

At the conclusion of the merge, the data set was checked for missing values as one should be congniznnt of these when cleaning data and handle appropriately during downstream processes of creating a tidy data set or subsequent analysis. Luckily this is amde easy by the fact there are no missing values.

######The script includes many comments and I would suggest consulting it [here](https://github.com/fomightez/clean_data_course_proj/blob/master/run_analysis.R) if you still seek additional insight about the processing of the raw data to a tidy data set.

Additional information and attribution
---------------------------------------

The raw data utilized here represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description and attribution is available at the site where the data was originally obtained:

[http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

The specific zipped file containing the raw data set for this project was provided by the class instructors.



