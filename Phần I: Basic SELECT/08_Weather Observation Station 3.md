## Problem
 Query a list of **CITY** names from **STATION** with even ID numbers only. You may print the results in any order, but must exclude duplicates from your answer.
 
 **Input Format:**
 
 The **STATION** table is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where **LAT_N** is the northern latitude and **LONG_W** is the western longitude.

## CODE:

    select city 
    from Station
    where ID % 2 = 0
    group by city 
    
## Output:

    Aguanga 
    Alba 
    Albany 
    Amo 
    Andersonville 
    Archie 
    Athens 
    Atlantic Mine 
    Bainbridge 
    Baker 
    Bass Harbor 
    Bayville 
    Beaufort 
    Bellevue 
    Benedict 
    Bennington 
    Bentonville 
    Biggsville 
    Bison 
    Bono {-truncated-}
    