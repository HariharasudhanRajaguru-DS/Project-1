## Data Scientist Portfolio

### Sample Project 1: Space X Falcon 9 First Stage Landing Prediction

We predicted the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars.

Other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. 

Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

### Questions:

1. What are the factors playing major role to safely launch the first stage successfully?

2. Finding relationships with each variable for a successful landing?

3. What are the variable measures has to taken for a successful landing?

### Data collection

Data collection methodology:
1. SpaceX rest API
2. Web scrapping from Wikipedia(https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922) 

Here I have collected data from the rest API as well as from the Wikipedia website.

### Data Wrangling
In the data set, there are several different cases where the booster did not land successfully. Sometimes a landing was attempted but failed due to an accident; for example, True Ocean means the mission outcome was successfully landed to a specific region of the ocean while False Ocean means the mission outcome was unsuccessfully landed to a specific region of the ocean. True RTLS means the mission outcome was successfully landed to a ground pad False RTLS means the mission outcome was  unsuccessfully landed to a ground pad. True ASDS means the mission outcome was successfully landed on a drone ship False ASDS means the mission outcome was unsuccessfully landed on a drone ship. We mainly convert those outcomes into Training Labels with 1 means the booster successfully landed 0 means it was unsuccessful.

### Performing data wrangling
For Machine learning used one hot encoding and dropped irrelevant columns 

### Perform exploratory data analysis (EDA) using visualization and SQL
Plotting Scatter plots, Cat plots and Bar graphs to understand the relationships between the independent and the dependent variables
Performing interactive visual analytics using Folium and Plotly Dash to find the successful landing sites and the key factors
Perform predictive analysis using classification models
How to build, tune, evaluate classification models



