
# Overview
In this challenge,  I  used Python, pandas, and SQLAlchemy to measure the temperatures for June and December and generates the summary statistics.
 
# Result
The below data gives us a summary of different statistics of the temperatures in the month of June.

![temps of June](/Resources/temps%20of%20June.PNG)

The below data gives us a summary of different statistics of the temperatures in the month of December.

![temps of Dec](/Resources/temps%20of%20%20Dec.PNG)


- The maximum temperature of June is 85.000000 however for the month of December is 83.000000.

- The Average temperature of June is 74.944118 however for the month of December is  71.041529.

- The minimum temperature of June is 64.000000 however for the month of December is 56.000000
                     
# Summary
From the data above we can conclude that Hawaii has mild weather through out the year because the temperature is in the 70s. This confirms that this is the ideal location for the surf and ice cream shop.
Below are additional queries to perform to gather more weather data for June and December:
- Query to get the precipitation for the month of December.
```
results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
```
- Query to get the precipitation for the month of June.
```
results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
```
