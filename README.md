# surfs_up

## Overview
The purpose of the analysis was to analyze weather data for the city of Oahu. The analysis targeted the months of June and December in effort to determine if a surf and ice cream shop business is sustainable year-round in this location.

## Results
Key differences between weather in June and December:<br>
    - Average temperatures in June were higher than average temperatures in December<br>
    - Minimum temperature recorded in December was 8 degrees lower than the lowest temperature recorded in June<br>
    - Total number of observations recorded in June were higher than that of December
    
**June Temperature statistics**<br> 
<img src= "https://github.com/ChrisBarton107/surfs_up/blob/main/Resources/June_temps.png" height="700" width="600"><br>

**December Temperature statistics**<br> 
<img src= "https://github.com/ChrisBarton107/surfs_up/blob/main/Resources/December_temps.png" height="700" width="500"><br>

## Summary
The analysis found that temperature in Oahu was relatively similar during the months of June and December. Average temperatures in June and December were approximately 75 and 71 degrees respectively. The only significant difference was found when finding minimum temperatures, with temperatures coming in at 64 degrees in June and 56 degrees in December. If additional weather data is desired, queries such as the following can supplement the current analysis:

- june_precipitation = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6)<br>
This query will extract all precipitation data from the month of June in the database and can be modified to extract precipitation data from December

- december_precipitation = session.query(Measurement.date, Measurement.prcp).\
filter(extract('month', Measurement.date) == 12).\
filter(extract('year', Measurement.date) == 2016).all()<br>
This query will extract precipitation data from the month of December during the year of 2016 and can be modified to extract precipitation data from June and any   other year when data was gathered

To further investigate the potential of the business venture, it would be encouraged to perform an analysis incorporating precipitation related data.
