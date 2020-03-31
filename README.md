# Airbnb-Quality-Classification-Project
I trained a random forest classification model to predict whether or not an Airbnb listing in NYC would be given a high rating based on both Airbnb data and NYC open data sets on art gallery locations and rodent inspections.  

**Data Sources**  
Data for this project came from three data sets across two sources.  

[Airbnb listing data](http://insideairbnb.com/get-the-data.html)  
Note that I only used the listings.csv for NYC

[NYC open data on rodent inspections](https://data.cityofnewyork.us/Health/Rodent-Inspection/p937-wjvj)

[NYC open data on art gallery locations](https://data.cityofnewyork.us/Recreation/New-York-City-Art-Galleries/tgyc-r5jh)  

The data sets were all saved in a postgress database on an AWS ec2 instance.

**Tools**  
Python 3  
  - Pandas  
  - Numpy  
  - SciKit Learn  
  - Matplotlib  
  - Seaborn  
  - psycopg2  
Tableau  
PostgreSQL  
AWS Ec2 instance  

**Data Cleaning**  
data_cleaning.ipynb is a jupyter notebook file with the code used to query and clean the necessary data for the project.  

This notebook saves aibnb_FINAL.csv, which is the csv that is used as input for modeling.ipynb.

**Modeling**  
modeling.ipynb is a jupyter notebook file with the code for some feature engineering and the model training.
The resulting model is a random forest model.

This notebook also saves test_data.csv, which is the data used
in the tableau dashboard for this project.

**Implementation**  
The product of this project was a tableau dashboard which allows a user to look at a map of Airbnb
listings in NYC and filter listings based on a "quality assurance level." This value is the
predicted probability from my random forest model that an Airbnb will receive a high customer rating.
Other filters on the dashboard include borough, neighborhood, and superhost status.  

On the left of the dashboard are three histograms for three of the most important listing features
according to the random forest model, price, amenity count, and the number of years the host
has been a host on Airbnb. These histograms are adjusted as the filters are applied.  

Gabriel_Proj3_Pres.pdf is a pdf of the presentation slides used to present this project.
