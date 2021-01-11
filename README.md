# Hackerrank-SQL
Solution for All SQL practice questions on Hackerrank.

## Weather Observation Station 1
```SQL
seelct city ,state from station ;
```
## Weather Observation Station 3
```SQL
select distinct city from station where ID%2 = 0 ;
```
## Weather Observation Station 4
```SQL
select count(city) - count(distinct city) from station ;
```
## Weather Observation Station 5
```SQL
Select city ,length(city) from station group by city order by length(city) ,city limit 1;
select city, length(city) from station group by city order by length(city) desc ,city limit 1;
```
## Weather Station Observation Station 6
```SQL
Select distinct city from station where city regexp '^[aeiou]' ;
```
## Weather Observation STATION 7
```SQL
Select distinct city from station where city regexp '[aeiou]$';
```
## Weather Observation Station 8
```SQL
Select distinct city from station
where city regexp '^[aeiou].*[aeiou]$' ;
```
## Weather Observation Station 9
```SQL
Select Distinct city from station
where city regexp '^[^aeiou]' ;
```
## Weather Observation Station 10
```SQL
Select distinct city from station
where city regexp "[^aeiou]$" ;
```
## Weather Observation Station 11
```SQL
Select distinct city from Station
where city regexp '^[^aeiou]|[^aeiou]$' ;
```
## Weather Observation Station 12
```SQL
Select distinct city from station
where city regexp '^[^aeiou].*[^aeiou]$' ;
```
## Higher Than 75 Marks
```SQL
Select Name from students
where marks > 75
order by right(name,3) ,id ;
```
## Employees Names
```SQL
Select name from employee
order by name asc ;
```
## Employee Salaries
```SQL
Select name from emplyee
where salary > 2000 and months < 10
order by employee_id asc ;
```
## Type of Triangle
```SQL
Select CASE
When 2*greatest(A,B,C) >= (A+B+C) Then "Not A Triangle"
When A = B and A = c Then "Equilateral"
When A = B or B = C or A = C Then "Isosceles"
Else "Scalene"
End
from Triangles ;
```
## The Pads
```SQL
Select concat(name ,'(',left(occupation),')') from occupations
order by name ;
Select concat('There are a total of ',count(occupation),' ',lower(occupation),'s.') from occupations
group by occupation
order by count(occupation) ;
```
## Revising Aggregations - The Count
```SQL
Select count(name) from city where population > 100000;
```
