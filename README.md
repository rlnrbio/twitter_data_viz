# **Corona & Twitter: A conversation-trend analysis** 

## Introduction
The Coronavirus pandemic has been the biggest story in the year 2020. It has been both a global news event, but at the same time impacted the lives of everybody
in a very personal way. There have been innumerable projects explaining many different aspects of the pandemic using interactive visualizations, usually focused on 
the progression of the virus showing cases and deaths or focusing on the economic impact of the pandemic. While these topics have been covered extensively, not so 
much focus has been put on analyzing the perception of and the communication about the first global virus pandemic in decades. The aim of this project is to understand
conversation trends about the virus over time with a main focus on twitter and therefore gives insights into how such a massive story is being discussed on 
one of the most important social networks.

## Domain problem characterization:
There has been a lot of discussion about the relationship between twitter and reality. A lot of people have been asking the question, whether discussions on twitter
actually reflect discussions in the wider public. Some claim that twitter is a bubble, in someway distinct from the "real world". Our visualization takes a look at that
fact and therefore might be especially interesting for people, who spend a significant amount of their lifetime in social networks like twitter. However, as described before,
it does not cover the pandemic as such and therefore is of interest especially to those people, who have seen a lot of the visualizations of cases and deaths already and 
might be looking for some less depressing content. While most of the visualization are self-explanatory, some understanding of the functionality of twitter helps to fully grasp
the content of the plots. Therefore the target group would be people who are active in social networks, more or less informed about the pandemic and interested in a bigger
picture that might bust their filter bubble.

## Data / task abstraction: 
Data acquisition initially has been a problem, since the twitter API does not allow for unrestricted access to a huge number of tweets. Other twitter datasets are provided by
commercial services which due to an unavailability of funds could not be used for this project. However, there were some datasets
that already existed and were of particular interest for us. The most abundant dataset of this kind has been created by Michael Kreil {source}. While we would have gotten
access to this dataset, the size of several terrabytes of data made the use of it unrealistic for this project. For further analysis in the future however, this dataset might 
provide a more in depth perspective. We also tried to acquire a dataset about the general mood in Germany curated by Zeit online {source}, but we were not given access to this data.

Instead, the data used in our project comes from another student project at UC Davis, who have collected samples of Coronavirus related tweets from each day in the beginning of
the pandemic. They also collected data about the trending topics {source} and news stories about the coronavirus on Fox News and CNN {source}, which we have also used in our visualizations.
They also provided the total number of Coronavirus related tweets per day.

The sampled tweet dataset contains for most days about 13.5 thousand tweets.
TBC


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
