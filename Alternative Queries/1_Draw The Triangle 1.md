## Problem

P(R) represents a pattern drawn by Julia in R rows. The following pattern represents P(5):

    * * * * * 
    * * * * 
    * * * 
    * * 
    *

Write a query to print the pattern P(20).

## CODE:

    WITH pattern (n) AS 
		(
    	SELECT 20
    	UNION ALL
    		SELECT n - 1 
			FROM pattern 
			WHERE n > 1
		)
		SELECT REPLICATE('* ', n) 
		FROM pattern;
    
## Output:
Your Output (stdout)

    * * * * * * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * * 
    * * * * * * * * * * * * * 
    * * * * * * * * * * * * 
    * * * * * * * * * * * 
    * * * * * * * * * * 
    * * * * * * * * * 
    * * * * * * * * 
    * * * * * * * 
    * * * * * * 
    * * * * * 
    * * * * 
    * * * 
    * * 
    * 



