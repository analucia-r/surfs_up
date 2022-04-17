# surfs_up
The weather data that was in the SQLite database using SQLAlchemy was used for the analysis and was coded in Jupyter notebook. 

# Overview of the analysis
Using the data contained in hawaii.sqlite and using SQLAlchemy it included information about teh temperature and precipitation measurements in Hawaii during the years of 2012 to 2017. The first table was measurement including the status, date and the recorded precipitation. The second table was station which included elevation levels and geographic coordinates. When we did the query for this analysis we summarized the differnces in the island based on the months of December and June. 

# Results: 

- As expected there was a higher average temperature in June than compared to December 
- There was an increase in the standard deviation in December than in June 
- 21 Fahrenheit grade difference in the max and min mesaurement in June and 27  Fahrenheit grade difference in December 


# Summary:
The average on record for the analysis was there was a much more higher temperature in the month of June than in December. Seeing this results we can determine that June will bea more profitable month compared to December. There will be more tourists during the time of Summer and in the Winter can be marketed tot he locals. When taking in consideration an additional query was comparying the different levels of precipitaion between the two months. An exmaple of the code below: 

- results = session.query(Measurement.prcp).filter(extract("month", Measurement.date) == 6).all()
- results = session.query(Measurement.prcp).filter(extract("month", Measurement.date) == 12).all()

