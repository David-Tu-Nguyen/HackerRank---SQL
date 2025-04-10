## Problem

Write a query that prints a list of employee names (i.e.: the name attribute) for employees in **Employee** having a salary greater than _**$2000**_  per month who have been employees for less than **_10_** months. Sort your result by ascending employee_id.

**Input Format**

The **Employee** table containing employee data for a company is described as follows:

![](https://s3.amazonaws.com/hr-challenge-images/19629/1458557872-4396838885-ScreenShot2016-03-21at4.27.13PM.png)

where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is the their monthly salary.

**Sample Input**

![](https://s3.amazonaws.com/hr-challenge-images/19630/1458558612-af3da3ceb7-ScreenShot2016-03-21at4.32.59PM.png)

**Sample Output**

    Angela
    Michael
    Todd
    Joe
    
**Explantion**

Angela has been an employee for **_1_**  month and earns **_$3443_** per month.

Michael has been an employee for **_6_** months and earns **_2017_** per month.

Todd has been an employee for **_5_** months and earns **_3396_** per month.

Joe has been an employee for **_9_** months and earns **_3573_** per month.

We order our output by ascending employee_id.

## CODE:

    select name
    from Employee
    where salary > 2000
        and months < 10
    ORDER BY employee_id ASC;
    
## Output:

    Rose 
    Patrick 
    Lisa 
    Amy 
    Pamela 
    Jennifer 
    Julia 
    Kevin 
    Paul 
    Donna 
    Michelle 
    Christina 
    Brandon 
    Joseph 
    Jesse 
    Paula 
    Louise 
    Evelyn 
    Emily 
    Jonathan {-truncated-}

