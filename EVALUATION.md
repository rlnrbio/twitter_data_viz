# Evaluation report of Group 6

Try out the online prototype. From the presentation video, get more information on the target group etc.

Use the Cognitive Walkthrough method to walk yourself through the visualization from the perspective of a person from the target group using this visualization. Write a short story about how a person from the target group uses the visualization and what question he/she can answer with it. Does the person run into problems (e.g., reading the visualizations, using the interface etc.)?

## 2. Formal validation

### Domain Problem and Data Characterization

The target groups for this application are stock market investors and people interested in the economy. Group 1 is trying to identify how to invest during the epidemic. This visualization shows countries and sectors that cut and growth in 2020.  Also, the authors highlight the most and least profitable companies. 

Domain-specific terminology and concepts are used in this application, for example, "recession," "equity market collapse," and "market indices".
Specific questions from the target are: 

1. Where should I invest as a high-risk-high-reward investor?
2. Where should I invest if I want to have the lowest risk? 
3. Should I invest in this particular country (country funds), sector (ETF), or company?

### Operation and Data Type Abstraction

Group 1 used three levels of data abstraction. The first level is changes in stock markets on the national level because of the epidemic, the next is changes by sectors, and the last was companies. They used numerical data.

Generic operations to answer all three questions are high-level tasks. They aim to identify general trends of companies, sectors and countries' development. 

### Visual Encoding and Interaction Design

Group 1 used different tools to visualize data: maps, line charts, bar charts, scatter plots. 

They interact with users through tooltips for most of them, but there is also interaction by clicking (Question 1, section "Answer") and zoom in/out for some ("Company Factors V.S. Stock change rate", "COVID-19 factors V.S. stock market change rate"). Users always have to read the description in order to receive information on how they can interact with visualizations. 

They mostly used color to encode country name. In the section "Global Level" they used color to encode drop/change rate. For visualisations "Overview of Stock Markets Development Worldwide" and "Overview of Corona Crash Worldwide" they also used size to encode the level of drop/change rate. For the "Overview of Corona Crash Worldwide" they also add opacity to encode level of drop rate.

## 3. What possible improvements do you suggest as a result of the validation?

From a User experience perspective, it would be better to have numbers and headers as a text  for all visualizations, so that a user can copy them.

If I use this application to make a financial decision, I would like to access data or to have references to the data source.

It is not easy to find variables descriptions (for example, "change_rate"). There should probably be bold text and separate paragraphs.

"Overview of Stock Markets Development Worldwide" and "Overview of Corona Crash Worldwide" would be more useful if the user can compare them: either have in one map or two maps side by side. The current version means that the user has to scroll up and down. Probably it would be better to use only size of point to show the difference in drop/chahge rates, without changing the opacity.

Probably the number of visualizations could be reduced. For example, as a professional investor, I will not benefit from chats from section "Recession shapes".

Visualizations from sections "Profit Gainers in 2020" and "Profit Losers in 2020" are difficult to compare. It would most likely be more comfortable to grasp if there were data for years 2019 and 2020 in the same chart. Also, it would be nice to have separate data about "Profit Gainers in 2020" and "Profit Losers in 2020" in the same chart (probably with a logarithmic scale). It also reduces the numbers of visualization from 4 to 3. 



