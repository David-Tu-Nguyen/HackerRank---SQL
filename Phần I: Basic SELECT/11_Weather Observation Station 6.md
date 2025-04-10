## Problem

 Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from **STATION**. Your result cannot contain duplicates.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where LAT_N is the northern latitude and LONG_W is the western longitude.

## CODE:

    select city 
    from station 
    WHERE CITY LIKE 'A%' 
        OR CITY LIKE 'E%' 
        OR CITY LIKE 'I%' 
        OR CITY LIKE 'O%' 
        OR CITY LIKE 'U%';
    
## Output:

    Acme 
    Addison 
    Agency 
    Aguanga 
    Alanson 
    Alba 
    Albany 
    Albion 
    Algonac 
    Aliso Viejo 
    Allerton 
    Alpine 
    Alton 
    Amazonia 
    Amo 
    Andersonville 
    Andover 
    Anthony 
    Archie 
    Arispe {-truncated-}
    