# getting-and-cleaning-data-project
Step1: 
put the raw data sets in the same folder. list of files:
--subject_train.txt,
--subject-test.txt,
--total_acc_x_train.txt,
--total_acc_x_test.txt,
--total_acc_y_train.txt,
--total_acc_y_test.txt,
--total_acc_z_train.txt,
--total_acc_z_test.txt,
--body_acc_x_train.txt,
--body_acc_x_test.txt,
--body_acc_y_train.txt,
--body_acc_y_test.txt,
--body_acc_z_train.txt,
--body_acc_z_test.txt,
--body_gyro_x_train.txt,
--body_gyro_x_test.txt,
--body_gyro_y_train.txt,
--body_gyro_y_test.txt,
--body_gyro_z_train.txt,
--body_gyro_z_test.txt,
--X_train.txt,
--X_test.txt,
--y_train.txt,
--y_test.txt,

Step2: install R packge matrixStats. 

Step3: run the following R script in Rstudio version 0.99.484.

R script: 

# read raw data into R
X_test<-read.table("./data/X_test.txt")
X_train<-read.table("./data/X_train.txt")
y_test<-read.table("./data/y_test.txt")
y_train<-read.table("./data/y_train.txt")
body_acc_x_test<-read.table("./data/body_acc_x_test.txt")
body_acc_x_train<-read.table("./data/body_acc_x_train.txt")
body_acc_y_test<-read.table("./data/body_acc_y_test.txt")
body_acc_y_train<-read.table("./data/body_acc_y_train.txt")
body_acc_z_test<-read.table("./data/body_acc_z_test.txt")
body_acc_z_train<-read.table("./data/body_acc_z_train.txt")
body_gyro_x_test<-read.table("./data/body_gyro_x_test.txt")
body_gyro_x_train<-read.table("./data/body_gyro_x_train.txt")
body_gyro_y_test<-read.table("./data/body_gyro_y_test.txt")
body_gyro_y_train<-read.table("./data/body_gyro_y_train.txt")
body_gyro_z_test<-read.table("./data/body_gyro_z_test.txt")
body_gyro_z_train<-read.table("./data/body_gyro_z_train.txt")
total_acc_x_test<-read.table("./data/total_acc_x_test.txt")
total_acc_x_train<-read.table("./data/total_acc_x_train.txt")
total_acc_y_test<-read.table("./data/total_acc_y_test.txt")
total_acc_y_train<-read.table("./data/total_acc_y_train.txt")
total_acc_z_test<-read.table("./data/total_acc_z_test.txt")
total_acc_z_train<-read.table("./data/total_acc_z_train.txt")
subject_test<-read.table("./data/subject_test.txt")
subject_train<-read.table("./data/subject_train.txt")

# merge training and test data sets
X=rbind(X_train,X_test)
y=rbind(y_train,y_test)
body_acc_x<-rbind(body_acc_x_train,body_acc_x_test)
body_acc_y<-rbind(body_acc_y_train,body_acc_y_test)
body_acc_z<-rbind(body_acc_z_train,body_acc_z_test)
body_gyro_x<-rbind(body_gyro_x_train,body_gyro_x_test)
body_gyro_y<-rbind(body_gyro_y_train,body_gyro_y_test)
body_gyro_z<-rbind(body_gyro_z_train,body_gyro_z_test)
total_acc_x<-rbind(total_acc_x_train,total_acc_x_test)
total_acc_y<-rbind(total_acc_y_train,total_acc_y_test)
total_acc_z<-rbind(total_acc_z_train,total_acc_z_test)
subject<-rbind(subject_train,subject_test)

#extract the mean and starndard deviation of each measurement
library(matrixStats)
body_acc_x_mean_sd<-data.frame(matrix(nrow=nrow(body_acc_x),ncol=2))
body_acc_x_mean_sd[,1]<-rowMeans(body_acc_x)
body_acc_x_mean_sd[,2]<-rowSds(as.matrix(body_acc_x))
names(body_acc_x_mean_sd)<-c("body_acc_x_mean","body_acc_x_sd")

body_acc_y_mean_sd<-data.frame(matrix(nrow=nrow(body_acc_y),ncol=2))
body_acc_y_mean_sd[,1]<-rowMeans(body_acc_y)
body_acc_y_mean_sd[,2]<-rowSds(as.matrix(body_acc_y))
names(body_acc_y_mean_sd)<-c("body_acc_y_mean","body_acc_y_sd")

