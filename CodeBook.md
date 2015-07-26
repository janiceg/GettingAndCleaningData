##CodeBook for Getting and Cleaning Data Project

###Data Source:
Site from where the Data was fetched
 http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones  

###Data for the Project
 https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  

###Saved in the Working Directory as folder named:
 UCI-HAR-Dataset

###About the Data set:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

- 'features_info.txt': Shows information about the variables used on the feature vector.
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.

###Script and variable list:
  - run_analysis.R 

Step1. Merges the training and the test sets to create one data set

- trainData : Holds Data fetched by - read.table('./train/X_train.txt')
- trainLabel : Holds Data fetched by - read.table('./train/y_train.txt')
- trainSubject: Holds Data fetched by - read.tabl('./train/subject_train.txt')
- testData : Holds Data fetched by - read.table('./test/X_test.txt')
- testLabel : Holds Data fetched by - read.table('./test/y_test.txt')
- testSubject : Holds Data fetched by - read.table('./test/subject_test.txt')
- features : Holds Data fetched by - read.table('./features.txt')
- activity : Holds Data fetched by - read.table('activity_labels.txt')

Merging the data and train and subject tables using rbind() function.
        
Step 2. Extracts only the measurements on the mean and standard deviation for each measurement.
 
Step 3. Uses descriptive activity names to name the activities in the data set. 

Step 4. Appropriately labels the data set with descriptive activity names.
        The dataset data.merge is created.
	 
Step 5. creates a second, independent tidy data set with the average of each variable for each activity and each subject.
	The file tidydata.txt is created.

###Output:
 
Files are available in the working directory
        
        tidydata.txt


