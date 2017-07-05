# NYC MTA Subway System Network and the L-Train Closure

### Fernando Melchor

##### Abstract—
Modelling systems as networks provides valuable insights. Calculating different measurements of connectivity, efficiency and capacity can help us to answer complicated questions. In this project, I explore the NYC Subway System Network and the impact of the L-Train partial closure. I propose a simulation that can help people understand the impact on the user experience depending on the origin and destination of the trip. 

#### Introduction

This report intends to provide a consolidated and comprehensive evaluation of the L-Train closure impact, scheduled for April 2019 with an estimated duration of 15 Months. The information presented here can help to program the number of buses and the needed contingency routes, the selection of them should also depend on the availability of space in the streets and the traffic congestion. The expected load increase in the other subway lines can be estimated with the information presented here. 
While most of the times, the impact and contingency actions are measured by the distribution of commuters loads to the different transportation systems, this approach tends to leave the population uniformed of what would be the actual impact in their daily life. Contingency actions need to be measured not only by loads of passengers but as well on the percentage commute time increase. The population needs to be able to estimate what the time increase to their daily commutes will be, and how and to what extent the contingency actions are mitigating this effect.
The simulation presented here is limited but it is a good base to start developing a more robust system. Further work should include the other transportation system (bus and ferry) and the street network, adding estimated travel time, and transfer time between different subway lines and to other transportation modes.
The approach and methodology presented here can be used to understand other kind of problems, for example: emergency evacuation or big scale event planning.


Through the development of this report different sources of data were used to provide insight on the situation and the potentially affected population of New York City. The information presented here can help to develop a contingency plan and evaluate it. All the data used is publicly available. This report includes the following analysis and information:
1.	Definition of the affected area.
2.	Characterization of the affected area.
3.	L-Train stations usage.
4.	Number of residents of the affected area in Brooklyn and Queens with jobs in Manhattan.
5.	Number of jobs in Manhattan occupied by residents of the affected area.
6.	Number of businesses in the affected area.
7.	Subway system connectivity change.
8.	Simulation, as a tool to evaluate the contingency actions. 


#### Data & Methods

##### Data
•	American Community Survey 2015: Median Age, Median Household Income, Percentage of White Population and Total Population, this survey was used and represented at the census tract level. (Census Bureau, 2017)
•	American Community Survey LODES 2014 LEHD Origin-Destination Employment Statistics. This information is available at the census block level and was aggregated at the census tract level. (Census Bureau, 2017)
•	Census Bureau. NYC Census tracts shapefiles.
•	NYC Open Data. Subway line and Subway stations data (NYC Open Data, 2017) (NYC Open Data, 2017)
•	Yelp Fusion API. Used to get the businesses in the affected area. (Yelp, 2017)
•	Mapzen Isochrone API. Used to calculate walking distances polygons. (Mapzen, 2017)
•	MTA Statistics. Average week-day usage of L-train stations (MTA, Average Weekday Ridership, 2017) 
•	MTA Subway Lines Information. Line Operation Booklet (MTA, Subway Lines Information, 2017)

##### Methodology
The first step in the methodology was the definition of the affected area and the characterization of it. This was done by selecting the areas around the L-Train stations within 15-minute walking distance. The census tracts intersecting with this area were used to characterize the residents. The whole extent of the L-Train Line was used for the definition of the area of interest considering that the overall connectivity and usefulness of the Line is affected by stopping the service from Bedford in Brooklyn to 8th Ave in Manhattan. The results can be consulted on Appendix Map 1.
The next step was understanding the usage of the L-Train. Statistics from MTA were used to compare each station, the result can be reviewed at the Appendix Map 2.
The Census Bureau Longitudinal Employer-Household Dynamics Survey from LODES was used to further the understanding of how people move through the city in this area. This survey connects residents and jobs location at the census block level, allowing us to understand the principal destinations of residents of the affected area. The results can be visualized as the number of residents with jobs in Manhattan (Appendix Map 3) and the number of jobs in Manhattan occupied by residents of the affected area (Appendix Map 4).
To understand the impact on businesses, data from Yelp was used. A list of the most affected neighborhoods is provided in the results (Table 3). When designing the contingency plan, it is necessary to provide options for these businesses to keep their demand unaffected. So far, there Is no clear approach to mitigate the effects on the economy of the area and uncertainty can potentially drive investments away. It is necessary to explore none-conventional approaches as a partnership with rideshare companies or shuttles to keep customers connected with these businesses. The result of the businesses density can be reviewed at the Appendix Map 5.
From the beginning, I wanted to understand the importance of the L-Train stations to the whole subway system. To do this I created a network representation of the subway system, based on the operation rules of the subway during weekday morning rush-hour. This network representation gives us to capability to measure the system the performance and efficiency. I provided the Average Shortest Path Length as the statistics to compare the connectivity of different areas of the city. In the Appendix Map 6  & 7 the change in connectivity can be appreciated, in addition an animated version of the change is available at the project link.
Finally, after doing this report, I realized that it was difficult to visualize and quantify the impact on people’s quality of life. So, I decided to use the networks previously developed to build a simulation tool that can explain in a more tangible way the effects on the commute of people. Ideally, the simulation would be able to quantify the percentage time increase for users, this early version only calculates the shortest route and compares the before and after closure of the L-Train stations. The simulation is available at the project link.


Normal Subway Network             |  L-Train Closure
:-------------------------:|:-------------------------:
<img src="/Data/2-0normal.gif" width="604">  |  <img src="/Data/2-0test.gif" width="604">
<img src="/Data/2-1normal.gif" width="604">  |  <img src="/Data/2-1test.gif" width="604">
<img src="/Data/2-2normal.gif" width="604">  |  <img src="/Data/2-2test.gif" width="604">
<img src="/Data/2-3normal.gif" width="604">  |  <img src="/Data/2-3test.gif" width="604">

#### Connectivity Change
<img src="/Data/connect.gif" width="808">