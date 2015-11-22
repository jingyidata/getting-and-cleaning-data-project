                                 DATA DICTIONARY -- Human Activity Recognition Using Smartphones Data Set
                                
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The tidy_run_data includes average of each variable for each activity and each subject.

Column 1. subject:
  This is the identification number of 30 volunteers performed the activity. Its range is from 1 to 30
  This column merges the training and test data sets (subject_train.txt and subject_test.txt).
  
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
