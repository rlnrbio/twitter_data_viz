# **Corona & Twitter: A conversation-trend analysis** 

## Introduction
The main idea of this project is to explore *Coronavirus twitter trends*. 
During the last decade, twitter has emerged as the primary discussion platform online for everybody who is or believes to be important. Therefore, a colossal event like a global pandemic will not just be a major topic on twitter, but looking at how it is discussed there can be quite enlightening. For everybody, who is a bit tired of looking only at infection numbers all the time, we offer some alternative findings about the coronavirus pandemic.
For this, we have taken a total of about 1.1 million random English tweets between January and April that thematized corona and analyzed them.

## Domain problem characterization:
We are trying to tell stories about relationship between twitter and reality. As we know there are lots of “serious” visualizations about Covid19 already exists so we tried to do something entertaining yet informative.
Target Group of our project is general public who is keen in knowing the Coronavirus Twitter trends.
The COVID-19 pandemic has changed the world. We would like to see how has it changed our tweets?

(Describe the domain situation, i.e., what is the group of target users, their domain of interest, their questions, and their data.)

## Data / task abstraction: 

(Formulate the tasks in a domain-independent vocabulary. How did you prepare (aggregate, filter...) the data to support the tasks?)

## Visual encoding / interaction design: 
We have first used area chart to show the total number of tweets and the sampled tweets and then we used line charts to show the trends 

(Describe the visual encoding and why you decided for it. What interaction types did you use and why? (be precise and try to cover all details in this part))

## Algorithm design: 

(How did you make sure that the computational complexity of your solution is appropriate? What is the bottleneck with respect to performance?)


## Other libraries used and why 


## Improvements
- If we would have more time then we could have tried getting recent data by using some of the commercial services. 
- We could have some more improvements in our word cloud widget such as: 
     - allow user to select date in last widget 
     - format data to appropriate format (dependent on user locale, using moment.js)

## Data sources:
- Covid pandemic data: https://covid.ourworldindata.org/data/owid-covid-data.csv
- Trending topics data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/Twitter_Trending_Topics/usa_trending.csv
- Sampled twitter data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/tree/master/Tweet_Raw_Data/raw_data
- News articles data, CNN data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/CNN_full.xlsx
- News articles data, FOX data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/foxnews_article_form.xlsx
- Number of total Coronavirus tweets: https://raw.githubusercontent.com/xxz-jessica/COVID-19_UCD_Challenge/master/Tweet_Raw_Data/tweet_per_day_1
