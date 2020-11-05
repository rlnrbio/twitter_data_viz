# **Corona & Twitter: A conversation-trend analysis** 

## Introduction
The Coronavirus pandemic has been the biggest story in the year 2020. It has been both a global news event, but at the same time impacted the lives of everybody
in a very personal way. There have been innumerable projects explaining many different aspects of the pandemic using interactive visualizations, usually focused on 
the progression of the virus showing cases and deaths or focusing on the economic impact of the pandemic. While these topics have been covered extensively, not so 
much focus has been put on analyzing the perception of and the communication about the first global virus pandemic in decades. The aim of this project is to understand
conversation trends about the virus over time with a main focus on twitter and giving insights into how such a massive story is being discussed on 
one of the most important social networks.

## Domain problem characterization:
There has been a lot of discussion about the relationship between twitter and reality. A lot of people have been asking the question, whether discussions on twitter
actually reflect discussions in the wider public. Some claim that twitter is a bubble, in someway distinct from the "real world". Our visualization takes a look at that
and therefore is therefore especially interesting for people, who spend a significant amount of their lifetime in social networks like twitter. However, as described before,
it does not cover the pandemic as such and so targets people, who have seen a lot of the visualizations of cases and deaths already and 
might be looking for some less depressing content. While most of the visualization are self-explanatory, some understanding of the functionality of twitter helps to fully grasp
the content of the plots. Therefore the target group would be people who are active in social networks, more or less informed about the pandemic and interested in a bigger
picture that might bust their filter bubble.

