### Project Title
Flight Internet Usage Prediction
**Author**
Anand George
#### Executive summary
Generated a Machine Learning model using Random forest regressor to predict the forward link demand in Mbps from any viasat fitted aircraft within 5% of Mean Absolute Error (based on test set error score).

Feature Types used for future predicitons
Features :-
- [ ] flight specific features
- [ ] internet product specific features
- [ ] time/day/season specific features

#### Rationale

Providing great internet service to commercial airline passengers is one of the primary goals of my company, Viasat.inc. In-order to deliver excellent QoE (Quality of Experience), we need to match the demand ( in Mbps ) from all the passengers on an aircraft at any point in space and time with appropriate amount of supply ( expensive satellite resources ). By doing so, we will be able to maximize customer QoE while minimizing satellite resource costs.

This project aims to identify the geo-spatial and temporal nature of internet usage/demand under a set of features that are known to my company ahead of time. I willbe able to generate these features for any future data of interest and have the ability to build a play back of the demand in future in-order to better understand how to deliver right amounts of supply.

#### Research Question
Given a set of features that will be available to me about an aircraft in an active commercial flight in future, predict the amount of forward link/downlink datarates/demand per 5 mins per tail id (unique aircraft identifier).
#### Data Sources
 Data collected from our own systems as well as publicly available data (US Dept of transportation )

Publicly availale transportation data collected from [here](https://data.bts.gov/Research-and-Statistics/Transportation-Services-Index-and-Seasonally-Adjus/bw6n-ddqk)

In addition to this, data available to me from my company -- Don't want to call out the specifics inorder to protect the specific details about data within my company from the public.
#### Methodology
Using different regression models to predict a real valued output which forward link demand in Mbps

#### Results
When I started this, I was under the impression that it is really hard to predict user behaviours and how much internet will any aircraft use at any 5 mins in time. But after identifying several key features and feature translations, I was able to come up with a prediciton algorithm which produced an R2 score of 0.56, MAPE score of 5.15 and MAE of 3.19 on the test data.
#### Next steps
I was using one month of data ( about 50 million records ) for this project so I was not able to incorporate the seasonal nature of airline traffic that I gathered from US Dept of transportation. I would like to add that in as a translation for the month feature, as well as predict out the retunk link usage/demand in Mbps per 5 mins.

#### Outline of project

- [flight_internet_usage_prediction.ipynb]()

- [animations] under animations

- [images] EDA, Feature dependency viz, Feature importance of best Model

##### Contact and Further Information
anand.george89@gmail.com
