## Problem

 Query the list of **CITY** names ending with vowels (a, e, i, o, u) from **STATION**. Your result cannot contain duplicates.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## CODE:

    SELECT DISTINCT CITY
    FROM STATION
    WHERE CITY LIKE '%A' 
     OR CITY LIKE '%E' 
     OR CITY LIKE '%I' 
     OR CITY LIKE '%O' 
     OR CITY LIKE '%U';
    
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
    Baileyville 
    Bainbridge 
    Barrigada 
    Baton Rouge 
    Bayville 
    Bellevue 
    Bentonville 
    Bertha {-truncated-}
    