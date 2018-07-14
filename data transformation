#using the blog_train.csv file to make the logistic model
train_csv<-read.csv('D:/Study Material/MGS 662 ML/Blog data/blogData_train.csv', header = FALSE)
train<-as.data.frame(train_csv)

#using the blog_train_logistic file in which the target variable is 282 in which the values are either 1(if v281>6.7(mean) or 0)
train_csv_log<-read.csv('D:/Study Material/MGS 662 ML/Blog data/blogData_train_logistic.csv', header=FALSE)
train_log<-as.data.frame(train_csv_log)


#creating data using relevant columns to be used in creating the models
basic_features<-train[,c(50,51,52,53,54,55,56,57,58,59,60,281)]

basic_features_log<-train_log[,c(50,51,52,53,54,55,56,57,58,59,60,282)]

#textual features
textual_features<-train[,c(63:262, 281)]

textual_features_log<-train_log[,c(63:262,282)]

#transform the data to make it more relevant
#transform for linear model
basic_features<-na.omit(log(basic_features+1))
summary(basic_features$V281)
textual_features<-na.omit(log(textual_features+1))
summary(textual_features)

#transform for logistic model
basic_features_log<-na.omit(log(basic_features_log+1))

textual_features_log<-na.omit(log(textual_features_log+1))

