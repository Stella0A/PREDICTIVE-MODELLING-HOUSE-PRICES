## Predictive Modeling of Housing Prices Using Linear Regression and Random Forest Machine Learning Methods
This project was a coursework assessment 

## Introduction
This report presents the analysis of a housing dataset consisting of features and prices using linear regression and random forest models. It aims to answer two key questions:
1.	What is the importance of each feature in the model?
2.	Predict the house prices in the provided test set and provide the estimated values.

## Data Description
The data provided in a CSV format (@University of Bradford Artificial Intelligence and Data Science course) is loaded into a Python (Jupyter) environment. Basic descriptive analysis is performed on the data with relevant libraries imported. The dataset contains 12 columns and has been split into a training set and a test set. The training set consists of 3000 rows and the test set consists of 1000 rows. The columns in the dataset are as follows: room, bathroom, kitchen, french_door, backyard, furnished, green_paint, solar_power, wood floor, qlm_security, and club_access. The purpose of the training set is to build the regression model, while the test set is used to evaluate the model's performance. Neither dataset has any missing values.

## Modelling
I built two models to predict house prices in the provided dataset: a linear regression model and a random forest regression model. The linear regression model was trained on the training set, and the coefficients of each feature were calculated to determine their importance. Similarly, the random forest regression model was trained on the same dataset and used to predict house prices in the test set. The performance of both models was evaluated and compared to determine which model provides better predictions. 

## Results
After training the models on the training set and using it to predict house prices on the test set, the following results were obtained:


|  Model	 |  MSE on Test Set   |	 MAE on Test Set |
| ------ | --------   | ---------- |
| Random Forest Regression   |  173.90	     | 51678 |
| Linear Regression        	 |  168.99      | 12.99 |

The results show that the linear regression model outperformed the random forest regression model on the provided dataset, with a lower mean squared error (MSE) and mean absolute error (MAE) on the test set. The MSE measures the average squared difference between the predicted and actual house prices, while the MAE measures the average absolute difference between the predicted and actual values. Therefore, the linear regression model is a better fit for predicting house prices on this dataset.

## Feature Importance
The feature importance scores for the linear regression model, based on the magnitude of the coefficients, are presented in Table 1.

Table 1: Feature Importance Scores for the Linear Regression Model
| Feature	| Importance Score |
| ------ | --------   | 
| furnished |	1999  |
| woodfloor	| 1889 |
| solar_power |	1529 |
| room	| 1000 |
| club_access |	730 |
| backyard | 560 |
| kitchen	| 500 |
| qlm_security |	440 |
| green_paint |	370 |
| bathroom	| 299 |
| french_door	| 240 |

The feature importance scores for the random forest model, based on the mean decrease impurity, are presented in Table 2.

Table 2: Feature Importance Scores for the Random Forest Model
|  Feature	Importance    | Score
| ------ | --------   | 
|  room	   |  0.43    | 
| furnished	   | 0.19    | 
| woodfloor    | 	0.17    | 
| solar_power	   | 0.11    | 
| club_access    | 	0.025    | 
| backyard	   | 0.014    | 
| kitchen	   | 0.011    | 
| qlm_security	   | 0.008    | 
| French_door	   | 0.008    | 
| green_paint	   |  0.006    | 
| bathroom	   | 0.004    | 

The results show that the feature importance scores for the linear regression model and random forest model are quite different. In the linear regression model, the top three important features are "furnished", "woodfloor", and "solar_power", while in the random forest model, the most important feature is "room" followed by "furnished" and "woodfloor". However, both models share similarities in their top four important features.

## Conclusion
In conclusion, the results of this study indicate that both linear regression and random forest models can effectively predict house prices based on the provided features. However, the feature importance scores for each model differ significantly. The linear regression model places higher importance on features such as "furnished", "woodfloor", and "solar_power", while the random forest model prioritizes "room" followed by "furnished" and "woodfloor". This suggests that the two models may be relying on different sets of features to make predictions, which can be useful information for real estate agents and potential home buyers to understand the factors driving house prices.
Despite these differences, both models share similarities in their top four important features. The linear regression model achieved a low MSE score of 168.99 and an MAE score of 12.99, indicating that it can make reasonably accurate predictions. Overall, the findings of this study can be useful in helping stakeholders better understand the factors driving house prices and make informed decisions based on this information.




