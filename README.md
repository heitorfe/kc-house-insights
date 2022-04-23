# King County Houses - Insight Project

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
  * 'city' was collect via API from 'lat' and 'long'; 
  * 'grade' and 'condition are subjective variables;
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

table

</details>

## 4.3. Data Filtering

## 4.4. Exploratory Data Analysis 

## 4.5. Creating Recommendation Database

# 5.0. Top Insights

## H1:

## H2:

## H3:

# 6.0. Results

## 6.1. Dashboard in Power BI

## 6.2. Recommendation




