## Exploratory data analysis of US-Accidents dataset

by Nikhil

Data source : 
1. US-Accidents Data : https://www.kaggle.com/sobhanmoosavi/us-accidents
2. US-Census (2020) Data: https://www.kaggle.com/darinhawley/us-2021-census-cities-populations-coordinates

Data structure: The US_Accident csv file include 1.5 M rows and 47 coloumns.

" 60+ Insights were found from the dataset. " The data analysis part is done in Google colab platform.
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

### Citation
- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. “A Countrywide Traffic Accident Dataset.”, arXiv preprint arXiv:1906.05409 (2019).
- Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. “Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights.” In proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, ACM, 2019.
