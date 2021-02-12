# Zillow Home Listing Price Prediction

**Objective**

- Predicting home listing prices in Vermont on a number of features.

**Data Sources**

- Zillow (728 homes)
- County Level Median Income - United States Department of Housing and Urban Development 

**Tools Used**

- Scraping: Beautiful Soup, Selenium
- Modelling: pandas, sklearn
- Visualization: Seaborn, Yellowbrick

**Features and Target Variables**

- Target Variable: Zillow Home Listing Price
- Final Features: 
  - On Waterfront 
  - Bathrooms **X** Year Built 
  - Home Sq. Ft. **X** ((Lot size Sq. Ft.) ^ 2)
  - View Description
  - Home Sq. Ft. ^ 3
  - Bathrooms ^ 3
  - On Waterfront **X** Home Sq. Ft.
  - On Waterfront **X** Bedrooms
  - View Description **X** Bathrooms 
  - On Waterfront **X** View Description
  - Zip Code (Top 15 and all other grouped as "Other")

**Results Summary**

The key factors contributing to home listing price were square footage cubed and whether a home was on waterfront.  A simple model of just square footage cubed resulted in a R2 of  0.34 and a more complex model yielded an R2 of 0.55 with an RMSE of $313,308 and MAE of $178,156.

**Next Steps**

Given the small number of data point, more data must be collected to regularize and improve the model.  The model final model was overfit to a high degree (training R2 = 0.91); however due to the limited datatpoints, applying a Lasso model did not improve overfitting.  A method for screening for home condition and the accuracy of key categorical variables is needed to improve the model.  This is due to a significant premium for renovated homes and major discrepancies between key categorical variables (i.e. waterfront).

**File Contents**

Pickle Files & csvs

- Saved from web scraping

Notebooks

- `Zillow_Scraping_Links.ipynb` contains all web-scraping for initial links to VT home listings.

- `Zillow_Scraping_Property_Info.ipynb` contains all web-scraping collected for individual homes.

- `ZillowModels.ipynb` contains all data cleaning, modelling and visualization for the project.

  

  
