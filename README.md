# Surfs_Up

## Overview
  
  This analysis was created to allow for a description of weather conditions, in Oahu, to be presented to a group of potential investors. This location's weather was analyzed so that the potential investors could evaluate the viability of investing in a startup surf shop owned and operated by yours truly. This anlysis uses Python, Pandas, Jupyter Notebook, SQL Alchemy, and a SQLite database to summarize the temperatures of given months so that any weather hinderances, to the surf shop's success, can be evaluated and/or accounted for.
  
## Results
  
    Some interesting results can be seen from the following two analyses.
    
### June Temperature Summary
![June_temp_summary.png](https://github.com/Beardlow/Surfs_Up/blob/main/June_temp_summary.png)

### December Temperature Summary
![Dec_temp_summary.png](https://github.com/Beardlow/Surfs_Up/blob/main/Dec_temp_summary.png)

*The weather in Oahu when comparing June and December is surprisingly very similar. (When compared to Ohio that is...)
  *Average Temperatures
    *June average temperature is 74.9 degees Fahrenheit.
    *December average temperature is 71.0 degrees Fahrenheit.
  *Minumum Temperatures
    *June minimum temperature is 64.0 degrees.
    *December minimum temperature is 56.0 degrees.
  *Maximum Temperatures
    *June maximum temperature is 85.0 degrees.
    *December maximum temperature is 83.0 degrees.
    
## Summary

  Overall the weather in Oahu seems very pleasant; however, there could be additional information gathered from the provided information in the hawaii.sqlite database. For instance the rainfall summary statistics for June could be gleaned by using the the following query in our Jupyter Notebook.
```
june_rain_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==6)
```
Additionally the December rainfall summary statistics could be gathered by using a very similar query as seen below.
```
dec_rain_results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==12)
```
This information could provide some useful insights into the cash flow of the store, assuming that a target sales per day in known and an estimate for reduced sales during poor weather could be extrapolated/assumed.
  
