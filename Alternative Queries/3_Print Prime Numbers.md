## Problem

Write a query to print all prime numbers less than or equal to **1000**. Print your result on a single line, and use the ampersand (**&**) character as your separator (instead of a space).

For example, the output for all prime numbers **<=10** would be:

    2&3&5&7

## CODE:

    SET QUOTED_IDENTIFIER ON
    GO
    With NumberSequence( Number ) as
    (
        Select 2 as Number
            union all
        Select Number + 1
            from NumberSequence
            where Number < 1000     
    ) 

    , primelist as (
    --list of prime numbers
    SELECT 1 as category, myvalue.number as value
    FROM numberSequence myvalue
    LEFT JOIN
    (
    --find the nonprime first
    SELECT DISTINCT myvalue.number

       FROM numbersequence as myvalue

       INNER JOIN numbersequence as compareto
       ON  myvalue.number > compareto.number
       AND ((myvalue.number * 1.0)/compareto.number) = (CEILING(((myvalue.number * 1.0)/compareto.number))  * 1.0)
    ) nonprimelist ON nonprimelist.number = myvalue.number
    WHERE nonprimelist.number IS NULL 
    )

    SELECT
         CAST(STUFF(
         (select CAST('&' AS varchar(1)) + cast(primelist.value as varchar(100))
         from primelist
         order by value
         for xml path(''), type).value('.[1]','nvarchar(max)')
         , 1, 1, '' ) AS VARCHAR(8000)) AS namelist
    option (maxrecursion 0);

## Output:
      
     2&3&5&7&11&13&17&19&23&29&31&37&41&43&47&53&59&61&67&71&73&79&83&89&97&101&103&107&109&113&127&131&137&139&149&151&157&163&167&173&179&181&191&193&197&199&211&223&227&229&233&239&241&251&257&263&269&271&277&281&283&293&307&311&313&317&331&337&347&349&353&359&367&373&379&383&389&397&401&409&419&421&431&433&439&443&449&457&461&463&467&479&487&491&499&503&509&521&523&541&547&557&563&569&571&577&587&593&599&601&607&613&617&619&631&641&643&647&653&659&661&673&677&683&691&701&709&719&727&733&739&743&751&757&761&769&773&787&797&809&811&821&823&827&829&839&853&857&859&863&877&881&883&887&907&911&919&929&937&941&947&953&967&971&977&983&991&997 

