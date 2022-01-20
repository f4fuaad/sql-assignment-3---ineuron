# sql-assignment-3---ineuron

Q-1. Write an SQL query to print the FIRST_NAME from Worker table after removing
white spaces from the right side.

Ans Select RTRIM(FIRST_NAME)
        From worker

Q-2. Write an SQL query that fetches the unique values of DEPARTMENT from Worker
        table and prints its length.

Ans: select distinct(department), len(department))
         From worker

Q-3. Write an SQL query to fetch nth max salaries from a table.

Ans: Select top 1 salary
         From (select top n name_employee, max(salary)
         From worker
         Group by name_employee order by salary desc)
        Order by salary asc