## The Data
Data acquisition initially has been a concern, since the twitter API does not allow for unrestricted access to a huge number of tweets. Other twitter datasets are provided by
commercial services which due to an unavailability of funds could not be used for this project. However, there were some datasets
that already existed and could be utilized for the project. The most abundant dataset of this kind has been created by Michael Kreil [[7]](#7). While he made the dataset available,
the size of several terabytes of data made the use of it unachievable for this project. For analysis in the future however, this dataset might 
provide a more in depth perspective. We also tried to acquire a dataset about the general mood in Germany curated by Zeit online [[8]](#8), but access was not provided.

Instead, the data used in our project comes from a student project at UC Davis, who have collected samples of Coronavirus related tweets from each day in the beginning of
the pandemic (20th of January to 8th of April) [[1]](#1). They also collected the daily trending topics [[2]](#2) and news stories about the coronavirus on Fox News and CNN [[3]](#3) [[4]](#4), 
which all have been used in these visualizations. Additionally they provided the total count of daily Coronavirus related tweets [[5]](#5).

As comparison, pandemic data from OurWorldInData was used [[6]](#6).


## From task to visual encoding

The sampled tweet dataset contains for most days about 13.5 thousand tweets. In the first visualization the number of daily tweets in the sampled dataset is shown in comparison to the total number
of coronavirus related tweets. Due to the big discrepancy the data is shown in logscale. Since some people have difficulties understanding logscale plots, an interactive tooltip 
allows the user to get the actual numbers for any specific day. The numbers were visualized using an areachart, since the area below the line represents the total number of tweets over
the whole time.
In the next two plots, the user can compare the progress of the pandemic with the number of total coronavirus tweets (left) and the number of news articles about the coronavirus. The number of
news articles was counted from the data provided in the UC Davis project. The user can interactively choose between different global pandemic indicators (new cases, new tests and new deaths) in the left
plot and between CNN articles and FOX news articles in the right plot. Because FOX news counts entries in livetickers as separate articles, the numbers there are much higher.

For the next three of plots a list of keywords has been defined and the number of times each keyword appears in the sampled twitter data per day was counted. Because the number of tweets remains rougly constant,
a normalization of the counts was not necessary. In the next three plots, the appearance of different keywords was shown over time. Since the aim is to explain, understand and compare trends over, here as well as for the 
plots before, linecharts have been used.
The plot "From local to global" shows the trends of keyword appearances that are related to the virus developing from a local outbreak to a global pandemic. 
For the plot "Preparation is key", keywords related to the very unusual situation of being locked down and preparing for it were selected. And for "fighting the virus", the keywords that resemble possible
mitigation strategies were shown. The tooltip allows the user to highlight a keyword by hovering over the line and also to get the exact number of appearances of a keyword in the sampled dataset
for a specific date.

In "steering the conversation", it is shown how one tweet by US President Donald Trump lead to a massive spike in appearances
of the term "chinese virus". For this visualization, the tweet is shown in the linechart visualizing the appearances without overlaying the data, additionally the date the tweet was posted is highlighted by a blue line.
The interactive tooltip allows the user to see the actual number of appearances of the keyword on specific days. The combined visualization with the tweet was chosen in
order to make the context of the visualization immediately clear.

The next two visualizations invite the user to further explore the data. Not every keyword chosen during preprocessing was included in one of the storytelling visualizations. Therefore, the visualization of the left lets the
user compare the appearances of a keyword over time with the pandemic data, but also the news publications and the total number of coronavirus tweets. The right plot lets the user directly compare
the appearances of two different keywords. The interactiveness with dropdown lists allows for the discovery of further possible connections between the twitter conversation and the pandemic.

The graph network visualization shows how often the keywords appear within the same tweet. The more often they appear together, the closer they are and the stronger the connection. 
Larger nodes indicate that the keywords appeared more often in the dataset overall. This analysis was done by counting the number of combined appearances for every combination of keywords. The graph was generated
using the Python package networkx, but visualized using the package netgraph, as this package also allows for interactive visualization. This interactive version based on the matplotlib
library is working, but could not yet be integrated in the prototype. In a later version, this visualization allows the user to drag and drop nodes and therefore to discover complex networks more easily. This
will be especially important when in future versions the user will be able to add additional keywords and the network will grow in size.

The last visualization shows the most used daily terms in a wordcloud. The shape of the twitter icon was chosen in order to visually encode the origin of the data. Therefore, the wordclouds could be easily understood
even outside the context of our prototype and be used for example as sharepics or as a preview image when the prototype is shared online. The visualization was created using the 
python library WordCloud. Individual visualizations were created for each day and then combined to a slideshow. Later versions should include a slider that lets the user chose the date more freely. The descision was made
against a small multiple visualization, as even if this would have allowed a better comparison between dates, the smaller words would not have been readible anymore. The size of the word corresponds to the number of appearances
in the sampled data, the words "Coronavirus", "Covid19" and "Covid2019" have been removed as they would have dominated the wordclouds (because the tweets are already filtered for these keywords). However, the words might still
appear in the clouds sometimes as for example the Spanish spelling with an í is not removed. 

Some improvements for the future were already mentioned, the most important would be to let the user add and search for its own keywords. That will not just add another layer of interactiveness and make the visualizations personalizable, 
but remove the restrictions posed by the preselection of keywords through the authors. This will add another layer of algorithmic complexity. Right now, all the preanalyzed data is stored in the site,
but no online anakysis takes place. That would change requiring increased Server capacity. In the case of huge popularity of the site in the future this might be a bottleneck. 

To explore the usability of the visualization prototype, watch this screencast: https://youtu.be/NLvXzepmJMs

The up and running prototype can be found here: https://nadja-mansurov.github.io/

## Data sources & References
<a id="1">[1]</a> 
Sampled twitter data
https://github.com/xxz-jessica/COVID-19_UCD_Challenge/tree/master/Tweet_Raw_Data/raw_data

<a id="2">[2]</a> 
Trending topics data
https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/Twitter_Trending_Topics/usa_trending.csv

<a id="3">[3]</a> 
News articles, CNN
https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/CNN_full.xlsx

<a id="4">[4]</a> 
News articles, FoxNews
https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/foxnews_article_form.xlsx

<a id="5">[5]</a>
Number of total daily Coronavirus tweets
https://raw.githubusercontent.com/xxz-jessica/COVID-19_UCD_Challenge/master/Tweet_Raw_Data/tweet_per_day_1

<a id="6">[6]</a>
Covid pandemic data
https://covid.ourworldindata.org/data/owid-covid-data.csv

<a id="7">[7]</a>
Size of total daily Coronavirus tweets
https://gist.github.com/MichaelKreil/95590d5cbcee1bce7cbd3c8bd660c5b6

<a id="8">[8]</a>
Zeit general mood data
https://www.zeit.de/gesellschaft/2017-03/stimmung-wie-geht-es-uns