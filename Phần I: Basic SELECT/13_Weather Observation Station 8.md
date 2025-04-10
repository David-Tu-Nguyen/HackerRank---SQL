## Problem
 
 Query the list of **CITY** names from **STATION** which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## CODE:

    SELECT CITY
    FROM STATION
    WHERE UPPER(SUBSTRING(CITY, 1, 1)) IN ('A', 'E', 'I', 'O', 'U')
         AND UPPER(SUBSTRING(CITY, LEN(CITY), 1)) IN ('A', 'E', 'I', 'O', 'U')
    group by city;
    
## Output:

    Acme 
    Aguanga 
    Alba 
    Aliso Viejo 
    Alpine 
    Amazonia 
    Amo 
    Andersonville 
    Archie 
    Arispe 
    Arkadelphia 
    Atlantic Mine 
    East China 
    East Irvine 
    Eastlake 
    Eleele 
    Elm Grove 
    Eriline 
    Ermine 
    Eskridge {-truncated-}
    