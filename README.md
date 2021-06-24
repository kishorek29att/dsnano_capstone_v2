# Data science Nano Degree - Capstone project
# Starbucks Capstone Challenge

 **Medium Blog Post**: [Here](https://kishorek29.medium.com/starbucks-capstone-challenge-fd84609dd74f)


As part of the final capstone project, i have worked on the starbucks capstone challenge.
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. 
Once every few days, Starbucks sends out an offer to users of the mobile app. 
An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free).

The goal of this project is to combine transaction, demographic, and offer data to determine which demographic groups respond best to which offer type.

<b> Data Source: </b> Data is readily available in the Udacity workspace.

<b> Problem Statement: </b> 
 This project focuses on building a model that predicts whether or not someone will respond to an offer. This will be accomplished using data processing and feature engineering. 
 In addition to this, we will perform exploratory data analysis to answer below questions:
 
  Analysis 1: which age group customers mostly belong to ? <br>
  Analysis 2: What is the most popular offers across age groups ? <br>
  Analysis 3: What is the most popular offers across gender ? <br>
  Analysis 4: which gender is more favorable to promotions ? <br>
  Analysis 5: what is the dominant income range of the customers? <br>
  Analysis 6: Which offer type is completed more than other offer types? <br>

 **Libraries**
 1.  pandas 
 2.  numpy
 3.  math
 4.  json
 5.  matplotlib
 6.  datetime
 7.  MinMaxScaler
 8.  seaborn
 9.  train_test_split
 10. DecisionTreeClassifier
 11. KNeighborsClassifier
 12. RandomForestRegressor
 13. GridSearchCV
  
 **Dataset overview:**
The data is contained in three files: <br>

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.) <br>
profile.json - demographic data for each customer  <br>
transcript.json - records for transactions, offers received, offers viewed, and offers completed  <br>
 <br>
Here is the schema and explanation of each variable in the files:  <br>

portfolio.json  <br>

id (string) - offer id  <br>
offer_type (string) - type of offer ie BOGO, discount, informational  <br>
difficulty (int) - minimum required spend to complete an offer  <br>
reward (int) - reward given for completing an offer  <br>
duration (int) - time for offer to be open, in days  <br>
channels (list of strings)  <br>
 <br>
profile.json  <br>

age (int) - age of the customer <br>
became_member_on (int) - date when customer created an app account <br>
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F) <br>
id (str) - customer id <br>
income (float) - customer's income <br>
 <br>
transcript.json <br>

event (str) - record description (ie transaction, offer received, offer viewed, etc.) <br>
person (str) - customer id <br>
time (int) - time in hours since start of test. The data begins at time t=0 <br>
value - (dict of strings) - either an offer id or transaction amount depending on the record <br>
<br>

 **Observations:**
 By performing exploratory data analysis on the datasets, am able to come up with results as below: <br>
 <br>
 
  Analysis 1: which age group customers mostly belong to? <br>
  Result: Most of the customers belong to adult age group ie., 40-65 years

  Analysis 2: What is the most popular offers across age groups? <br>
  Result:  Most Popular offer is bogo followed by discount across all age groups

  Analysis 3: What is the most popular offers across gender? <br>
  Result: All genders seem to like bogo and discount offers and they have the same reaction toward informational offers

  Analysis 4: which gender is more favorable to promotions? <br>
  Result:  we can see that Female customer offer acceptance rate (74%) is much higher than male customers (58%).
      		 we can infer that female customers respond favorbly to promotions
		 
  Analysis 5: what is the dominant income range of the customers? <br>
  Result: Highest number of customers fall into Low income range (30000 to 60000) followed by Medium income range

  Analysis 6: Which offer type is completed more than other offer types? <br>
  Result: From the chart we can observe that discount offer is the most used offer by customers
  
 **Model**:
  Using customer, transaction and offer data, engineered features and built models.<br>
  Built 3 models - Decision Tree Classifier model, Random Forest Classifier Model and KNeighbors Classifier Model.<br>
  Evaluated models using the Accuracy metric. <br>
  Accuracy metric is selected as it works best for classification models. <br>
  As part of model refienment,performed hyperparameter tuning using Gridsearch technique
  analyzed the prediction accuracy scores from all the models.
  Chose Decision tree as the best performing model based on prediction accuracy<br>
  <br>
 **Future improvements**<br>
  To employ additional Model tuning,more feature engineering to identify features can be implemeted in future to improve the model <br>
  <br>
 **Conclusion**<br>
   As part of the project, am able to accomplish below tasks.<br>
      1. Data processing:  <pre> 
             a. analyzed the datasets <br>
             b. cleaned the data<br>
             c. preprocessed the data<br>
             d. Merging the datasets  </pre> <br>
      2. Data analaysis: performed data analysis on the data to answer the questions <br>
      3. Data modeling: <pre>
             a. Build model to predict customer response to offer<br>
             b. used accuracy as evaluation metric to determine best model<br>
             c. Decision Tree Classifier, Random Forest Classifier and KNeighbors Classifier models have been considered for this project.<br>
	     d. after initial scores,as part of model refinement, we employed GridSearch technique through which we can come to know the best parameters for a model.<br>
	     e. Decisiontree has the best prediction accuracy on validation set data compared to other models.<br> 
	        Hence, We can use Decision tree to predict customer response for the offer. <br>
	     f. Also, Reward and Time are the most important features for the model.   
	     </pre><br>
<br>
  **Results** <br>
   Detailed observations on the Project are documented [here](https://kishorek29.medium.com/starbucks-capstone-challenge-fd84609dd74f)<br>



 **Acknowledgements** <br>
      Thanks Starbucks and Udacity group for sharing the dataset required for analysis.<br>

  