###Output summary:

 - Description of the variables in the tidydata.txt file
 - Column 1 : ActivityName		
                
                - 1: WALKING                    : Subject was walking during the test
                
                - 2: WALKING_UPSTAIRS		: Subject was walking up a staircase during the test
                
                - 3: WALKING_DOWNSTAIRS	        : Subject was walking down a staircase during the test
                
                - 4: SITTING			: Subject was sitting during the test
                
                - 5. STANDING			: Subject was standing during the test
                
                - 6. LAYING			: Subject was laying down during the test
                
      
 - Column 2 : 	 Subject			: The ID of the test subject (volunteer)
 - Column 3 :	 ActivityClass			: The type of activity performed when the corresponding measurements were taken
 - Column 4 - 69 :	 Measurements	: 
                
        
                tBodyAcc-mean()-X       
                : Mean value of X coordinate of body acceleration captured by accelerometer in the time domain
                tBodyAcc-mean()-Y	
                : Mean value of Y coordinate of body acceleration captured by accelerometer in the time domain
                tBodyAcc-mean()-Z	
                : Mean value of Z coordinate of body acceleration captured by accelerometer in the time domain
                tBodyAcc-std()-X
                : Standard deviation of X coordinate of body acceleration captured by accelerometer in the time domain
                tBodyAcc-std()-Y
                : Standard deviation of Y coordinate of body acceleration captured by accelerometer in the time domain
                tBodyAcc-std()-Z	
                : Standard deviation of Z coordinate of body acceleration captured by accelerometer in the time domain
                tGravityAcc-mean()-X	
                : Mean value of X coordinate of gravity acceleration captured by accelerometer in the time domain
                tGravityAcc-mean()-Y	
                : Mean value of Y coordinate of gravity acceleration captured by accelerometer in the time domain
                tGravityAcc-mean()-Z	
                : Mean value of Z coordinate of gravity acceleration captured by accelerometer in the time domain
                tGravityAcc-std()-X	
                : Standard deviation of X coordinate of gravity acceleration captured by accelerometer in the time domain
                tGravityAcc-std()-Y	
                : Standard deviation of Y coordinate of gravity acceleration captured by accelerometer in the time domain
                tGravityAcc-std()-Z	
                : Standard deviation of Z coordinate of gravity acceleration captured by accelerometer in the time domain
                tBodyAccJerk-mean()-X	
                : Mean value of X coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerk-mean()-Y	
                : Mean value of Y coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerk-mean()-Z	
                : Mean value of Z coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerk-std()-X	
                : Standard deviation of X coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerk-std()-Y	
                : Standard deviation of Y coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerk-std()-Z	
                : Standard deviation of Z coordinate of body acceleration jerk captured by accelerometer in the time domain
                tBodyGyro-mean()-X	
                : Mean value of X coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyro-mean()-Y	
                : Mean value of Y coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyro-mean()-Z		
                : Mean value of Z coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyro-std()-X		
                : Standard deviation of X coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyro-std()-Y		
                : Standard deviation of Y coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyro-std()-Z		
                : Standard deviation of Z coordinate of body acceleration captured by gyroscope in the time domain
                tBodyGyroJerk-mean()-X		
                : Mean value of X coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerk-mean()-Y		
                : Mean value of Y coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerk-mean()-Z		
                : Mean value of Z coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerk-std()-X		
                : Standard deviation of X coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerk-std()-Y		
                : Standard deviation of Y coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerk-std()-Z		
                : Standard deviation of Z coordinate of body acceleration jerk captured by gyroscope in the time domain
                tBodyAccMag-mean()		
                : Mean value of magnitude of body acceleration captured by accelerator in the time domain
                tBodyAccMag-std()		
                : Standard deviation of magnitude of body acceleration captured by accelerator in the time domain
                tGravityAccMag-mean()		
                : Mean value of magnitude of gravity acceleration captured by accelerator in the time domain
                tGravityAccMag-std()		
                : Standard deviation of magnitude of gravity acceleration captured by accelerator in the time domain
                tBodyAccJerkMag-mean()		
                : Mean value of magnitude of body acceleration jerk captured by accelerometer in the time domain
                tBodyAccJerkMag-std()		
                : Standard deviation of magnitude of body acceleration jerk captured by accelerometer in the time domain
                tBodyGyroMag-mean()		
                : Mean value of magnitude of body acceleration captured by gyroscope in the time domain
                tBodyGyroMag-std()		
                : Standard deviation of magnitude of body acceleration captured by gyroscope in the time domain
                tBodyGyroJerkMag-mean()	
                : Mean value of magnitude of body acceleration jerk captured by gyroscope in the time domain
                tBodyGyroJerkMag-std()		
                : Standard deviation of magnitude of body acceleration jerk captured by gyroscope in the time domain
                fBodyAcc-mean()-X		
                : Mean value of X coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAcc-mean()-Y		
                : Mean value of Y coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAcc-mean()-Z		
                : Mean value of Z coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAcc-std()-X		
                : Standard deviation value of X coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAcc-std()-Y		
                : Standard deviation value of Y coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAcc-std()-Z		
                : Standard deviation value of Z coordinate of body acceleration captured by accelerometer in the frequency domain
                fBodyAccJerk-mean()-X		
                : Mean value of X coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyAccJerk-mean()-Y		
                : Mean value of Y coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyAccJerk-mean()-Z		
                : Mean value of Z coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyAccJerk-std()-X		
                : Standard deviation of X coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyAccJerk-std()-Y		        
                : Standard deviation of Y coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyAccJerk-std()-Z		
                : Standard deviation of Z coordinate of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyGyro-mean()-X		
                : Mean value of X coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyGyro-mean()-Y		
                : Mean value of Y coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyGyro-mean()-Z		
                : Mean value of Z coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyGyro-std()-X		
                : Standard deviation of X coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyGyro-std()-Y		
                : Standard deviation of Y coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyGyro-std()-Z		
                : Standard deviation of Z coordinate of body acceleration captured by gyroscope in the frequency domain
                fBodyAccMag-mean()		
                : Mean value of magnitude of body acceleration captured by accelerator in the frequency domain
                fBodyAccMag-std()		
                : Standard deviation of magnitude of body acceleration captured by accelerator in the frequency domain
                fBodyBodyAccJerkMag-mean()	
                : Mean value of magnitude of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyBodyAccJerkMag-std()	
                : Standard deviation of magnitude of body acceleration jerk captured by accelerometer in the frequency domain
                fBodyBodyGyroMag-mean()	
                : Mean value of magnitude of body acceleration captured by gyroscope in the frequency domain
                fBodyBodyGyroMag-std()		
                : Standard deviation of magnitude of body acceleration captured by gyroscope in the frequency domain
                fBodyBodyGyroJerkMag-mean()	
                : Mean value of magnitude of body acceleration jerk captured by gyroscope in the frequency domain
                fBodyBodyGyroJerkMag-std()	
                : Standard deviation of magnitude of body acceleration jerk captured by gyroscope in the frequency domain