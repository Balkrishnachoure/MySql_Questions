# MySql_Questions


Order of Execution of Sql Queries :

In an SQL query, the logical processing order of the statements is as follows:
FROM clause: The data is retrieved from the specified table(s) in the FROM clause.
WHERE clause: If there's a WHERE clause, the conditions specified are applied to filter the rows from the tables specified in the FROM clause.
GROUP BY clause: If there's a GROUP BY clause, the rows are then grouped based on the specified columns.
SELECT clause: The SELECT clause is applied to the grouped data, and any aggregate functions are calculated (such as COUNT in your case).
ORDER BY clause: If there's an ORDER BY clause, the results are then sorted based on the specified columns.

Some Theoretical Qustions :
1.Explain 1Nf,2NF ,3NF ,BCNF ?
2.Explain All joins ?
3.Difference between Delete and Truncate , Primary Key and Composite Key , Unique and Primary Key ?
4.Look into and see the Query of Update ,Alter ,Drop ?

Section 1 :  Aggregate Functions : Count() , Max() , Min() , Sum() , Avg()  
1. Calculate the average salary of all employees in the "salaries" table.
2. Grouping and Aggregating: For each department in the "employees" table, find the total number of employees and the average salary.
3. List the departments from the "employees" table where the average salary is greater than 50000.
4. Calculate the total number of employees and the average salary for each department in the "employees" table.
5. Find the number of unique job titles in the "jobs" table.
6. Find the department with the highest average salary in the "employees" table.
7. Using GROUP_CONCAT or STRING_AGG:  Concatenate the names of all employees in each department, separated by a comma.


 Section 2 :  Group By and  Having Clause :  Having clause can't be used without group by but group by can be used without having :
 1. Write a query to find the total number of employees in each department from the "employees" table.
 2. Find the number of employees in each salary range (e.g., 0-50000, 50001-100000, etc.) from the "salaries" table
 3. List the job titles and their respective average salaries. Display only those job titles where the average salary is below 70000.
 4. For each department, calculate the average salary and display only those departments where the average salary is above 60000.
 5. Write a query to find the total number of employees in each department and only display departments with more than 10 employees.
 6. Calculate the standard deviation of salaries for each department and display only those departments where the standard deviation is greater than 10000.
 7. Find the maximum salary in each department and only display departments where the maximum salary is above 90000.
 8. Calculate the total bonus amount for each department and display only those departments where the total bonus is greater than 50000.
 9. Salary Growth Analysis:For each department, find the average salary for the year 2023 and the average salary for the year 2024. Display only those departments where the average salary has increased by at least 10%.

Section 3 : Order By :
1.Basic Ordering:Write a query to retrieve all employees from the "employees" table ordered by their last name in ascending order.
2.Descending Order:Retrieve the names and salaries of all employees from the "employees" table, ordering them by their salary in descending order.
3.Multiple Columns Order:Show the names, departments, and salaries of employees from the "employees" table, ordered by department first in ascending order, and then by salary in descending order.
4.Ordering with NULL Values:Retrieve all records from the "students" table ordering them by the "birthdate" column in ascending order. Handle NULL values appropriately.
5.Order by Expression:Write a query to fetch the names of employees and their total annual salary (assuming a monthly salary exists), ordered by the total annual salary in descending order.
6.Order by Aggregate Function:Retrieve the department names and the total number of employees in each department, ordered by the total number of employees in descending order.
7.Order by Date:Fetch all orders from the "orders" table ordered by their order date in descending order.
8.Order by String Length:Retrieve the names of all products from the "products" table ordered by the length of their product name in ascending order.
9.Order by Multiple Columns with Different Directions:Write a query to fetch the names and joining dates of employees from the "employees" table, ordered by joining date in descending order, and then by name in ascending order.
10.Order by Case Statement:Fetch all student records from the "students" table and order them by their grade level. However, if the grade level is 'K', it should appear last.

Section 4 : Joins :
1.Inner Join:Retrieve the names of all employees and their corresponding department names from the "employees" and "departments" tables using an inner join.
2.Left Join:Display the names of all employees and their department names. If an employee does not belong to any department, display "No Department" instead, using a left join.
3.Right Join:List all departments and the names of employees who belong to them. If a department has no employees, display "No Employees" using a right join.
4.Full Outer Join:Fetch all records from both the "students" and "grades" tables, displaying student names and their grades if available. If a student has no grade, display "Not Graded".
5.Self Join:Retrieve the names of all employees and their managers from the "employees" table. Match employees to their managers using a self join.
6.Cross Join:List all possible combinations of employees and departments from the "employees" and "departments" tables using a cross join.
7.Join with Multiple Conditions:Retrieve the names of all employees and their corresponding department names where the employee's department ID matches and the department is located in 'New York'.
8.Join with Aggregate Functions:Display the department names and the total number of employees in each department from the "employees" table using an appropriate join.
9.Join with Subquery:
Retrieve the names of all products and their suppliers from the "products" and "suppliers" tables, where the supplier's country is 'USA'.
10.Join with Group By:Show the department names and the average salary of employees in each department, considering only departments with an average salary greater than $50000.
11.Nested Join with IN Clause:Retrieve the names of all employees from the "employees" table who work in departments located in 'New York'. Use a nested subquery with the IN clause to achieve this.
12.Nested Join with EXISTS Clause:List all products from the "products" table that have been ordered at least once. Utilize a nested subquery with the EXISTS clause to accomplish this task.
13.Nested Join with Aggregate Function:Display the names of all employees who have a salary greater than the average salary of employees in their department. Use a nested subquery with an aggregate function to compute the average salary for each department.

     
