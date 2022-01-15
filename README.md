# Surfs_Up

## Overview of Surfs_Up Analysis
In this project, we are exploring an investment idea for a surfing shop in Oahu, Hawaii.  This shop would also sell ice cream, to ensure maximum profitability.  However, previous investments for similar shops had not been productive.  It is theorized that the concerns included lack of planning, especially around weather data.  The hypothesis is that if an island is selected based on weather data such as year-round temperature readings and precipitation levels, a shop of this nature would be profitable.  However, in order to get investors on board, data will need to be shared showing that the island of Oahu is a great spot for a surfing/ice cream shop.

## Resources

- Software: Python 3.7.11, Jupyter Notebook 7.29.0, SQLAlchemy

## Surfs_Up Analysis Results:

The first step in this analysis was to download the SQL database with weather data into Jupyter Notebook.  This data was then stored in SQLite, to allow for the analysis of the data in an effective manner.  We were then able to connect to the SQLite database with SQLAlchemy to assist in querying the database. Our first query reported average precipitation and temperature readings for the previous year.  This information was well-received, but the investors would like to look at two specific times of the year - June and December.  This will help determine whether a shop in Oahu will be profitable year-round.  The following data was retrieved and analyzed for the months of June and December:

* The average temperature for the month of June was 77°F, while the average temperature for December was 71°F.
* The highest temperature for the month of June was 83°F, while the average temperature for December was 78°F.
* The lowest temperature in the month of June was 71°F, while the lowest temperature in December was 60°F.
* There were 191 total temperature readings for the month of June, and 200 total temperature readings for the month of December from the 9 stations providing this data.

![June Temperatures](https://github.com/crtallent/surfs_up/blob/main/Resources/June.png)

![Dec. Temperatures](https://github.com/crtallent/surfs_up/blob/main/Resources/December.png)


