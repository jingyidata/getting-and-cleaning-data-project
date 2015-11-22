                                 CodeBook -- Human Activity Recognition Using Smartphones Data Set

Study Design:                                
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. 
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) 
wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 
we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. 
The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, 
where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and 
then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). 
The sensor acceleration signal, which has gravitational and body motion components, was separated using a 
Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have 
only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, 
a vector of features was obtained by calculating variables from the time and frequency domain. 
See 'features_info.txt' for more details. 

For each record it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.



Codebook:

The tidy_run_data includes average of each variable for each activity and each subject.

Column 1. subject:
  This is the identifier of 30 volunteers who carried out the experiment. Its range is from 1 to 30.
  This column is merged data of training and test data sets (subject_train.txt and subject_test.txt).
  
Column 2. total_acc_x:
  The acceleration signal from the smartphone accelerometer x axis in standard gravity units 'g'. 
  This column is the average of measurements in x axial.
  First the tranining and test data sets (total_acc_x_train.txt and total_acc_x_test.txt) were merged into one data set. Then the average of each row was calculated. 
  
Column 3. total_acc_y:
  The acceleration signal from the smartphone accelerometer y axis in standard gravity units 'g'. 
  This column is the average of measurements in y axial.
  First the tranining and test data sets (total_acc_y_train.txt and total_acc_y_test.txt) were merged into one data set. Then the average of each row was calculated.  
  
Column 4. total_acc_z:
  The acceleration signal from the smartphone accelerometer z axis in standard gravity units 'g'. 
  This column is the average of measurements in z axial.
  First the tranining and test data sets (total_acc_z_train.txt and total_acc_z_test.txt) were merged into one data set. Then the average of each row was calculated. 
  
Column 5. body_acc_x:
  The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
  This column is the avarge of measurements in x axial.
  First the tranining and test data sets (body_acc_x_train.txt and body_acc_x_test.txt) were merged into one data set. Then the average of each row was calculated. 
  
Column 6. body_acc_y:
  The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
  This column is the avarge of measurements in y axial.
  First the tranining and test data sets (body_acc_y_train.txt and body_acc_y_test.txt) were merged into one data set. Then the average of each row was calculated. 

Column 7. body_acc_z:
  The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
  This column is the avarge of measurements in z axial.
  First the tranining and test data sets (body_acc_z_train.txt and body_acc_z_test.txt) were merged into one data set. Then the average of each row was calculated.
  
Column 8. body_gyro_x:
  The angular velocity vector measured by the gyroscope. The units are radians/second.
  This column is the avarge of measurements in x axial.
  First the tranining and test data sets (body_gyro_x_train.txt and body_gyro_x_test.txt) were merged into one data set. Then the average of each row was calculated.
  
Column 9. body_gyro_y:
  The angular velocity vector measured by the gyroscope. The units are radians/second.
  This column is the avarge of measurements in y axial.
  First the tranining and test data sets (body_gyro_y_train.txt and body_gyro_y_test.txt) were merged into one data set. Then the average of each row was calculated.

Column 10. body_gyro_z:
  The angular velocity vector measured by the gyroscope. The units are radians/second.
  This column is the avarge of measurements in z axial.
  First the tranining and test data sets (body_gyro_z_train.txt and body_gyro_z_test.txt) were merged into one data set. Then the average of each row was calculated.
