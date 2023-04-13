# Airbnb Analysis - London :uk:

### Date : January 2023

### Team : [Masooma Alghawas](https://www.linkedin.com/in/masoomaalghawas), [Eman Mohamed](https://www.linkedin.com/in/eman-mohemmed), [Jubran AlTaitoon](https://www.linkedin.com/in/jubranaltaitoon), [Budoor Sulaiman](https://www.linkedin.com/in/budoor-sulaiman) & [Saleh Alfardan](https://www.linkedin.com/in/salehalfardan)

### Tools : 
  - Microsoft Excel : Data cleaning, EDA, and Visualization
  - Microsoft PowerPoint: Presentation

### Summary :
Analysis of Airbnb London listings for the purpose of presenting investors interested in entering the Airbnb market in London.  The scope of this analysis involved a comparison of the neighborhoods in London based on the number of listings, average ratings, type of properties, and the estimated average revenue. Then, proposing recommendations for the types of properties and the neighborhoods to invest in within London for Airbnb purposes.

### [Data Source](http://insideairbnb.com/get-the-data/)

### Data Dictionary:
|__Field__ | __Type__ | __Calculated__ | __Description__ | __Reference__|
|------|------|------------|-------------|----------|
|id | integer |  | Airbnb's unique identifier for the listing | |	
|listing_url | text | y | |		
|scrape_id | bigint | y | Inside Airbnb "Scrape" this was part of | |	
|last_scraped | datetime | y | UTC. The date and time this listing was "scraped". | |
|source | text |  | One of "neighborhood search" or "previous scrape". "neighborhood search" means that the listing was found by searching the city, while "previous scrape" means that the listing was seen in another scrape performed in the last 65 days, and the listing was confirmed to be still available on the Airbnb site. | |	
|name | text |  | Name of the listing | |	
|description | text |  | Detailed description of the listing | |
|neighborhood_overview | text |  | Host's description of the neighbourhood | |	
|picture_url | text |  | URL to the Airbnb-hosted regular-sized image for the listing | |	
|host_id | integer |  | Airbnb's unique identifier for the host/user | |	
|host_url | text | y | The Airbnb page for the host | |	
|host_name | text |  | Name of the host. Usually just the first name(s). | |	
|host_since | date |  | The date the host/user was created. For hosts that are Airbnb guests this could be the date, they registered as a guest. | |	
|host_location | text |  | The host's self reported location | |	
|host_about | text |  | Description about the host | |	
|host_response_time |  |  |  | |				
|host_response_rate |  |  |  | |				
|host_acceptance_rate |  |  | That rate at which a host accepts booking requests. | |	
|host_is_superhost | boolean |  | [t=true; f=false] | |		
|host_thumbnail_url | text |  |  | |			
|host_picture_url | text |  |  | |			
|host_neighbourhood | text |  |  | |			
|host_total_listings_count | text |  | The number of listings the host has (per Airbnb calculations) | |	
|host_verifications |  |  |  | |				
|host_has_profile_pic | boolean |  | [t=true; f=false] | |			
|host_identity_verified | boolean |  | [t=true; f=false] | |			
|neighbourhood | text |  |  | |			
|neighbourhood_cleansed | text | y | The neighborhood is geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. | |	
|neighbourhood_group_cleansed | text | y | The neighborhood group is geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. | |	
|latitude | numeric |  | Uses the World Geodetic System (WGS84) projection for latitude and longitude. | |	
|longitude | numeric |  | Uses the World Geodetic System (WGS84) projection for latitude and longitude. | |	
|property_type | text |  | Self selected property type. Hotels and Bed and Breakfasts are described as such by their hosts in this field | |	
|room_type | text |  | "Entire home/apt, Private room, Shared room, Hotel<br><br>All homes are grouped into the following three room types:<br>Entire place<br>Private room<br>Shared room<br>Entire place<br>Entire places are best if you're seeking a home away from home. With an entire place, you'll have the whole space to yourself. This usually includes a bedroom, a bathroom, a kitchen, and a separate, dedicated entrance. Hosts should note in the description if they'll be on the property or not (ex: "Host occupies the first floor of the home"), and provide further details on the listing.<br><br>Private rooms<br>Private rooms are great for when you prefer a little privacy and still value a local connection. When you book a private room, you'll have your private room for sleeping and may share some spaces with others. You might need to walk through indoor spaces that another host or guest may occupy to get to your room.<br><br>Shared rooms<br>Shared rooms are for when you don't mind sharing a space with others. When you book a shared room, you'll be sleeping in a space that is shared with others and share the entire space with other people. Shared rooms are popular among flexible travelers looking for new friends and budget-friendly stays." | https://www.airbnb.com/help/article/5/what-does-the-room-type-of-a-listing-mean |
|accommodates | integer |  | The maximum capacity of the listing | |	
|bathrooms | numeric |  | The number of bathrooms in the listing | |	
|bathrooms_text | string |  | "The number of bathrooms in the listing.
On the Airbnb website, the bathrooms field has evolved from a number to a textual description. For older scrapes, bathrooms are used." | |	
|bedrooms | integer |  | The number of bedrooms | |	
|beds | integer |  | The number of bed(s) | |	
|amenities | json |  |  |  | 			
|price | currency |  | daily price in local currency | |	
|minimum_nights | integer |  | minimum number of night stay for the listing (calendar rules may be different) |  | 	
|maximum_nights | integer |  | maximum number of night stay for the listing (calendar rules may be different)	 |  | 
|minimum_minimum_nights | integer | y | the smallest minimum_night value from the calendar (looking at 365 nights in the future) |  | 	
|maximum_minimum_nights | integer | y | the largest minimum_night value from the calendar (looking at 365 nights in the future)	 |  | 
|minimum_maximum_nights | integer | y | the smallest maximum_night value from the calendar (looking at 365 nights in the future)	 |  | 
|maximum_maximum_nights | integer | y | the largest maximum_night value from the calendar (looking at 365 nights in the future)	 |  | 
|minimum_nights_avg_ntm | numeric | y | the average minimum_night value from the calendar (looking at 365 nights in the future)	 |  | 
|maximum_nights_avg_ntm | numeric | y | the average maximum_night value from the calendar (looking at 365 nights in the future)	 |  | 
|calendar_updated | date |  | |  |  			
|has_availability | boolean |  | [t=true; f=false] |  | 	
|availability_30 | integer | y | avaliability_x. The availability of the listing x days in the future is determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. | |
|availability_90 | integer | y | avaliability_x. The availability of the listing x days in the future is determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. |  | 	
|availability_365 | integer | y | avaliability_x. The availability of the listing x days in the future is determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. |  | 	
|calendar_last_scraped | date |  |  |  | 			
|number_of_reviews | integer |  | The number of reviews the listing has |  | 	
|number_of_reviews_ltm | integer | y | The number of reviews the listing has (in the last 12 months) |  | 	
|number_of_reviews_l30d | integer | y | The number of reviews the listing has (in the last 30 days)	 |  | 
|first_review | date | y | The date of the first/oldest review |  | 	
|last_review | date | y | The date of the last/newest review|	
|review_scores_rating |  |  |  |  | 				
|review_scores_accuracy |  |  |  |  | 				
|review_scores_cleanliness |  |  |  |  | 				
|review_scores_checkin |  |  |  |  | 				
|review_scores_communication |  |  |  |  | 				
|review_scores_location |  |  |  |  | 				
|review_scores_value |  |  |  |  | 				
|license | text |  | The licence/permit/registration number |  | 	
|instant_bookable | boolean |  | [t=true; f=false]. Whether the guest can automatically book the listing without the host requiring to accept their booking request. An indicator of a commercial listing. |  | 	
|calculated_host_listings_count | integer | y | The number of listings the host has in the current scrape, in the city/region geography. |  | 	
|calculated_host_listings_count_entire_homes | integer | y | The number of Entire home/apt listings the host has in the current scrape, in the city/region geography |  | 	
|calculated_host_listings_count_private_rooms | integer | y | The number of Private room listings the host has in the current scrape, in the city/region geography |  | 	
|calculated_host_listings_count_shared_rooms | integer | y | The number of Shared room listings the host has in the current scrape, in the city/region geography	 |  | 
|reviews_per_month | numeric | y | The number of reviews the listing has over the lifetime of the listing |  | 	

