## Problem

 Query the two cities in **STATION** with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Sample Input**

Let's say that CITY only has four entries: DEF, ABC, PQRS and WXY

**Sample Output**

    ABC 3
    PQRS 4
    
**Explanation**

When ordered alphabetically, the CITY names are listed as ABC, DEF, PQRS, and WXY, with the respective lengths **3,3,4**  and **3** . The longest-named city is obviously PQRS, but there are **3** options for shortest-named city; we choose ABC, because it comes first alphabetically.

**Note**

**You can write two separate queries to get the desired output. It need not be a single query.**

## CODE:
    -- Query to find the shortest city name
    SELECT TOP 1 CITY, LEN(CITY) AS CityLength
    FROM STATION
    ORDER BY LEN(CITY) ASC, CITY ASC;

    -- Query to find the longest city name
    SELECT TOP 1 CITY, LEN(CITY) AS CityLength
    FROM STATION
    ORDER BY LEN(CITY) DESC, CITY ASC;
    
## Output:

    Amo 3 
    Marine On Saint Croix 21 



