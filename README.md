# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
Goal of the project is to be able to pull data from API's and use that data to join together as a single table and create a model for the data. 

## Process
- chose a city and pulled bike station data from the citybikes API (origianlly chose Ljubljana, but ended up choosing Glasgow, Scotland)
- pulled information for all the bike stations from the first step from the foursqure API
- pulled information for all the bike stations from the first step from the yelp API
- joined the output from the citybikes API to the output from the Yelp API (chose to go with just the Yelp API as there was more information pulled from it). The data was joined on the latitude/longitude - which was each bike station
- created a model with "number of bikes" as the dependent variable. first put "rating", "noOfReviews", and "distance" as independent variables 
- then removed "rating" from the model as th p-value was >5


## Results
The Yelp API gave output for more "businesses" that the foursquare API did. I put the same points of interest in both(bars, lodging, historicsites). The Yelp API also had more information stored within each business as well. In the end for my model I just combined the results from the Yelp API to the citybikes API. The information from the foursquare API was similar to Yelp so did not need to be repeated. 

The top 10 rated businesses for yelp were:

Sapori d'Italia 		5.0 	16 	

Sapori d'Italia 		5.0 	16 	

Sapori d'Italia 		5.0 	16 	

Sapori d'Italia 		5.0 	16 	

Sapori d'Italia 		5.0 	16 	

Wee Lochan 		        5.0 	15 	

Two Fat Ladies 	        5.0 	15 

Two Fat Ladies  	    5.0 	15 

Two Fat Ladies 		    5.0 	15 

Two Fat Ladies 	 	    5.0 	15 

Wee Lochan 	 	        5.0 	15 

Wee Lochan 	            5.0 	15 

As there were more than 10 results with a 5 rating, I then took those with the most reviews as a second thing to consider. Those with more ratings were considered stronger than those with less ratings. 12 were chosen in the end as the next only had 13 reviews. 


The model had a best fit with number of reviews and distance, however there was issues with multicollinearity. 

## Challenges 
The challenges I faced with this project was intially having issues pulling the data from API's. Once I was able to figure out how to properly pull the data from the yelp API I realized the city I had initially chosen was not supported there, so needed to start over with a new city. 

I did have some issues understanding the looping of data to do all the steps more efficiently. I also had isssues executing the SQLite. 

## Future Goals
With more time I might pull more information from the API's to have more information to put into the model and to be able to try different inputs to the model. 

With more time I would also like to do some more data exlpoation, look into ways of handling data assumptions - example model indicated strong mulitcollinearity. Overall have a more polished project. 
