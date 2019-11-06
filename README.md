# Building predictive models to predict customer churn rate of a telecom company


![Alt textimg](screenshots/images.png)<img src="screenshots/images.png" width=800/> #![](screenshots/images.png)


# Why this project?
Customer churn is one of the most important factors for a growing business.While every telecom company wants to make the business as profitable as possible, the growth rate also dependds on the no.of customers using their services.As the number of customers decreases, the company also faces a loss.So churn rate(Possibility of a customer leaving a company or moving to another company) needs to be predicted to retain customers.

# Market Research
As per most of the business studies, customer retention is more difficult and requires more attention in telecom industry than gaining new customers.Customer churn does not happen overnight.Churn happens when the customer is not satisfied with the services.So it is responsibility of the company to not only listen to the feedback of the customers but also implement necessary actions to meet the customers's needs.With predictive modelling, the company can anticipate the churn and devise relevant marketing strategies to improve customer retention.


# Dataset
The telecom churn dataset contains 7043 records of customers of telecom company.It also contains 21 features or dimensions to describe the customers subscribed services and activities.

Following are the features used in the dataset:

customerID        
gender            
SeniorCitizen     
Partner           
Dependents      
tenure          
PhoneService    
MultipleLines   
InternetService 
OnlineSecurity  
OnlineBackup    
DeviceProtection
TechSupport     
StreamingTV     
StreamingMovies 
Contract        
PaperlessBilling
PaymentMethod   
MonthlyCharges  
TotalCharges       
Churn            

# Preprocessing
AAlmost all the features are categorical and contain labels.Since most of these columns contain only 2 unique values(yes,no :0,1), encoding these categorical values can be done using dummification or one hot encoding or label encoding.Since label encoding will be more convenient here in terms of handling data as each column contains only 2 labels, label encoding is used here to convert these labels into numbers.Tenure,Monthly charges and Total Charges are numerical features which are not encoded.Standard scaling is applied to these data to use all the features on the same scale of units.There was no need to handle missing values as the data was very clean without any null or improbable values.

# Modelling
 For this particular problem , both supervised and unsupervised techniques are applied to compare the accuracy of the models.The to metric used here to compare the models is accuracy to verify the correct predictions of the model.For unsupervised, clustering techniques like k-mean and agglomerative clustering was used to cluster the data into 2 groups corresponding to the churn.Then all the classification models such as KNN,Naive Bayes,Decision Tree and Random Forest algorithms were used to build the model for prediction.

# Inference
From all the modelling techniques used, we can see that Random Forest and SVM gave the best results for unsupervised(98%) and supervised models(79%).Further boosting these supervised models might lead to better accuracy.
