# Fare Prediction NYC Taxi and Limousine Commission (TLC)
To develop a regression model that helps estimate taxi fares before the ride based on the data that TLC has gathered. The ML model developed could show a fair price prior to the ride. (This is a pedagogical project)

The data set is provided by NYC TLC, [2017_Yellow_Taxi_Trip_Data.csv](2017_Yellow_Taxi_Trip_Data.csv).<br>
For more information on the dataset view the dataset dictionary file -> [Dataset_Dictionary.pdf](Dataset_Dictionary.pdf).

Initial assesment and conclusions are provided in the [InitialAssesment.ipynb](InitialAssesment.ipynb)  jupyter notebook. In this part of the project, I performed an inspection of the data provided by the NY TLC in order to provide key data variables and anomalies to ensure the data provided is suitable for generating clear and actionable insights.<br>

Preliminary Data analysis is performmed in [PreliminaryDataAnalysis.ipynb](PreliminaryDataAnalysis.ipynb) file After looking at the dataset, the two variables that are most likely to help build a predictive model for taxi ride fares are total_amount and trip_distance because those variables show a picture of a taxi cab ride.

Exploratory data analysis is performed in [ExploratoryDataAnalysis.ipynb](ExploratoryDataAnalysis.ipynb) file. EDA helps to get to know the data, understand its outliers, clean its missing values, and prepare it for future modeling.
  * I have learned that most rides are below 6 miles and the maximum trip distance is of 35 miles. Also, most rides costs belo $20, but the maximum value is of $1200.
  * My other questions are why few trips shows 0 trip distance and still charge non zero fare.
  * My client would likely want to know about the trip durations also. Do they affect the fare prices. when the trip durations are highest chronologically.
