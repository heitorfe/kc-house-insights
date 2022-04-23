# King County Houses - Insight Project

<img src="https://user-images.githubusercontent.com/77629603/164895726-ded8c237-d95a-4c08-8655-1dea0a9a4d69.png" alt="" style="width:700px;"/>

# 1.0. Context

House Rocket is a fictitious company that buy and sell real estate in King County (US). Profit comes from the difference between the purchase price and the sale price. 

# 2.0. Business Problem

Increase profit through data analysis. With the database we can find out what most impacts the price of real estate and buy cheap, increase value and sell for a higher price. For that purpose it was developed:
* Dashboard in Power BI;
* Database with the recommended properties;
* Insights from validating hypotheses.

# 3.0 Business Assumptions

* Data available is from May 2014 to May 2015;
* The business model of House Rocket is buy and sell houses, not rent;
* Data meaning:
  * 'yr_renovated' = 0 means not renovated;
  * 'grade', 'condition' and 'view' are subjective variables;
* All the data is available for buying and sell;

# 4.0. Solution

I used Python and Power BI to develop the solution. With the steps below:

## 4.1. Data Collection and Description

The data was download from [Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction/discussion/141767) and loaded in Jupyter Notebook. There were not null values. The raw data contains 21613 rows and 29 columns.

<details>
<summary>Original Data Features</summary>

| Feature       | Definition                                                                        |
|---------------|-----------------------------------------------------------------------------------|
| id            | Unique ID for each property available                                             |
| date          | Date that the property was available                                              |
| price         | Sale price of each property                                                       |
| bedrooms      | Number of bedrooms                                                                |
| bathrooms     | Number of bathrooms. 0.5 = toilet 0.75 = bathroom with shower or bathtub          |
| sqft_living   | Square footage of the apartments interior living space                            |
| sqft_lot      | Square footage of the land space                                                  |
| floors        | Number of floors                                                                  |
| waterfront    | 1 = Waterfront property, 0 = Not waterfront property                              |
| view          | Means how good the view of the property is from 0 to 4                            |
| condition     | Means how good the condition of the property is from 0 to 5                       |
| grade         | Unspecified                                                                       |
| sqft_above    | The square footage of the interior housing space that is above ground level       |
| sqft_basement | /The square footage of the interior housing space  that is below ground level     |
| yr_built      | The year that the construction of the property began                              |
| yr_renovated  | The year of the property’s last renovation                                        |
| zipcode       | What zipcode area the property is in                                              |
| lat           | Lattitude                                                                         |
| long          | Longitude                                                                         |
| sqft_living15 | The square footage of interior housing living space  for the nearest 15 neighbors |
| sqft_lot15    | The square footage of the land lots of the nearest 15 neighbors                   |

</details>

## 4.2. Feature Engineering

Here i created new features from the original database.


<details>
<summary>Features Created</summary>

| Feature   | Definition                                |
|-----------|-------------------------------------------|
| year      | Year extracted from date                  |
| month     | Month extracted from date                 |
| day       | Day extracted from date                   |
| season    | Season of the year                        |
| m²        | Conversion of "sqft_lot" to m²            |
| price/m²  | Price of m²                               |
| city      | City collected via API from lat and long  |
| basement  | Whether the property has basement or not  |
| renovated | Whether the property was renovated or not |

</details>

## 4.3. Data Filtering

Filtering properties with  disproportionate amounts of number of bathrooms and bedrooms.

## 4.4. Exploratory Data Analysis 

Checking the distribution of the variables and validating hypothesis. Here I already delivered the first result for the business, which were the insights.

## 4.5. Creating Recommendation Database

I made a Recommendation Database with SQLite following these criteria:
1. Price is below the median price of the base;
2. Price is below the median price of the zipcode;
3. Property was not renovated

This base correspond to:
* Number of properties: 5646
* % of original database 26.13%
* Total Price $1,685,541,856.00

## 4.6. Creating Dashboard 

I built a dashboard with Power BI to show with data visualization the insights. The dashboard is available in this [link](https://app.powerbi.com/view?r=eyJrIjoiNzExYzgyMDQtZjU5ZC00YzAzLTk4MzItYTI3MGQ2ZDM5MDJhIiwidCI6Ijg3MDk0MzhmLTMzNDItNGI0Yy1hZDY5LTNkMjFlMmY4OTZlOSJ9&pageName=ReportSection25f6ac0f4d2653587e84). It can be accessed everywhere with a smartphone, tablet or desktop.

I also made a [video](https://youtu.be/pgNkOtxIgPI) with my own analyzes.

# 5.0. Top Insights

## Hypotesis 1: Houses with basements are at least 10% cheaper than the rest.

False: Houses with a basement are 27% more expensive on average.

![image](https://user-images.githubusercontent.com/77629603/164895178-b8406bb8-e7b9-4086-ba18-9f2aae5261ed.png)


## Hypotesis 2: The value/m² of the property facing the sea is 50% more expensive than the others

False: Waterfront properties are 37% more expensive

![image](https://user-images.githubusercontent.com/77629603/164895287-09786dc5-6fb0-41c8-8c38-28cdc6518c84.png)


But, the average price is 213% higher

![image](https://user-images.githubusercontent.com/77629603/164895255-ade52319-c201-4ea1-a566-d9c9611dfed6.png)


## Hypotesis 3:

Renovated properties are at least 10% more expensive than not renovated

True: Renovated properties are 20% more expansive than not renovated

![image](https://user-images.githubusercontent.com/77629603/164895326-95089552-5252-488c-9bcf-6337929cffc2.png)

## More insights 

Available in this [video](https://youtu.be/pgNkOtxIgPI).

# 6.0. Results

We can expect conservatively a 20% increase of the profit by choosing the best properties based on the location, features and time. Renovations can be made to increase the value, maybe choosing the number of bedrooms, design, build a basement, etc. 

# 7.0 Next Steps

* Collect more external data of geolocation to know better the relation with the price.
* Analyse more price by area of property.
* Create a Machine Learning model to predict the price based on property features.
* Collect feedbacks of the dashboard and make improvements.




