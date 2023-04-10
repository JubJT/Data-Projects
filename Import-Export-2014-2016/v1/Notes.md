# Global Trade Insight: Import & Export 2014-2016

Date: February 2023

Team: Mohammed Jaafar & Jubran AlTaitoon

Tools: 
  - SQLite : Data cleaning
  - Tableau: EDA, Visualization & Presentation ([Presentation including interactive Dashboard](https://public.tableau.com/views/GlobalInsightImportandExport2014-2016/GlobalInsightImportExport2014-2016?:language=en-GB&:display_count=n&:origin=viz_share_link))

### [Data Source](https://www.kaggle.com/datasets/unitednations/global-commodity-trade-statistics)

### Data Cleaning:
The dataset contains international commodities trade transaction records from 1988 - 2016.
Number of Features (Columns): 10
Number of Observations (Rows): 8.23M 

- Using SQLite to filter the data to the last three years (2014-2016)
- Using Tableau to create a calculated field Balance of Trade. _Balance of Trade is the difference between the value of a country's exports and the value of a country's imports for a given period._

### Data Dictionary:
| Column | Discription|
|--------|------------|
|country_or_area|Country name of record|
|year|Year in which the trade has taken place|
|comm_code|Per the World Customs Organization: The Harmonized Commodity Description and Coding System generally referred|
|commodity|The description of a particular commodity code, i.e. "Horses, live pure-bred breeding"|
|flow|Flow of trade i.e. Export, Import|
|trade_usd|Value of the trade in USD|
|weight_kg|Weight of the commodity in Kilograms|
|quantity_name|A description of the quantity measurement type given the type of item (i.e. Number of Items, Weight in|
|quantity|Count of the quantity of a given item based on the Quantity Name|
|category|Category to identify commodity|
