# Quality Predictions in a Mining Process
### Disclaimer
This project was conduct for University of Toronto - School of Continuing Studies (SCS) as part of the Machine Learning 3253 Course. The dataset used for this project was retrieved from https://www.kaggle.com/edumagalhaes/quality-prediction-in-a-mining-process

Submitted By:
 - Adam Gregg
 - Nisarg Patel
 - Omar Hamdy
 - Khurram Shafiq

### Introduction
The main goal is to use this data to predict how much impurity is present in the ore concentrate. The impurity is present in the form of Silica. Hence, the primary goal is to predict % Silica present in the Iron Ore concentrate. The impurity is measured every hour, if we can predict how much silica (impurity) is in the ore concentrate, it can help the engineers, giving them early information to take actions and make process improvements. Hence, they will be able to take corrective actions in advance (reduce impurity, if it is the case) and also help the environment (reducing the amount of ore that goes to tailings as you reduce silica in the ore concentrate).

### Dataset
The data is collected from machine sensors every 20 seconds and we have data from a 6 month range (march of 2017 until september of 2017). The dataset contains 737,453 instances and 24 attributes with the target varibale being % Silica Concentrate. Our team decided to take 2 different approaches to see which approach will perform better. Due to the large dataset, we decided to create a resampled dataset that aggregated the sensor values to every 1 hour from 20 seconds, which became our second approach.

### Machine Learning Model
We started off by splitting the data into training and testing sets. We then built a pipeline that consisted of a transformer and an estimator. Next, we used cross validation on the training data in order to determine which regression algorithm performs the best on out of sample data. The best respective model for each approach was then chosen to build the regression model. We then evaluated the models with the testing data in order to get a baseline model. Next, hyperparameter tuning was performed using GridsearchCV and lastly the models were finalized and validated with the best estimator previously discovered during the tuning phase. 

### Conclusion
After using various algorithm’s, we documented their performance using the RMSE score, R^2, and accuracy. We found out that the Random Forest Regressor performed better on the larger dataset that was sampled every 20 seconds and the Gradient Boosting Regressor performed better on the resampled dataset that aggregated the values every hour from the original dataset. We were able to predict the % Silica Concentrate with an accuracy of 93.80% on the large original dataset and an accuracy of 62.89% on the small resampled dataset. 

### Presentation
- [PowerPoint](https://github.com/npatel221/SCS-ML-3253---Final-Project/blob/master/presentation/Revised%20Final%20Presentation.ppsx)
- [PDF](https://github.com/npatel221/SCS-ML-3253---Final-Project/blob/master/Final%20Presentation_COPY.pdf)
- [YouTube Video](https://www.youtube.com/watch?v=fvTKZxlI1gE)
- [GoogleDrive](https://drive.google.com/drive/folders/1ifrMKTualLm222UuDd08rrx23e8hT1DN?usp=sharing)
