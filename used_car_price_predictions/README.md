# used-car-predictions

An attempt to predict the price of used cars in US

## Data set used

Under data/vehicles.csv

## Business Problem

Understand what factors make a car more or less expensive.  As a result of the analysis, provide clear recommendations to a used car dealership -- as to what consumers value in a used car

## Predition Models used

Linear Regression, Ridge Regression, Lasso Regression.
Explorer Hyper parameter tuning, different cross validation techniques, numrical feature scaling, categorical feature encoding - onehot encoding, ordinal encoding (used box plots of categorical features against output variable to identify the orders).

## Findings

After analyzing 300 thousand records of past used car sales from all states within the US with a wide variety of price ranges and involving about 41 different car manufacturers, what I have found out is that the following are the key elements that drive the price of a used car in the US in the order of importance

1. Age of the car in years ( affects price negatiely )
2. Miles travelled by the car (odometer reading) ( affects pricve negatively )
3. Diesel cars have better resale value than gasoline cars
4. The following manufacturer's cars seems to have good resale value given other parameters like age of the car and odometer remains the same,
    Tesla,Porsche, Lexus, Rover, Austin Martin, Land Rover, Audi , Mercedes Benc, Alpha romeo in that order
5. The following  manufacturer's cars seems to have a negative influence on resale value given all other things remain the same,
    Ferrari, organ
6. Manual transmission cars seems to have better resale value compared to the others.
