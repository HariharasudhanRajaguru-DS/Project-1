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
   

### Data Wrangling
>In the data set, there are several different cases where the booster did not land successfully. Sometimes a landing was attempted but failed due to an accident; for example, True Ocean means the mission outcome was successfully landed to a specific region of the ocean while False Ocean means the mission outcome was unsuccessfully landed to a specific region of the ocean. True RTLS means the mission outcome was successfully landed to a ground pad False RTLS means the mission outcome was  unsuccessfully landed to a ground pad. True ASDS means the mission outcome was successfully landed on a drone ship False ASDS means the mission outcome was unsuccessfully landed on a drone ship. We mainly convert those outcomes into Training Labels with 1 means the booster successfully landed 0 means it was unsuccessful.

### Calculating the number of launches from each site
>LEO: Low Earth orbit (LEO)is an Earth-centred orbit with an altitude of 2,000 km (1,200 mi) or less (approximately one-third of the radius of Earth),[1] or with at least 11.25 periods per day (an orbital period of 128 minutes or less) and an eccentricity less than 0.25.[2] Most of the manmade objects in outer space are in LEO.
VLEO: Very Low Earth Orbits (VLEO) can be defined as the orbits with a mean altitude below 450 km. Operating in these orbits can provide a number of benefits to Earth observation spacecraft as the spacecraft operates closer to the observation.
GTO A geosynchronous orbit is a high Earth orbit that allows satellites to match Earth's rotation. Located at 22,236 miles (35,786 kilometers) above Earth's equator, this position is a valuable spot for monitoring weather, communications and surveillance. Because the satellite orbits at the same speed that the Earth is turning, the satellite seems to stay in place over a single longitude, though it may drift north to south,” NASA wrote on its Earth Observatory website.
SSO (or SO): It is a Sun-synchronous orbit also called a heliosynchronous orbit is a nearly polar orbit around a planet, in which the satellite passes over any given point of the planet's surface at the same local mean solar time.
ES-L1 :At the Lagrange points the gravitational forces of the two large bodies cancel out in such a way that a small object placed in orbit there is in equilibrium relative to the center of mass of the large bodies. L1 is one such point between the sun and the earth.
HEO: A highly elliptical orbit, is an elliptic orbit with high eccentricity, usually referring to one around Earth.
ISS A modular space station (habitable artificial satellite) in low Earth orbit. It is a multinational collaborative project between five participating space agencies: NASA (United States), Roscosmos (Russia), JAXA (Japan), ESA (Europe), and CSA (Canada).
MEO Geocentric orbits ranging in altitude from 2,000 km (1,200 mi) to just below geosynchronous orbit at 35,786 kilometers (22,236 mi). Also known as an intermediate circular orbit. These are "most commonly at 20,200 kilometers (12,600 mi), or 20,650 kilometers (12,830 mi), with an orbital period of 12 hours
HEO Geocentric orbits above the altitude of geosynchronous orbit (35,786 km or 22,236 mi) \[9]
GEO It is a circular geosynchronous orbit 35,786 kilometres (22,236 miles) above Earth's equator and following the direction of Earth's rotation
PO It is one type of satellites in which a satellite passes above or nearly above both poles of the body being orbited (usually a planet such as the Earth

![](https://github.com/HariharasudhanRajaguru-DS/Hariharasudhan-Rajaguru/blob/main/images/Orbit_image.png)
### [Performing data wrangling](https://github.com/HariharasudhanRajaguru-DS/IBM_Data-Science-/blob/main/Capstone_project-week1_Data%20Wrangling.ipynb)
For Machine learning used one hot encoding and dropped irrelevant columns 



### Perform exploratory data analysis (EDA) using visualization and SQL
Plotting Scatter plots, Cat plots and Bar graphs to understand the relationships between the independent and the dependent variables
Performing interactive visual analytics using Folium and Plotly Dash to find the successful landing sites and the key factors
Perform predictive analysis using classification models
How to build, tune, evaluate classification models



