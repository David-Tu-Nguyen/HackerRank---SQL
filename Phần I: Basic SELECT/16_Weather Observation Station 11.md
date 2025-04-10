## Problem

 Query the list of CITY names from **STATION** that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## CODE:

    SELECT DISTINCT CITY
    FROM STATION
    WHERE SUBSTRING(CITY, 1, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
        OR SUBSTRING(CITY, LEN(CITY), 1) NOT IN ('A', 'E', 'I', 'O', 'U');
    
## Output:

    Addison 
    Agency 
    Alanson 
    Albany 
    Albion 
    Algonac 
    Allerton 
    Alton 
    Andover 
    Anthony 
    Arlington 
    Arrowsmith 
    Athens 
    Auburn 
    Baileyville 
    Bainbridge 
    Baker 
    Baldwin 
    Barrigada 
    Bass Harbor {-truncated-}
    