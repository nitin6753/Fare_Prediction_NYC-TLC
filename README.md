# Fare Prediction NYC Taxi and Limousine Commission (TLC)
To develop a regression model that helps estimate taxi fares before the ride based on the data that TLC has gathered. The ML model developed could show a fair price prior to the ride. (This is a pedagogical project)

The data set is provided by NYC TLC, [2017_Yellow_Taxi_Trip_Data.csv](2017_Yellow_Taxi_Trip_Data.csv).<br>
For more information on the dataset view the dataset dictionary file -> [Dataset_Dictionary.pdf](Dataset_Dictionary.pdf).

Initial assesment and conclusions are provided in the [InitialAssesment.ipynb](InitialAssesment.ipynb)  jupyter notebook. In this part of the project, I performed an inspection of the data provided by the NY TLC in order to provide key data variables and anomalies to ensure the data provided is suitable for generating clear and actionable insights.<br>

Preliminary Data analysis is performmed in [PreliminaryDataAnalysis.ipynb](PreliminaryDataAnalysis.ipynb) file After looking at the dataset, the two variables that are most likely to help build a predictive model for taxi ride fares are total_amount and trip_distance because those variables show a picture of a taxi cab ride.<br>

Exploratory data analysis is performed in [ExploratoryDataAnalysis.ipynb](ExploratoryDataAnalysis.ipynb) file.
>   * EDA helps to get to know the data, understand its outliers, clean its missing values, and prepare it for future modeling. 
>   * It was observed that most rides are below 6 miles and the maximum trip distance is of 35 miles. Also, most rides costs belo $20, but the maximum value is of $1200. 

`Questions Raised`: Why few trips shows 0 trip distance and still charge non zero fare. I would likely want to know about the trip durations also. Do they affect the fare prices. when the trip durations are highest chronologically.<br>

Descriptive statistics and hypothesis testing is performed in [StatisticalReview.ipynb](StatisticalReview.ipynb) file. 
>   * The goal for this A/B test is to sample data and analyze whether there is a relationship between payment type and fare amount. Discover if customers who use credit cards pay higher fare amounts than customers who use cash. The hypothesis that customer with credit card paid higher fare amount compared to cash is statistically significant and did not occured due to chance. So, enouraging customers to pay with credit card could improve revenue for taxi cab drivers. 
>   * Most importnatly, customers riding for larger trip distance might pay with credit card instead of cash as they might not carry lots of cash. So, there is a likelihood that fare amount also determines the payment method, rather than vice-versa.<br>

Multiple linear regression is performed in [RegressionAnalysis.ipynb](RegressionAnalysis.ipynb) file.
>   * To build model, EDA is performed & then Model Assumptions are cheked.
>   * Feature Engineering is performed by grouping dropoff and pickup locations to calculate `Mean Distance`, `Mean Duration` and `Mean Fare amount`. `Rush hours` are also identified using pickup timings. Training and test datasets were also created.
>   * These variables were used to train the Multiple Regression Model and predict the Fare Amount.
>   * For every 1 mile travelled, 1 minute duration, and Rush hour the fare amount increases by `$1.862727`, `$0.33941`, `$0.272958`, respectively.
>   * Below are the model metrics:
>       * R^2: 0.8593964669421976
>       * MAE: 1.9206528389740898
>       * MSE: 10.1248318524279
>       * RMSE: 3.181954093387882

>   This model explains about 86% variance in the fare amount.

The folder [Figures](Figures) contains all the plots generated during EDA performed using Tableau public. The link for the tableau public page -> [NYC-TLC Tableau Public](https://public.tableau.com/views/NYCTLC_17146140834130/TipAmountDistribution?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link).