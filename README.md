## Exploratory data analysis of US-Accidents dataset

by Nikhil

Data source : 
1. US-Accidents Data : https://www.kaggle.com/sobhanmoosavi/us-accidents
2. US-Census (2020) Data: https://www.kaggle.com/darinhawley/us-2021-census-cities-populations-coordinates

Data structure: The US_Accident csv file include 1.5 M rows and 47 coloumns.

" **60+ Insights were found from the dataset** " The data analysis part is done in Google colab platform.
Librarires used: Pandas, Matplotlib, Seaborn, Numpy.

### Description

This is a countrywide car accident dataset, which covers 49 states of the USA. This dataset has been collected in real-time, using multiple Traffic APIs and is collected from February 2016 to December 2020. Currently, there are about 1.5 million accident records in this dataset.

Apart from the US_Accident data set, I ahve also used a US population census dataset for each state and City, to verify the findings from Accident dataset with the population.

### Application of dataset

US-Accidents can be used for numerous applications such as real-time accident prediction, studying accident hotspot locations, casualty analysis and extracting cause and effect rules to predict accidents, or studying the impact of precipitation or other environmental stimuli on accident occurrence.

### Questions:



I have tried to answer these questions with great depth and good visuals:

1. Which city in US has reported the most number of accident cases?
2. Which 5 states reported the highest number of accident cases?
3. Which timezone reported the most number of accident cases?
4. Which street is most accident prone in US?
5. What time of the day are accidents most frequent in?
6. Which days of the week have the most accidents?
7. Which months have the most accidents?
8. What is the trend of accidents year over year (decreasing/increasing?)
9. Effects of road condition on the accident cases.
10. How did the weather conditions affected the cases?



### Data Analysis:

The Number column had almost 70% data missing, Precipitation(in) and Wind_Chill(F) also had >=30% data missing. Since, Number column (which shows the street number) had majority of its data missing, I dropped it.

### (a) City: 

As there are 10657 unique cities, I can't plot data for all of them. So, I plotted data of cities which had reported more than 10k accident cases.

[image]

- We see that Los Angeles had the largest number of accidents (it is also the 2nd most populated city of US), Miami is the city with 2nd highest no. of accident cases reported(bcz Miami city is in more than 1 state).

### (b) State:

Next, I see which state reported the most number of accidents.

[image]

- I see that California (CA) had the most number of accidents,followed by Florida, Oregon, Texas and New york. It appears to be right as California also has the largest population.
- In past 5 years, on average 246 accidents (daily) happened in California, implies approximately 10 accidents per hour.

### (c) Timezone:

Lets see how the accidents cases reported varies with different tiomezones.

[image]

- US/Eastern timezone region reported the most number of accident cases (Census data also shows that the population in this timezone is also the largest), followed by US/Pacific, US/Central and US/Mountain.
- Eastern and Pacific timezone regions accounts for about 76% of the accident cases. Interestingly, these two regions also accounts for about 72% of the population.

### (d) Street:

I tried to answer which street is more prone to accidents?

[image]

- 26,645 (28.64%) accidents occured on Street I-5 N in the last 5 years (2016-2020) in US.
- On average 14 accidents were reported on street I-5 N per day.

### (e) Time:

It is interesting but obvious to see the time at which more accident cases were reported.

[image]

- Highest number of accidents occur between 3:00PM - 6:00PM, and between 6:00AM - 9:00AM (Possibly because of work hours).
- In evening, around 27% of the road accidents occurred in between 3:00PM to 6:00PM.
- Around 18% of the road accidents occurred in between 6:00AM to 9:00AM.
- The most-deadliest accident hour is 5:00PM implies the Evening Office-Returning Hours.
- The 2nd most-deadliest accident hour is 8:00AM implies the Morning Office-Going Hours.

### (f) Day:

I observed an interesting thing while I was looking at accident cases data for different days.

[image]

- Thrusday reported the highest no of cases.
- It looks like overall it is evenly distributed on the business days.
- Only around 17% of the cases were reported on weekends.
- Working Days of the week have almost 2 times higher accident percentage, compared with the Weekend Days which is expected.

As a surprise, there are less accidents occuring on the weekends. It will be interesting to see how the accidents are distributed over the weekend w.r.t time.

[image]

- On the weekends, the distribution of accidents taking place over the day looks very different from that of on weekdays. It is more distributed through out the day, instead of peaking at a specific hour range.

### (g) Month:

Lets see how the accidents are distributed over the months.

[image]

- Around 18% of the cases are reported in December.
- July is the month with least (3.54%) no. of road accidents in US.
- 45% of the road accidents occurred only within the 3 months, October to December
- Towards the end of the year the number of accidents is quite high.

Lets try to figure out why there are more accidents towards the end of the year? Lets try to look at it for different years.

[image]

- I can see that for year 2016,2019,2020 less data was recorded for first 6 months. This could explain why we observed more accident cases reports in the last quarter of the year.
- The dataset is a compilation of records from different sources, it means that the source has missing data.


### (h) Year:

Lets take a look at the trends of accidents year over year.

[image]

- The trend is almost exponentially increasing year by year with a sharp rise in year 2020.
- Year 2020 reported half of the cases in the whole data set.
- 65661 accidents reported per month in year 2020.


### (i) Road Conditions:

Road conditons like presence of a U-turn, bump, crossing etc can cause accidents.

[image]
[image]

- Almost in every case (99.98%) Bumper was absent in the accident spot.
- In 5.7% cases, road accidents happened near the crossing.
- In 98.83% cases, there were no Stop near the accident area.
- 13.49% road accident cases recorded near the junctions.
- There are no accident cases recorded near the Turning Loop.
- 11.21% road accident cases recorded near the traffic signal.


### (j) Weather conditions:

Weather conditons can have drastic effects on the number of accident cases. Lets take a look at them,

[image]
[image]
[image]
[image]

- Maximum no of cases occured between temperature range: 40-80 F.
- Humidity increases the no of cases also increases.
- Higest no of accident occured when the air pressure range is between 20(in) - 30(in).
- Large no. of cases were reported for wind chill range between 51(F) - 71(F).
- Maximum cases were recorded for the wind speed range between 5(mph) - 10(mph), which is not much and thus it is not a major cause behind the accidents.
- In maximum cases of road accident, the Visibility range is between 5(mi) - 10(mi), which is quite good and thus it is not a major cause behind the accidents.
- Weather condition was Fair most of the time and thus it is not a major cause behind the accidents.



### Citation
- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. “A Countrywide Traffic Accident Dataset.”, arXiv preprint arXiv:1906.05409 (2019).
- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. “Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights.” In proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, ACM, 2019.