body_acc_z_mean_sd<-data.frame(matrix(nrow=nrow(body_acc_z),ncol=2))
body_acc_z_mean_sd[,1]<-rowMeans(body_acc_z)
body_acc_z_mean_sd[,2]<-rowSds(as.matrix(body_acc_z))
names(body_acc_z_mean_sd)<-c("body_acc_z_mean","body_acc_z_sd")

body_gyro_x_mean_sd<-data.frame(matrix(nrow=nrow(body_gyro_x),ncol=2))
body_gyro_x_mean_sd[,1]<-rowMeans(body_gyro_x)
body_gyro_x_mean_sd[,2]<-rowSds(as.matrix(body_gyro_x))
names(body_gyro_x_mean_sd)<-c("body_gyro_x_mean","body_gyro_x_sd")

body_gyro_y_mean_sd<-data.frame(matrix(nrow=nrow(body_gyro_y),ncol=2))
body_gyro_y_mean_sd[,1]<-rowMeans(body_gyro_y)
body_gyro_y_mean_sd[,2]<-rowSds(as.matrix(body_gyro_y))
names(body_gyro_y_mean_sd)<-c("body_gyro_y_mean","body_gyro_y_sd")

body_gyro_z_mean_sd<-data.frame(matrix(nrow=nrow(body_gyro_z),ncol=2))
body_gyro_z_mean_sd[,1]<-rowMeans(body_gyro_z)
body_gyro_z_mean_sd[,2]<-rowSds(as.matrix(body_gyro_z))
names(body_gyro_z_mean_sd)<-c("body_gyro_z_mean","body_gyro_z_sd")

total_acc_x_mean_sd<-data.frame(matrix(nrow=nrow(total_acc_x),ncol=2))
total_acc_x_mean_sd[,1]<-rowMeans(total_acc_x)
total_acc_x_mean_sd[,2]<-rowSds(as.matrix(total_acc_x))
names(total_acc_x_mean_sd)<-c("total_acc_x_mean","total_acc_x_sd")

total_acc_y_mean_sd<-data.frame(matrix(nrow=nrow(total_acc_y),ncol=2))
total_acc_y_mean_sd[,1]<-rowMeans(total_acc_y)
total_acc_y_mean_sd[,2]<-rowSds(as.matrix(total_acc_y))
names(total_acc_y_mean_sd)<-c("total_acc_y_mean","total_acc_y_sd")

total_acc_z_mean_sd<-data.frame(matrix(nrow=nrow(total_acc_z),ncol=2))
total_acc_z_mean_sd[,1]<-rowMeans(total_acc_z)
total_acc_z_mean_sd[,2]<-rowSds(as.matrix(total_acc_z))
names(total_acc_z_mean_sd)<-c("total_acc_z_mean","total_acc_z_sd")

names(subject)<-c("subject")
        
# create a tidy data set with the average of each variable for each activit and each subject
tidy_run_data<-data.frame(matrix(nrow=nrow(total_acc_x),ncol=10))
names(tidy_run_data)<-c("subject","total_acc_x","total_acc_y","total_acc_z","body_acc_x","body_acc_y","body_acc_z","body_gyro_x","body_gyro_y","body_gyro_z")
tidy_run_data$subject<-subject$subject
tidy_run_data$total_acc_x<-total_acc_x_mean_sd$total_acc_x_mean
tidy_run_data$total_acc_y<-total_acc_y_mean_sd$total_acc_y_mean
tidy_run_data$total_acc_z<-total_acc_z_mean_sd$total_acc_z_mean
tidy_run_data$body_acc_x<-body_acc_x_mean_sd$body_acc_x_mean
tidy_run_data$body_acc_y<-body_acc_y_mean_sd$body_acc_y_mean
tidy_run_data$body_acc_z<-body_acc_z_mean_sd$body_acc_z_mean
tidy_run_data$body_gyro_x<-body_gyro_x_mean_sd$body_gyro_x_mean
tidy_run_data$body_gyro_y<-body_gyro_y_mean_sd$body_gyro_y_mean
tidy_run_data$body_gyro_z<-body_gyro_z_mean_sd$body_gyro_z_mean

# write the tidy data set to a txt file
write.table(tidy_run_data,file = "./data/tidy_run_data.txt", row.names = F, col.names = T,sep = "\t",quote = F)
