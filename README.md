# Car-Price-Prediction

 This is an application where I am trying to predict the resale value of a car based on the previous data of Cardekho.com which I have used from Kaggle  (https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho).

 The price is predicted based on Features like Year of Manufacturing,Selling Price ,Present Price ,Kms Driven,Fuel Type, Seller Type , Transmission Type and Type of Owner.
 
### Data Exploration and Cleaning.

-> We  create a variable "age of Vehile " and find age of the vehile by subtraciting Manufacturing Year from Present year.

-> We have three categoreis in Fuel type (CNG,Petrol and Diesel) , we covert Fuel Type(which is categorical Variable) to Dummy/Indicator Variables like Fuel_Type_Diesel and Fuel_Type_Petrol. To Decrease the number of Varibale we use "drop_first = True" which leaves us two variables "Fuel_Type_Diesel" and "Fuel_Type_Petrol". So when both the variables have 0 as a value this means the Fuel_type of the Vehicle would have been "CNG".

-> As we don't want current Year as a varibale any more we drop the column from the data set.

### Data Visualization and Analysis
-> To see the relationship between the two variables we find the correlation value of every variable with each other.

-> To get a better visualization we plot a heat map 



