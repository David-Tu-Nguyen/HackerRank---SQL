## Problem
 Query the list of **CITY** names from **STATION** that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where **LAT_N** is the northern latitude and **LONG_W** is the western longitude.
## CODE:

    SELECT DISTINCT CITY
    FROM STATION
    WHERE SUBSTRING(CITY, 1, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
        AND SUBSTRING(CITY, LEN(CITY), 1) NOT IN ('A', 'E', 'I', 'O', 'U');
    
## Output:

    Baker 
    Baldwin 
    Bass Harbor 
    Beaufort 
    Beaver Island 
    Benedict 
    Bennington 
    Berryton 
    Beverly 
    Bison 
    Blue River 
    Bowdon 
    Bowdon Junction 
    Bridgeport 
    Bridgton 
    Brighton 
    Brilliant 
    Bristol 
    Brownstown 
    Buffalo Creek {-truncated-}
    