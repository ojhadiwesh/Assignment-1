# linear regression model on train
#remove v55 and v60 from the model to remove rank defiency because they have many missing values
fit<-lm(V281~(V50+V51+V52+V53+V54+V56+V57+V58+V59+V60), data = basic_features)
sum(residuals(fit)^2)
#logistic regression on train
#remove v55 and v60 from the model to remove rank defiency because they have many missing values
fit_log<-glm(V282~(V50+V51+V52+V53+V54+V56+V57+V58+V59+V60), data = basic_features_log)
pred<-predict(fit,test_csv1)
#testing the linear model on  test data
for(i in 1:60){
  pred<-predict(fit,test_data_list[i])
  test_data<-test_data_list[i]
  test_data
  rss_list<-sum((pred-test_data$v281)^2)
  test_data<-NULL
}
#testing logistic model
sum((pred-test_csv1$V281)^2)
pred_log<-predict(fit_log,test_csv1)

