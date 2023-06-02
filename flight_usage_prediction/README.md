# In-Flight-Connectivity usage predictions

**Author**
Anand George

## Executive summary

Predicting the internet usage pattern of passengers in-flight is a crucial endeavor for delivering an exceptional quality of internet experience to onboard passengers. In today's connected world, air travel has become a common platform for people to stay connected and engaged with their digital lives. With the increasing reliance on internet connectivity during flights, understanding and predicting the internet usage patterns of passengers allows airlines and service providers to optimize their network infrastructure, bandwidth allocation, and service offerings. By accurately anticipating the demands and preferences of passengers, airlines and service providers can proactively tailor their internet services to provide reliable, high-speed connectivity, ensuring a seamless and satisfying online experience. This predictive capability enables service providers to deliver exceptional internet services, enhancing passenger satisfaction, productivity, and overall flight experience, while also optimizing resource utilization and operational efficiency.

Predicting internet usage patterns is a really challenging problem on it's own given the limited set of features available for prediction and challenges in getting clean data about these features.

This project is an attempt at predicting internet usage patterns on a per flight, per 5 min basis given a set of features that are available to service providers ahead of time.

Feature Types used for future predicitons are the following,
Features :-

- [ ] flight specific features
- [ ] internet product specific features
- [ ] time/day/season specific features
- [ ] location specific features
## Rationale

Providing great internet service to commercial airline passengers is one of the primary goals of any IFC service provider. In-order to deliver excellent QoE (Quality of Experience), IFC service providers need to match the demand ( in Mbps ) from all the passengers on an aircraft at any point in space and time with appropriate amount of supply ( expensive satellite resources ). By doing so, they will be able to maximize customer QoE while minimizing satellite resource costs.

This project aims to identify the geo-spatial and temporal nature of internet usage/demand under a set of features that are known to service providers ahead of time. The goal is to be able to generate these features for any future date of interest and have the ability to build a play back of the demand in future in-order to better understand how to deliver right amounts of satellite supply that results in excellent customer satisfaction.

## Research Question

Given a set of features that will be available to service providers about an aircraft in an active commercial flight in future, predict the amount of forward link/downlink datarates/demand per 5 mins per tail id (unique aircraft identifier).

## Data Sources

 Data collected from our own production systems as well as publicly available data (US Dept of transportation )

Publicly availale transportation data collected from [here](https://data.bts.gov/Research-and-Statistics/Transportation-Services-Index-and-Seasonally-Adjus/bw6n-ddqk)

In addition to this, data available to me from my company -- Don't want to call out the specifics inorder to protect the specific details about data.

## Methodology

Using different regression models to predict a real valued output which is the forward link demand in Mbps per tail per 5 min


## Results

When I started this, I was under the impression that it is going to be really hard to predict user behaviours and how much internet will any aircraft use at any 5 mins in time. But after identifying several key features and feature translations, I was able to come up with a prediciton algorithm which produced an R2 score of 0.56, MAPE score of 5.15 and MAE of 3.19 on the test data.

The following is the summary of different regression models

| Model                   | Mean Squared Error (MSE) | Root Mean Squared Error (RMSE) | Mean Absolute Error (MAE) | Mean Absolute Percentage Error   (MAPE) | R^2 Score |      |
|-------------------------|--------------------------|--------------------------------|---------------------------|-----------------------------------------|-----------|------|
| Linear Regression       | 21.53                    | 4.64                           | 3.64                      | 10.11                                   | 0.42      | 0.42 |
| Ridge Regression        | 21.53                    | 4.64                           | 3.64                      | 10.11                                   | 0.42      | 0.42 |
| Lasso Regression        | 21.53                    | 4.64                           | 3.64                      | 10.11                                   | 0.42      | 0.42 |
| Random Forest  | 17.99                    | 4.24                           | 3.15                      | 5.58                                    | 0.52      | 0.52 |
| AdaBoost       | 24.36                    | 4.94                           | 3.85                      | 8.58                                    | 0.35      | 0.35 |


## Next steps

- [ ]  I was using one month of data ( about 50 million records ) for this project so I was not able to incorporate the seasonal nature of airline traffic that I gathered from US Dept of transportation. I would like to add that in as a translation for the month feature, as well as predict out the retunk link usage/demand in Mbps per 5 mins.

- [ ]  Try using automl

## Outline of project

- Main projet notebook [flight_internet_usage_prediction.ipynb]()

- Few Animations under [animations]()

- EDA, Feature dependency viz, Feature importance of best Model [images]()

## Contact and Further Information
<anand.george89@gmail.com>
