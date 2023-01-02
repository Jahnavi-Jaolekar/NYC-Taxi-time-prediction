# NYC-Taxi-time-prediction

PROBLEM STATEMENT

To Build a machine learning model that predicts the duration of NYC taxi trip using the dataset which includes pickup time, geo-coordinates, the number of passengers, and several other variables.

APPROACHES

Step 1:  
Viewing and cleaning data being the initials, we started with importing necessary libraries, mounting drive and storing data in variables for deriving meaningful insights. Presence of null values would have created possible errors in the further steps, so evaluated presence of any null values. 

![NULL COUNT](https://user-images.githubusercontent.com/112775752/210239330-587c4010-8265-423a-bfd2-300810dbce55.png)

Luckily our dataset did not have any null values.

Step 2:

Preprocessing and feature engineering were the next. We had 2 columns in timestamp format, changed them to datetime format. As a part of feature engineering, we created an extra column “distance” using geodesic distance.

Step 3:

Next step being data analysis and visualization, in which we determined peak hours of pickup and drop-offs, months in which taxi services were used maximum, further we also got insights over weekdays with surge in taxi use, etc. Further we dealt with outliers in our data set by using quartile method, we performed multicollinearity correlation check by using heatmaps and VIF

![PICKUPS AND DROPOFFS](https://user-images.githubusercontent.com/112775752/210239591-41ed48ea-1fe7-4e41-afcd-c217c16e5c6c.png)

![PASSENGER COUNT](https://user-images.githubusercontent.com/112775752/210239650-025b50a5-064e-4939-b126-b1564d9d1179.png)

![PD HOURS](https://user-images.githubusercontent.com/112775752/210239680-7b4213a1-9588-4f12-9f87-53d4a8bd422b.png)

![VENDOR TRIPS](https://user-images.githubusercontent.com/112775752/210239719-b68ea342-a457-4d8e-85d4-8678cf081e5b.png)

![HEATMAP](https://user-images.githubusercontent.com/112775752/210239738-b00d231d-2813-41c4-bae7-763e50c3e797.png)

![FEATURE SELECTION](https://user-images.githubusercontent.com/112775752/210239769-54c57b05-9518-48ff-9e43-ca38c3240b75.png)

![SKEWNESSS](https://user-images.githubusercontent.com/112775752/210239802-78ca0e58-371d-45a9-8ee2-b811009db3bf.png)

Step 4:

Final step being our model training where we used 5 different algorithms to train our model (linear regression, decision tree, xg boost, gradient boost, random forest), we compared evaluation metrics for all 5 algorithms and based on that finalized one algorithm for training our model.

SCORES:

![TABLE](https://user-images.githubusercontent.com/112775752/210240179-72e4d13c-fb44-4820-92e5-84484ecc3494.png)

R2 SCORES:

![R2 SCORE](https://user-images.githubusercontent.com/112775752/210240248-b57f0ef2-6c60-46aa-b509-d06e4e1556a9.png)

MSE SCORES:

![MSE SCORES](https://user-images.githubusercontent.com/112775752/210240324-30cdb077-6a5e-4557-87a2-488436695de9.png)

CONCLUSION

(EDA)

As for the exploratory part various insights were obtained, we found out peak months(April and March) when taxi service is used to its maximum, weekdays when service is at surge are Friday and Saturday which suggests that people might be going for weekend parties or celebrations, we also got information on hourly basis  and it we found that mostly pickups and drop-offs are in the morning around 10 am and in the late evenings which suggests that people use taxi service for going to workplace and coming back from there, we also saw that most of the people don’t prefer car pool and are solo travelers. Vendor 2 had a greater number of bookings as compared to vendor 1.

(Model Training)

We tried 5 algorithms(Linear Regression, Decision Tree, XG Boost, Gradient Boost, Random Forest) for model training and compared their evaluation metrics (R2, Adjusted R2, MSE, RMSE).out 5 algorithms we found that only XG Boost gave best accuracy score 71% and low MSE scores followed by Random Forest, we tried taking optimum parameter so that our model doesn’t overfit.
