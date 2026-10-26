# Airbnb NYC Market Analysis

## Introduction
In this project, I analyzed Airbnb listings in New York City to see how prices differ depending on location, room type, and other factors.
I wanted to find out which areas are the most expensive, what types of accommodation are the most common, and what might be related to Airbnb prices.
I also used linear regression to see how well I could predict prices using the available data.

## Dataset

I used the New York City Airbnb Open Data (2019) dataset from Kaggle.
The dataset contains 48,895 Airbnb listings and 16 columns. It includes information about prices, locations, room types, reviews, minimum nights, and availability.
I started by checking for missing values and duplicates. I also removed 11 listings with a price of 0.
After cleaning, I had 48,884 listings to work with.

## Tools Used
Python
Pandas and NumPy
Matplotlib and Seaborn
Statsmodels
Scikit-learn
Jupyter Notebook
Data Analysis

I started by looking at where Airbnb listings are located in New York City and how prices differ between boroughs.
Most listings are in Manhattan and Brooklyn.
Manhattan has the highest median price at 150 USD per night, while the Bronx has the lowest at 65 USD.
I also compared different room types:
Entire homes and apartments: 160 USD per night

Private rooms: 70 USD per night

Shared rooms: 45 USD per night

Entire apartments are generally more expensive than private and shared rooms.
I also looked at reviews, minimum nights, and availability.
The correlation between price and the number of reviews was around -0.05, while the correlation between price and availability was around 0.08. Both relationships were very weak.
Linear Regression
After exploring the data, I used multiple linear regression to see how different variables were related to Airbnb prices.
I included location, room type, minimum nights, number of reviews, and availability.
I built two models:

Original Price — using the original prices.

Log Price — using the logarithm of prices.
The first model had an R² of 0.092, meaning it explained about 9% of the variation in prices.
The log-price model had an R² of 0.473, meaning it explained about 47% of the variation in log prices.
These results are not directly comparable because the models use different target scales.

## Model Evaluation

I split the data into 80% for training and 20% for testing.
I compared both models using MAE and RMSE.

## Original Price Model

MAE: 72.82 USD

RMSE: 187.69 USD

Log Price Model

MAE: 62.99 USD

RMSE: 189.85 USD

The log-price model had a lower MAE, which means its predictions had smaller absolute errors on average.
However, the original model had a slightly lower RMSE.
Neither model performed better on both metrics.

## Conclusion
In this project, I found that Airbnb prices in New York City differ quite a lot depending on location and room type.
Manhattan was generally the most expensive borough, and entire apartments cost more than private and shared rooms.
The regression models helped me explore how different factors are related to prices, but the predictions were not always accurate.
Other information, such as apartment size, amenities, and more detailed location data, could help improve the models.
