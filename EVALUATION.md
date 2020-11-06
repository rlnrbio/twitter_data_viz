# Evaluation report of Group 6

## 1. Cognitive Walkthrough

The target group of this application is the people who want to invest in the stock market. This application tries to help investors to recognize companies in different countries in which one can invest amidst these corona times. As a user by looking at this application we could understand and gain an overall idea of how the global stock market looks like.

Using the current application we can detect countries where the market dropped at most with the help of the first visualization “Overview of Stock Markets Development Worldwide”. It was easy to follow along with the conclusion but ran into problems while reading the legend ‘change_rate_nom’ because it was not described first. With ‘maximum drop rate and final change rate’ bar chart visualization we could understand and answer the question as to how the countries are affected and how slow or fast they recover from this pandemic attack. However, the terms `drop rate` and `change rates` were still not very clear. 

The next interactive visualization (rate change in continents and countries) was easy to navigate through the bar chart but it would be better to be able to select the countries through the line chart. The choice of tooltip was not helping instead overlapping in the line chart. Using line charts we can get an overall idea of the change rates in continents and countries but we feel the information was quite redundant. Also, we find it difficult to select the country in the second bar chart because of the chosen resolution.

Then the application tries to explain the market performances based on three aspects i.e. `National level, Industry level and Company level`. From the visualization ‘COVID-19 factors V.S. stock market change rate of countries’ under national level, we are able to answer what are some of the factors influencing countries’ stock market during this pandemic. With the provided interactivity we could easily see the correlation of these factors with different countries and that provides an overall idea about which of the factors are highly correlated with stock market change of the country. The conclusion was easy to follow as well.

Moving forward authors tried to find out the right sector to invest under industry level in which they mainly compared some sectors in the US and in the whole Europe. They tried to explain that why they chose the US and the whole Europe for comparison, but the answer was not quite satisfying because we felt the comparison was quite abstract. Nevertheless we got to know that the IT sector is doing good as compared to other sectors and can be a good sector to invest in.

Lastly, under company level, authors chose the 4 key company factors which affects the company’s stock price and tried to show the correlation between these factors and the company's stock price change rate which was nicely done and easily understandable with the help of interactivity provided on the scatter plots but how they chose these factors was not clear with the given explanation and the visualization. With the help of their conclusion and the scatter plots we could see that the percentage of profitable and non-profitable companies is 50% in the US whereas it is not true for China. Overall authors concluded the application with some investment advices which was intelligible, but the concluding bar charts showing profits gainers and losers in 2020 are difficult to compare. Ultimatley as a user, we did learn about the stock market and how bad it is affected by the COVID-19. Also which country and sector can be a good choice for the investment.

## 2. Threats of Visualization Design

At the domain specification stage: 
* As an investor users probably will not be interested in correlation between hospital beds and stock market change during pandemic.
* The section "Recession shapes" might not be interesting for the most investors. 

Within the data and abstraction stage, Group 1 mentioned three levels of data: `national, industry and companies`. First section shows stock market changes by countries. However, the second section addresses not sectors by countries, authors allow users to compare industry sectors of the USA and of the whole Europe. They do not give data by sectors by countries in Europe/Asia.

In the encoding interaction technique design:
* Users always have to read the description in order to receive information on how they can interact with visualizations. 
* "Overview of Stock Markets Development Worldwide" (1) and "Overview of Corona Crash Worldwide" (2) are difficult to use. Current version means that the users have to scroll up and down, if they want to compare on map. 
* For (1) and (2) they used size to encode the level of drop/change rate, however, for (2) they also add opacity to encode level of drop rate.
* Visualizations from sections "Profit Gainers in 2020" (3) and "Profit Losers in 2020" (4) are difficult to compare. At first sight, companies from both (3) and (4) in 2019 and in 2020 have quite similar profit levels. User have to carefully read axes to see, that Group 1 used different scale for each of four visualisations in (3) and (4)

## 3. What possible improvements do you suggest as a result of the validation?

From a user experience perspective, it would be better to have numbers and headers as a text for all the visualizations, so that a user can copy them.

If I use this application to make a financial decision, I would like to access data or to have references to the data source.

It is not easy to find variables descriptions (for example, "change_rate"). There should probably be bold text and separate paragraphs.

"Overview of Stock Markets Development Worldwide" and "Overview of Corona Crash Worldwide" would be more useful if the user can compare them: either have one map or two maps side by side. Probably it would be better to use only the size of the point to show the difference in drop/change rates, without changing the opacity.

Probably the number of visualizations could be reduced. For example, as a professional investor, I will not benefit from chats from section "Recession shapes".

Visualizations from sections "Profit Gainers in 2020" and "Profit Losers in 2020" are difficult to compare. It would most likely be more comfortable to grasp if there were data for years 2019 and 2020 in the same chart. Also, it would be nice to have separate data about "Profit Gainers in 2020" and "Profit Losers in 2020" in the same chart (probably with a logarithmic scale). It also reduces the numbers of visualization from 4 to 3. 

