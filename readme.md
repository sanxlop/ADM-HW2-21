# Homework 2 - How do Taxis move in NYC?
In this assignment we perform an analysis of Taxis in NYC using the open data of Taxi's trips in NYC. In particular we take into account the data related to Yellow cabs in the city of New York.
## Data to analyze
We used the data of the [Yellow Cabs](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml) for the year 2018. The data we have been able to retrive is the one about Q1 and Q2, since the data of the Q3 and Q4 has not been released yet.
## Additional data
We used also additional data provided in the [Homework 2 repository](https://github.com/CriMenghini/ADM-2018/tree/master/Homework_2). In particular we used the [CSV](https://github.com/CriMenghini/ADM-2018/blob/master/Homework_2/taxi_zone_lookup.csv) containing additional informations about NYC boroughs and district, which has been combined with the main dataset to give meaning to some IDs contained in the database; we used as well the **old** version of the (GeoJSON)[https://github.com/CriMenghini/ADM-2018/blob/master/Homework_2/taxi_zones.json] provided in the Homework 2 repository, the one that was giving the maps of the boroughs. Since we did not notice that this has been changed on the homework ongoing, and since we decided to go more specific showing the data with the districts instead of the boroughs, we used an additional GeoJSON from [data.betaNYC](http://data.beta.nyc/dataset/nyc-zoning-districts). We noticed just after that the JSON had been changed, but we decided to keep both maps, they explain different aspects of the same data.
## List of files
1. `Homework2.ipynb`
⋅⋅⋅This ipython notebook contains the answer to all the RQs and CRQS. Here you will find all the data analysis we did on NYC taxis.
2. `results\` 
...It's a subfolder containing all the saved Choropleth maps outputs from CRQ2, that can be consulted in case they cannot be seen on the jupyter notebook. The maps displays correctly on Safari and Firefox on the `Homework2.ipynb`, meanwhile has problem rendering in Chrome.
## RQs briefing
### RQ1
In this RQ we analyze the period of the year in which taxis are more used. Therefore, we calculate the average of trips per day in each month taking into account multiple factors and filtering the data. This first exercise has served as a basis for the extraction and manipulation of data for the following ones. Next, we analyze the same situation for each borough. 

People that worked on this RQ: Alberto Sanchez and Federica Spoto.
### RQ2
In the second RQ the porpouse was to find what were the time slots with more passengers. We started fixing time slots of 1 hour, since we thought they were small enough to have an idea of what is going on during all the day, but large enough to be a significative summary of what was happening in that slot. We then procecced the data and looked at the result for the overall New York City and by single Borough, ending with some explainations about what has been observed.

People that worked on this RQ: Fabio Montello.
### RQ3
The objective of this RQ is to analyze the duration of travel in New York and each of the boroughs. So we obtain the duration from the timestamp of departure and arrival and then we plot the results.

People that worked on this RQ: Alberto Sanchez.
### RQ4
The main purpose of this RQ is to find out which of the possible ways of payment is the most common. With this aim, we analyze the frequency distribution of the variable “payment type” in all the city and the contingency table for the joint distribution of the variables "payment type" and "boroughs." Eventually we run the Chi-Squared test to see whether there is a correlation between these two variables. 
People that worked on this RQ: Federica Spoto.
### RQ5
In the RQ5 were trying to see if there was a correlation between the distance and the duration of the trip on average. After reading the data, we retrived the duration of the trip from the dataset and we computed the mean of it, according to every trip distance we had. The we plotted the dataset to see if we had to expect any kind of correlation, and then computed the Person Coefficient to get the real correlation with and without some outliners.

People that worked on this RQ: Federica Spoto, Fabio Montello.
### CRQ1
The main goal of this RQ is to find if the fare for mile change across NY's borough. First, we analyze the prices per mile and then add a temporary variable (duration of each trip) to compare the results using statistical tests.

People that worked on this RQ: Alberto Sanchez with statistical help of Federica Spoto to understand some staff.
### CRQ2
For each yellow cab trip this research question wanted to explore better the zones the Taxi pick up and drop off the users. We started testing how the Choropleth maps using folium were working, then we displayed the processed data of how many pick ups and drop off we had for each borough. We did some more considerations removing Manhattan from the data, and then we repeated the same exploration, this time by districts instead of boroughs.

People that worked on this RQ: Fabio Montello.