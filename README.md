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

## From task to visual encoding (combined b-d)

## Data / task abstraction: 
Data acquisition initially has been a problem, since the twitter API does not allow for unrestricted access to a huge number of tweets. Other twitter datasets are provided by
commercial services which due to an unavailability of funds could not be used for this project. However, there were some datasets
that already existed and were of particular interest for us. The most abundant dataset of this kind has been created by Michael Kreil {source}. While we would have gotten
access to this dataset, the size of several terrabytes of data made the use of it unrealistic for this project. For further analysis in the future however, this dataset might 
provide a more in depth perspective. We also tried to acquire a dataset about the general mood in Germany curated by Zeit online {source}, but we were not given access to this data.

Instead, the data used in our project comes from another student project at UC Davis, who have collected samples of Coronavirus related tweets from each day in the beginning of
the pandemic (20th of January to 8th of April). They also collected data about the trending topics {source} and news stories about the coronavirus on Fox News and CNN {source}, which we have also used in our visualizations.
They also provided the total number of Coronavirus related tweets per day.

The sampled tweet dataset contains for most days about 13.5 thousand tweets. In the first visualization the number of daily tweet in our dataset is shown alongside the total number
of coronavirus related tweets on twitter. Due to the big difference the data is shown in logscale. Since some people have problems understanding logscale plots, an interactive tooltip 
allows the user to get the actual numbers for any specific day. The numbers were visualized using an areachart, since the area below the line represents the total number of tweets over
the whole time.
In the next plots, the user can compare the progress of the pandemic with the number of total coronavirus tweets (left) and the number of news articles about the coronavirus. The number of
news articles was counted from the data provided in the UC Davis project. The user can choose between different pandemic indicators (new cases, new tests and new deaths). These are the 
numbers for the entire world extracted from the OurWorldInData Covid19 Dataset (source). The user can also choose between CNN articles and FOX news articles. Because FOX news counts entries 
in livetickers as separate articles, the numbers there are much higher.
For the next number of plots a list of keywords has been defined and the number of sampled tweets each keyword appears in per day was counted. Because the number of tweets remains rougly constant,
a normalization of the counts was not necessary. In the next three plots, the appearance of different keywords was shown over time. Since the aim is to explain trends, here as well as for the 
plots before, linecharts have been used. They are one of the simplest ways to understand change over time. 
The plot "From local to global" shows the trends of keyword appearances that are related to the virus developing from a local outbreak to a global pandemic. 
For the plot "Preparation is key", keywords related to the very unusual situation of being locked down and preparing for it were selected. And for "fighting the virus", the keywords that resemble possible
mitigation strategies were shown. The tooltip allows the user to highlight a keyword by hovering over the line and also to get the exact number of appearances of a keyword in the sampled dataset
for a specific date.
Another option of doing that is done by showing how one tweet by US President Donald Trump lead to a massive spike in appearances
of the keyword "chinese virus". For this visualization, the tweet is shown right next to the line visualizing the appearances, additionally the date the tweet was posted is highlighted by a blue line.
The tooltip allows the user to see the actual number of appearances of the keyword but also to identify values for specific days. The combined visualization with the tweet was chosen in
order to make the context of the visualization immediately clear. 
The next two visualizations invite the user to further explore the data. Not every keyword chosen was included in one of the viusalizations before, the visualization of the left lets the
user compare the appearances of a keyword over time with the pandemic data, but also the news publications and the total number of coronavirus tweets. The right plot lets the user directly compare
the appearances of two different keywords. The interactiveness with dropdown lists allows for the discovery of further possible connections between the twitter conversation and the pandemic than the one shown
previously.
The next visualization shows a graph network depicting how often the keywords appear together in tweets. The more often they appear together, the closer they are and the stronger the connection. 
Larger nodes indicate that the keyword appeared more often in the dataset overall. This analysis was done by counting the number of combined appearances for every combination of keywords. The graph was generated
using the Python package networkx, but visualized using the package netgraph, as this package also allows for a interactive visualization. This interactive version based on the interactive matplotlib
plot function is working, but could not yet be integrated in the prototype. In a later version, this visualization allows the user to drag and drop nodes and therefore to discover complex networks more easily. This
will be especially important if in future versions the user can add additional keywords and the network will grow in size.
The last visualization shows the most used daily terms in a wordcloud. The shape of the twitter icon was chosen in order to visually encode the origin of the data. Therefore, the wordclouds could be easily understood
even outside the context of our prototype. Therefore, they could be used for example as sharepics or as a preview image when the prototype is shared for example on twitter. The visualization was created using the 
python library WordCloud. Individual visualizations were created for each day and then combined to a slideshow. Later versions should include a slider that lets the user chose the date more freely. The descision was made
against a small multiple visualization, as even if this would have allowed a better comparison between dates, the smaller words would not have been readible anymore. The size of the word corresponds to the number of appearances
of the word, the words "Coronavirus", "Covid19" and "Covid2019" have been removed as they would have dominated the wordclouds (because the tweets are already filtered for these keywords). However, the words might still
appear in the clouds sometimes as for example the Spanish spelling with an í is not removed. 
Some improvements for the future were already mentioned, the most important would be to let the user add and search for its own keywords. That will not just add another layer of interactiveness to the site, but also lets
the user explore twitter using words that the authors did not think of, therefore making the visualizations personalizable. This will add another layer of algorithmic complexity. Right now, all the preanalyzed data is stored in the site,
but no life analysis is going on. That would change requiring increased Server capacity. In the case of huge popularity of the site in the future this might be a bottleneck. 

To explore the usability of the visualization prototype, watch this screencast:
<iframe width="560" height="315" src="https://www.youtube.com/embed/NLvXzepmJMs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Data sources:
- Covid pandemic data: https://covid.ourworldindata.org/data/owid-covid-data.csv
- Trending topics data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/Twitter_Trending_Topics/usa_trending.csv
- Sampled twitter data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/tree/master/Tweet_Raw_Data/raw_data
- News articles data, CNN data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/CNN_full.xlsx
- News articles data, FOX data: https://github.com/xxz-jessica/COVID-19_UCD_Challenge/blob/master/News_Fox_CNN/foxnews_article_form.xlsx
- Number of total Coronavirus tweets: https://raw.githubusercontent.com/xxz-jessica/COVID-19_UCD_Challenge/master/Tweet_Raw_Data/tweet_per_day_1
