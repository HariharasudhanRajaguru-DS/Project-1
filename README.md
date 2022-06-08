## Data Scientist Portfolio

### Sample Project 1: Space X Falcon 9 First Stage Landing Prediction
>We predicted the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars.
Other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. 
Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

### Questions:

1. What are the factors playing major role to safely launch the first stage successfully?

2. Finding relationships with each variable for a successful landing?

3. What are the variable measures has to taken for a successful landing?

### Data collection

Data collection methodology:

1.[SpaceX rest API](https://api.spacexdata.com/v4/rockets/)

   I collected the data in JSON file format with the help of libraries Pandas and Requests. We can nomalize(pd.json_normalize()) the data.
   
   [Data collection - API Jupyter Notebook](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/jupyter-labs-spacex-data-collection-api.ipynb)
   
2.[Web scrapping from Wikipedia](https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922)

   I have collected the data from wikipedia website then used BeautifulSoup(bs4) Parsed html and found the data table for the project.
   
   [Data collection - Web scrapping Jupyter Notebook](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/CapstoneProject_Web%20Scraping%20(1).ipynb)

>I selected Space X Falcon 9 launch records only.

### Data Wrangling

The Pandas dataframe columns are FlightNumber, Date,BoosterVersion, PayloadMass, Orbit, LaunchSite, Outcome, Flights, GridFins, Reused, Legs, LandingPad, Block, ReusedCount, Serial, Longitude, Latitude

I have calculated no of launches in each launch sites, no of occurences to each orbit, launch outcome to each orbit type and created a landing outcome calculated the success rate. 

[Performing data wrangling -Jupyter Notebook](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/Capstone_project-week1_Data%20Wrangling.ipynb)

For Machine learning used one hot encoding and dropped irrelevant columns 

### Perform exploratory data analysis (EDA) using visualization and SQL

Plotting Scatter plots, Cat plots and Bar graphs to understand the relationships between the independent and the dependent variables

Analyzing the connection between FlightNumber vs LaunchSite


![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/LaunchSite%20vs%20FlightNumber.jpg)



![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/FlightNumber%20vs.%20PayloadMass.png)




![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/FlightNumber%20and%20Orbit%20type.png)




![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/Payload%20and%20Launch%20Site.png)




![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/Payload%20and%20Orbit%20type.png)




![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/launch%20success%20yearly%20trend.png)





![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/success%20rate%20of%20each%20orbit%20type.png)





[Exploratory Data Analysis - Jupyter Notebook](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/Capstone_project-week2-DataAnalysis_EDA_matplotlib.ipynb)

### Performing interactive visual analytics using Folium and Plotly Dash to find the successful landing sites and the key factors
###Perform predictive analysis using classification models
How to build, tune, evaluate classification models



