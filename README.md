# Term-Deposit-Subscription-Clasification
There are several factors and parameters to consider in the banking sector when it comes to customers and their term deposits. The main intention of this project is to use the data from the marketing campaigns from a Portugues firm whether a customer would subscribe to a term deposit or not. Features such as age, marital status, default status, job type etc are evaluated for prediction. Efficient and accurate prediction of term deposits will help in personalised marketing strategies and business models.

Steps Involved:
* Data Observation and Preparation
* EDA: Data visualisation and understanding
* Model Building Logistic Regression, SVM, Decision Tree, Random Forest, Bagging & Boosting.
* Model Evaluation
* Cross Validation
* Hyperparameter Tuning

Data Used: The model is trained using the UCI Bank Marketing Dataset. The raw dataset consisted of 20 features such as age, job, martial, education etc. to predict the variable y state, a binary variable indicating whether the client subscribed to the term deposit(yes,no). The total number of samples available in the dataset is 41,188 with all features mostly being integers or objects with no null values.


Classification methods:
* Baseline - Logistic/Softmax Regression
* Support Vector Machines
   * Linear SVM
   * RBF SVM
   * Polynomial SVM
* Decision Trees
* Random Forest
* Adaboost
* Gradient Boost

Hyperparameter Tuning was carried out by GridSearch CV and Randomized Search CV

## Discussion and Results
We can observe from the results that Gradient Boost Classifier has performed the best with an accuracy of 0.907 closely followed by the hyperparameter tuned Random Forest Classifier and Decision Tree Classifier. This shows that ensemble learning works with precision for our model. This  is due to weights which are continuously being rearranged to each instance, with higher weights assigned to incorrectly classified instances. It reduces the bias thus boosting the model for best performance. 
Accuracy of ensemble models was the same both pre-scaled and post-scaled, hence cross validation on f1 score was calculated for prescaled and post-scaled for svm models while the training set and entire set for the ensemble models. The cross validation scores on f1 scores have been very low for ensemble models ranging even lower than 0.1 incase of random forest. This indicates that accuracy of these models are high but the precision recall of such models are low.
The pre-scaled model for polynomial SVM was  unable to be processed due to unknown reasons.
We were able to successfully perform hyperparameter tuning including grid search and random search only for two models which are Random Forest and Decision Trees.  The processing time for the hyperparameter tuning of  other models were not handled appropriately by our systems not yielding any results. Other models yielded inconsistent results hence are not mentioned in the report. This is one of the major limitations of our analysis.
Hyperparameter tuning yielded optimal results with Random Forest and Decision Trees. We believe that if hypertuning was indeed able to be carried out in other models, there is a high possibility that their scores will also be enhanced in finding the optimum hyper parameters.

Out of the Analysis carried out, we conclude that Gradient Boost Classifier proved to be the most accurate in classifying the term deposit value based on the parameters provided closely followed by Random Forest Regressor. With high accuracy, we can deploy this model to predict the term deposits of customers helping in personalised marketing strategies and business models for the bank