### Data Handling Summary:
1. We removed unuseful columns. __*(36 columns)*__	 
2. We checked for duplicated id.	 
3. We checked the price column for negative values, outliers, and nulls. __*(Deleted 19 rows with null values deleted)*__	 
4. We fix a typo in a cell in neighbourhood_cleansed. __*("Shepherd‚Äôs hut" to "Shepherd's hut")*__	 
5. Reformated the price to currency.	 
6. Added a new column to calculate 'estimated revenue'.	 
7. Added a new column to calculate the number of years the property was listed by estimating the difference between the first review and the last review.

__Columns__

_Key:_
|  |__key map__|
|--|-------|
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|__used columns__|
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|__removed columns__|

|   |__Column name_|__Note__|__Data Type__|
|---|------------ | ------ | ------|
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|id |Numeric| No duplicated|
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)| listing_url	|| | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)| scrape_id	||| 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)| last_scraped ||| 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)| source	 ||| 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|name	 || |
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|description |||  	
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|neighborhood_overview	 ||| 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|picture_url	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_id	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_url	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_name	 | | | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_since	 |Date|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_location	 ||| 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_about	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_response_time |Categorical|  |
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_response_rate|Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_acceptance_rate	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_is_superhost	 |Boolean|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_thumbnail_url	 || |
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_picture_url	 || |
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_neighbourhood	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_listings_count	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_total_listings_count	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_verifications	 | || 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|host_has_profile_pic	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|host_identity_verified	 |Boolean|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|neighbourhood	 ||| 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|neighbourhood_cleansed |Categorical|  | 	
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|neighbourhood_group_cleansed || blanks | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|latitude	 || |
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|longitude	 || |
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|property_type	 |Categorical|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|room_type	 |Categorical|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|accommodates	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|bathrooms | |blanks |
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|bathrooms_text	| |  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|bedrooms	 |  | |
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|beds |Numeric| | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|amenities	 |  | |
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|price |Numeric| 19 record remeoved | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|minimum_nights	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|maximum_nights	 ||  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|minimum_minimum_nights	| |  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|maximum_minimum_nights	 ||  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|minimum_maximum_nights	 ||  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|maximum_maximum_nights	 | | | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|minimum_nights_avg_ntm	 |  || 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|maximum_nights_avg_ntm	 |  || 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|calendar_updated || blanks | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|has_availability	 |Boolean|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|availability_30	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|availability_60	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|availability_90	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|availability_365	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|calendar_last_scraped	 |Date  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|number_of_reviews	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|number_of_reviews_ltm	 | | | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|number_of_reviews_l30d	 | | | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|first_review	 |Date|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|last_review	 | | | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_rating |Numeric|  | 	
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_accuracy	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_cleanliness	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_checkin	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_communication	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_location	 Numeric||  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|review_scores_value	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|license || blanks | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|instant_bookable	 |Boolean|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|calculated_host_listings_count |Numeric|  | 	
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|calculated_host_listings_count_entire_homes |Numeric|  | 	
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|calculated_host_listings_count_private_rooms	 |Numeric|  | 
|![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png)|calculated_host_listings_count_shared_rooms	 |Numeric|  | 
|![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png)|reviews_per_month	 | | |
|   | No_Years |Numeric|Calculated Column|
|   | Revenue |Numeric|Calculated Column|

### EDA (Exploratory Data Analysis):
__Q: What’s the count of observations (rows) and features (columns)?__

_A: 69332 Observations (rows) & 40 Features (columns)_

__Q: Are there any features that are dependent on other features in your data?__

_A: Yes, as example the reviews_score_rating depend on review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value_

__Q: What's the data type of each feature — categorical or numerical?__

_A: Both, Categorical and Numerical_

__Q: What is the most number of rental properties (host_listings_count or host_total_listings_count) that one person or company has?__

_A: host id: 28820321 listings owned by the host: 285_

__Q: Is it easy to tell the difference between people renting out properties, and companies renting out properties? If so, how?__

_A: No, we didn't have enough data to tell difference between people and companies renting out properties._

__Q: Which neighborhoods host the most listings?__

_A: Westminster with 7758 listings_

__Q: What is the average neighborhoods rating?__

_A: All neighborhoods have a high rate between 4.5-5_

__Q: What property type received the most positive reviews?__

_A: Entire rental unit ( 32.86% of positive reviews )_
