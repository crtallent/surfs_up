# Surfs_Up

## Overview of Surfs_Up Analysis
In this project, we are exploring an investment idea for a surfing shop in Oahu, Hawaii.  This shop would also sell ice cream, to ensure maximum profitability.  However, previous investments for similar shops had not been productive.  It is theorized that the concerns included lack of planning, especially around weather data.  The hypothesis is that if an island is selected based on weather data such as year-round temperature readings and precipitation levels, a shop of this nature would be profitable.  However, in order to get investors on board, data will need to be shared showing that the island of Oahu is a great spot for a surfing/ice cream shop.

## Resources

- Software: Python 3.7.11, Jupyter Notebook 7.29.0, SQLAlchemy

## Surfs_Up Analysis Results:

The first step in this analysis was to download the SQL database with weather data into Jupyter Notebook.  This data was then stored in SQLite, to allow for the analysis of the data in an effective manner.  We were then able to connect to the SQLite database with SQLAlchemy to assist in querying the database. Our first query reported average precipitation and temperature readings for the previous year.  This information was well-received, but the investors would like to look at two specific times of the year - June and December.  This will help determine whether a shop in Oahu will be profitable year-round.  The following data was retrieved and analyzed for the months of June and December between the years of 2010 and 2017:

* The average temperature for the month of June was 75°F, while the average temperature for December was 71°F.
* The highest temperature for the month of June was 85°F, while the highest temperature for December was 83°F.
* The lowest temperature in the month of June was 64°F, while the lowest temperature in December was 56°F.
* There were 1,700 total temperature readings for the month of June, and 1,517 total temperature readings for the month of December from the 9 stations providing this data.

![June Temperatures](https://github.com/crtallent/surfs_up/blob/main/Resources/June.png)

![December Temperatures](https://github.com/crtallent/surfs_up/blob/main/Resources/December.png)

## Surfs_Up Summary:

The above data indicates that the temperatures in Oahu, Hawaii may be warm enough to justify the existence of a year-round surf and ice cream shop in that area.  The lowest temperature appears in December, but it is still 60°F.  Analysis of ice cream sales and surfing activities in relation to temperature would be useful in making further decisions.  Further analysis on precipitation levels for both June and December could prove very useful information for the investors as well.  This can be done by filtering the Measurement table by precipitation data:

```
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date <= '2017-06-30', Measurement.date >= '2017-06-01').all()
```

```
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date <= '2016-12-31', Measurement.date >= '2016-12-01').all()
```
The following chart shows the precipitation amounts for the months of June 2017 and December 2016, respectfully, showing a low amount of precipitation on average for both months of those years (most recent data):

![June Precipitation Chart](https://github.com/crtallent/surfs_up/blob/main/Resources/June%20Chart.png)
![Dec. Precipitation_Chart](https://github.com/crtallent/surfs_up/blob/main/Resources/Dec%20Chart.png)

While comfortable temperatures are very important, precipitation data also shows that most days have very little precipitation.  This could further indicate that Oahu may be a good choice for a year-round surf and ice cream shop, as comfortable temperatures and low precipitation are common on this island, as shown by the data.  Further analysis could also be completed on temperatures for a year-round snapshot of data, as shown below, indicating that the temperature is most often at 75°F or higher throughout the year:

![2017 Temp Data](https://github.com/crtallent/surfs_up/blob/main/Resources/2017%20Temps.png)
