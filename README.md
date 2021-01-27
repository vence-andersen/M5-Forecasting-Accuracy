# M5-Forecasting-Accuracy
A competition held by Kaggle, *https://www.kaggle.com/c/m5-forecasting-accuracy.*

The **EDA_M5.ipynb** file consist of all the EDA that were done on this data/problem.

The **Feature_Engineering.ipynb** file consist of the feature engineering required for this problem.

The **models.ipynb** consist of the all the models that I tried, which also includes the my best model, the LGBM Regressor based.

*************************************************************************************************************
The **Ensemble_Model.ipynb** consist of the custom ensemble based model, where I first split the data into train and test with 80-20 percent as Train and Test. Then with the 80 percent data I am making 2 cross validation like splitting the whole data approximately on 50 percent each as D1 and D2. Now on D1 I created 5 base models with 'm' number of samples almost 70 percent of data(sampling with replacement) and each model has different algorithms, which I chose based on the score I got with the models that I worked on model.ipynb file.

Then I created a meta model, here for trainig the meta model, I used my D2 data and predicted it's value using my 5 base models i created and created a dataframe with the predicted value. Now this will be the X_train for my meta model and y_train is the true value which we have.

Now for the parameter tuning I used my Test data, which I passed to my 5 base models, created a dataset with the prediction I got from the 5 base models, then I predicted the values on this dataset using the meta model, and calcualted the MSE using true value we have for the test data.

After getting the best parameters, i then predicted the values required for submission using the same way.
**************************************************************************************************************
**Kaggle_score.png** shows my score I got in the competiton, which should be on the **top 5%.**
