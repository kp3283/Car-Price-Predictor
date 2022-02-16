# Car-Price-Prediction

 This is an application where I am trying to predict the resale value of a car based on the previous data of Cardekho.com which I have used from Kaggle  (https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho).

 The price is predicted based on Features like Year of Manufacturing,Selling Price ,Present Price ,Kms Driven,Fuel Type, Seller Type , Transmission Type and Type of Owner.
 
### Data Exploration and Cleaning:

-> We  create a variable "age of Vehile " and find age of the vehile by subtraciting Manufacturing Year from Present year.

-> We have three categoreis in Fuel type (CNG,Petrol and Diesel) , we covert Fuel Type(which is categorical Variable) to Dummy/Indicator Variables like Fuel_Type_Diesel and Fuel_Type_Petrol. To Decrease the number of Varibale we use "drop_first = True" which leaves us two variables "Fuel_Type_Diesel" and "Fuel_Type_Petrol". So when both the variables have 0 as a value this means the Fuel_type of the Vehicle would have been "CNG".

-> As we don't want current Year as a varibale any more we drop the column from the data set.

### Data Visualization and Analysis:
-> To see the relationship between the two variables we find the correlation value of every variable with each other.

-> To get a better visualization we plot a heat map 
![HeatMap](https://user-images.githubusercontent.com/92235451/150414510-9fc1d3b8-6468-4812-b5a4-35bb320a154b.png)


-> To improve the prediction ( pridictive accuracy and control over fitting) we import "ExtraTreeRegressor" class from sklearn.ensemble library.

-> We find that these are the top 5 relevant features of the model.It can help with better understanding of the solved problem and sometimes lead to model improvements by employing the feature selection.

![Relative image](https://user-images.githubusercontent.com/92235451/150423099-a2059f11-de2d-4f69-a0d7-e121f727a332.png)

### Developing Model:
-> For training and testing of data I have use train_test_split of sklearn library.

-> RandomForestRegressor algorithm is used to develope the base model. I have used RandomForestRegressor instead of ExtraTreeRegressor because with ExtraTreeRegressor ( it is faster than RandomForestRegressor) but if the data is redundant or repeated frequently the variance will increase and this will decrease the efficiency of the model.

-> I have used RandomizedsearchCV to find the best solution for the built model. The reason of selecting RandomizedSearchCV instead of GridsearchCV because it will randomly select the parameter combinations and for Grindsearchcv we need to specify the parameter combinations. This has increased the the model generalizability.

-> Precision of the outcome of the model was visulaized with scatter plot.

![scatter](https://user-images.githubusercontent.com/92235451/150428001-80f44aa1-f404-48db-8ab7-4b9fbba18d5a.png)


# Here is the link for the application : https://car-sellprice.herokuapp.com/

