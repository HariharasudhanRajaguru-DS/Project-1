### [Project 1: Space X Falcon 9 First Stage Landing Prediction](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-)
We predicted the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars.
Other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. 
Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

### Questions:

1. What are the factors playing major role to safely launch the first stage successfully?

2. Finding relationships with each variable for a successful landing?

3. What are the variable measures has to taken for a successful landing?

### Data collection

For data collection two methodologies has been used. Data collected from Space X REST API as well as from Wikipedia website.

1.[SpaceX REST API Data Collection](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/jupyter-labs-spacex-data-collection-api.ipynb)

   I collected the data in JSON file format with the help of libraries Pandas and Requests. We can nomalize(pd.json_normalize()) the data.
   
   [REST API web page](https://api.spacexdata.com/v4/rockets/)
   
2.[Web scrapping from Wikipedia](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/CapstoneProject_Web%20Scraping%20(1).ipynb)

   Data was collected from wikipedia website using requests library then used BeautifulSoup(bs4) Parsed html and found the data table for further analysis.
   
   [Wikipedia web page](https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922)

I selected Space X Falcon 9 launch records only.

### [Data Wrangling](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/Capstone_project-week1_Data%20Wrangling.ipynb)

The Pandas dataframe columns are FlightNumber, Date,BoosterVersion, PayloadMass, Orbit, LaunchSite, Outcome, Flights, GridFins, Reused, Legs, LandingPad, Block, ReusedCount, Serial, Longitude, Latitude.

I have calculated no of launches in each launch sites, no of occurences to each orbit, launch outcome to each orbit type and created a landing outcome calculated the success rate. 

For Machine learning used one hot encoding and dropped irrelevant columns.

### [Perform exploratory data analysis (EDA) using visualization and SQL](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/Capstone_project-week2-DataAnalysis_EDA_matplotlib.ipynb)

Plotting Scatter plots, Cat plots and Bar graphs to understand the relationships between the independent and the dependent variables

Analyzing the connection between FlightNumber vs LaunchSite


![](./images/FlightNumber%20vs%20LaunchSite.png)

From the above scatter plot we can clearly find CCAFS SLC 40 launching site has the highest no of launches, and	followed by KSC LC 39A, and followed by VAFBSLC	4E .

![](./images/Payload%20and%20Launch%20Site.png)

From the above plot, we can find that CCAFS SLC 40 launching site has the flight’s payload mass has the highest of 15000.

![](./images/Payload%20and%20Orbit%20type.png)

As you see that in the LEO orbit the Success appears related to the number of flights; on the other hand, there seems to be no relationship between flight numbers when in GTO orbit.

![](./images/launch%20success%20yearly%20trend.png)

We can observe that the success rate since 2013 kept increasing till 2020.


![](./images/success%20rate%20of%20each%20orbit%20type.png)

From the bar chart, we can find orbits GEO, HEO, SSO, ES-L1 has the Best Success Rate.


### [Performing interactive visual analytics using Folium](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/CapstoneProject_week3-FoliumMap.ipynb)

1.launch sites are in close proximity to equator to minimize fuel consumption by using Earth's ~ 30km/sec eastward spin to help spaceships get into orbit.

2.Launch sites are in close proximity to coastline so they can fly over the ocean during launch, for at least two safety reasons-- 

 (a) crew has option to abort launch and attempt water landing 
   
 (b) minimize people and property at risk from falling debris. 
   
3.Launch sites are in close proximity to highways, which allows for easily transport required people and property. 

4.Launch sites are in close proximity to railways, which allows transport for heavy cargo. 

5.Launch sites are not in close proximity to cities, which minimizes danger to population dense areas.

### Plotly Dash findings 
![](./images/Pie%20chart.png)

By this pie chart, we can jump to the conclusion of KSC LC-39A has the highest success rate compared to other launch sites. 

Different types of booster versions has been launched from this site.

But the payload never exceeded 10000 kg.

The small payload flights have the most successful launch rate than the high payload flights.


### Perform predictive analysis using classification models
How to build, tune, evaluate classification models



