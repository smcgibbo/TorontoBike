# TorontoBike
Toronto Bikeshare is a system of bikes available to rent 24/7 at 30 docking sttions across the Greater Toronto Area. Ridership data is publically available via Open Data TO and can be found here: [Toronto Bike Share data](https://open.toronto.ca/dataset/bike-share-toronto/). I chose to explore the 2021 data to better understand usage of these bikes and factors affecting ridership.

## Bike Usage over time
To get a sense of the way the bikes are used, I first looked at when, and for how long people used the bikeshare. I found that most trips lasted less than one half hour (which is the maximum length of a less expensive "short trip"), and peak utilization occures between May and September 5pm - 6pm.
### Trip duration after removing trips shotrer than 2 minutes and longer than 6 hours.
![Trip Duration](https://user-images.githubusercontent.com/14931592/203406566-d6491bd7-fea0-4f97-b1ac-e0d8aef8e523.png)
### Heatap of usage of bikes over the day and month of the year.
![Bikeshare_utilization_heatmap](https://user-images.githubusercontent.com/14931592/203406654-9ef89e3b-4e52-43e7-9d58-876de6ae2aac.png)
The most popular start and stop location in the city is York st. and Queen's Quay, located along a popular bike path followingthe lakefront. Of the top 50 most used start and stop locations, 50% are located along the Line 2 subway route, indicating that commuters are using the bike share system in combination with TTC trips to get to and from their destinations. This may also be an effect of the introduction of hte bikelanes on Bloore street, making the area more safe for bike usage. The follow map shows all bike dock locations, with larger sizes corresonding to docks with higher capacity.

![image](https://user-images.githubusercontent.com/14931592/203407773-406aceba-f30f-4114-b106-c2e9480c21ef.png)

Because the start and stop locations needed by users do not perfectly balance, redistribution of the bikes must be done to leave bikes available at docks where people may want to start their trips, and docks empty at locations riders may want to end their trips. This process is called rebalancing and unfortunately this data is not included publically. To get a sense of hte need for rebalancing, I looked at the average flux of each station over the year. This analysis does not include and estimate of the docks being full or empty, and this information is not included in the data.

![flux_bikes](https://user-images.githubusercontent.com/14931592/203408785-f77def34-d461-45f7-9638-bcd93a2054f4.png)

We can see that over 50% of the bike docks have a net flux of usage close to zero. There are however about 15% of docks having either a large outflow (more bikes leaving than being dropped off) or large inflow (more bikes arriving than being picked up). The usage can be sustained by having enough docks and bikes to maintain demand until rebalancing has occured. I will be looking at te availability of data to test rebalancing optimization and estimate revennue loss due to unavailability of bikes and/or empty docks.
## Packages used -- note that if you use anaconda to install, use forge channel or you will need to re-install shapely. It will lead to import issues.
Geopandas https://geopandas.org/en/stable/
