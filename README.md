## Predictive Modeling of Housing Prices Using Linear Regression and Random Forest Machine Learning Methods
This project was a coursework assessment 

## Introduction
This report presents an analysis of housing prices using two machine learning methods: Linear Regression and Random Forest. The primary goals are:
1. To determine the importance of each feature in predicting house prices.
2. To predict house prices in the test dataset and evaluate the accuracy of these predictions.

## Data Description
The housing dataset used in this study was provided as part of the University of Bradford's Artificial Intelligence and Data Science course. The dataset consists of 12 columns, each representing various attributes related to housing, such as room count, kitchen, backyard, etc. It is split into a training set of 3000 rows and a test set of 1000 rows.
The columns are as follows:
room, bathroom, kitchen, french_door, backyard, furnished, green_paint, solar_power, wood_floor, qlm_security, and club_access.
Both datasets have no missing values and are used to build and evaluate the models.

## Modelling
Two models were built to predict house prices:
Linear Regression: This model assumes a linear relationship between features and house prices. It calculates coefficients for each feature, which helps determine their importance.
Random Forest Regression: This non-linear method uses an ensemble of decision trees to make predictions. It ranks feature importance based on their contribution to reducing impurity in the trees.
Both models were trained on the training set and then used to predict prices on the test set. Their performance was measured using Mean Squared Error (MSE) and Mean Absolute Error (MAE).

## Results
After training and testing the models, the following results were obtained:

|  Model	 |  MSE on Test Set   |	 MAE on Test Set |
| ------ | --------   | ---------- |
| Random Forest Regression   |  173.90	     | 51678 |
| Linear Regression        	 |  168.99      | 12.99 |

The Linear Regression model outperformed the Random Forest model, achieving lower MSE and MAE values. MSE measures the average squared difference between predicted and actual values, while MAE captures the average absolute difference.

## Feature Importance
Feature importance was calculated differently for each model:
Linear Regression: Importance is based on the magnitude of the coefficients.
Random Forest: Importance is based on the mean decrease in impurity.

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

## Discussion
The two models exhibited different patterns of feature importance:
Linear Regression: Prioritized features like furnished, woodfloor, and solar_power.
Random Forest: Placed the most importance on room, followed by furnished and woodfloor.
Both models agreed on the importance of furnished and woodfloor but differed significantly in the importance assigned to other features. For example, room was much more critical for Random Forest, while solar_power had higher importance in Linear Regression.

## Conclusion
Both models effectively predicted house prices, with Linear Regression outperforming Random Forest on this dataset. The feature importance analysis revealed that furnished, woodfloor, and solar_power were crucial predictors in the Linear Regression model, while room and furnished were most important in the Random Forest model. These insights can be valuable for real estate stakeholders looking to understand which features most influence house prices.

The linear regression model, with its lower MSE and MAE, provides a more reliable prediction for this dataset. The findings suggest that different models may prioritize features differently, highlighting the importance of model selection based on the dataset's characteristics.







