# Evaluation report of Group 6

Try out the online prototype. From the presentation video, get more information on the target group etc.

Use the Cognitive Walkthrough method to walk yourself through the visualization from the perspective of a person from the target group using this visualization. Write a short story about how a person from the target group uses the visualization and what question he/she can answer with it. Does the person run into problems (e.g., reading the visualizations, using the interface etc.)?

## 2. Threats of Visualization Design

At the domain specification stage: 
* As an investor users probably will not be interested in correlation between hospital beds and stock market change during pandemic.
* The section "Recession shapes" might not be interesting for the most investors. 

Within the data and abstraction stage. Group 1 mentioned three levels of data: national, industry and companies. First section shows stock market changes by countries. However, the second section addresses not sectors by countries, authors allow users to compare industry sectors of the USA and of the whole Europe. They do not give data by sectors by countries in Europe/Asia.

In the encoding interaction technique design:
* Users always have to read the description in order to receive information on how they can interact with visualizations. 
* "Overview of Stock Markets Development Worldwide" (1) and "Overview of Corona Crash Worldwide" (2) are difficult to use. Current version means that the users have to scroll up and down, if they want to compare on map. 
* For (1) and (2) they used size to encode the level of drop/change rate, however, for (2) they also add opacity to encode level of drop rate.
* Visualizations from sections "Profit Gainers in 2020" (3) and "Profit Losers in 2020" (4) are difficult to compare. At first sight, companies from both (3) and (4) in 2019 and in 2020 have quite similar profit levels. User have to carefully read axes to see, that Group 1 used different scale for each of four visualisations in (3) and (4)

## 3. What possible improvements do you suggest as a result of the validation?

From a User experience perspective, it would be better to have numbers and headers as a text  for all visualizations, so that a user can copy them.

If I use this application to make a financial decision, I would like to access data or to have references to the data source.

It is not easy to find variables descriptions (for example, "change_rate"). There should probably be bold text and separate paragraphs.

"Overview of Stock Markets Development Worldwide" and "Overview of Corona Crash Worldwide" would be more useful if the user can compare them: either have in one map or two maps side by side. Probably it would be better to use only size of point to show the difference in drop/change rates, without changing the opacity.

Probably the number of visualizations could be reduced. For example, as a professional investor, I will not benefit from chats from section "Recession shapes".

Visualizations from sections "Profit Gainers in 2020" and "Profit Losers in 2020" are difficult to compare. It would most likely be more comfortable to grasp if there were data for years 2019 and 2020 in the same chart. Also, it would be nice to have separate data about "Profit Gainers in 2020" and "Profit Losers in 2020" in the same chart (probably with a logarithmic scale). It also reduces the numbers of visualization from 4 to 3. 

