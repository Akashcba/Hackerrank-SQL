# Hackerrank-SQL
Solution for All SQL practice questions on Hackerrank.
## [Revising The Select Query 1](https://www.hackerrank.com/challenges/revising-the-select-query)
```SQL
select * from city
where population > 100000 and countrycode = 'USA' ;
```
## [Revising The Select Query 2](https://www.hackerrank.com/challenges/revising-the-select-query-2)
```SQL
select name from city
where population > 120000 and countrycode = 'USA' ;
```
## [Select All](https://www.hackerrank.com/challenges/select-all-sql)
```SQL
select * from city ;
```
## [Select By ID](https://www.hackerrank.com/challenges/select-by-id)
```SQL
select * from city where id = 1661 ;
```
## [Japanese Cities Attributes](https://www.hackerrank.com/challenges/japanese-cities-attributes)
```SQL
select * from city
where countrycode = 'JPN' ;
```
## [Japanese Cities Names](https://www.hackerrank.com/challenges/japanese-cities-name)
```SQL
select name from city
where countrycode = 'JPN' ;
```
## [Weather Observation Station 1](https://www.hackerrank.com/challenges/weather-observation-station-1/problem)
```SQL
seelct city ,state from station ;
```
## [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem)
```SQL
select distinct city from station where ID%2 = 0 ;
```
## [Weather Observation Station 4](https://www.hackerrank.com/challenges/weather-observation-station-4/problem)
```SQL
select count(city) - count(distinct city) from station ;
```
## [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem)
```SQL
Select city ,length(city) from station group by city order by length(city) ,city limit 1;
select city, length(city) from station group by city order by length(city) desc ,city limit 1;
```
## [Weather Station Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem)
```SQL
Select distinct city from station where city regexp '^[aeiou]' ;
```
## [Weather Observation STATION 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem)
```SQL
Select distinct city from station where city regexp '[aeiou]$';
```
## [Weather Observation Station 8](https://www.hackerrank.com/challenges/weather-observation-station-8/problem)
```SQL
Select distinct city from station
where city regexp '^[aeiou].*[aeiou]$' ;
```
## [Weather Observation Station 9](https://www.hackerrank.com/challenges/weather-observation-station-9/problem)
```SQL
Select Distinct city from station
where city regexp '^[^aeiou]' ;
```
## [Weather Observation Station 10](https://www.hackerrank.com/challenges/weather-observation-station-10/problem)
```SQL
Select distinct city from station
where city regexp "[^aeiou]$" ;
```
## [Weather Observation Station 11](https://www.hackerrank.com/challenges/weather-observation-station-11/problem)
```SQL
Select distinct city from Station
where city regexp '^[^aeiou]|[^aeiou]$' ;
```
## [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem)
```SQL
Select distinct city from station
where city regexp '^[^aeiou].*[^aeiou]$' ;
```
## [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem)
```SQL
Select Name from students
where marks > 75
order by right(name,3) ,id ;
```
## [Employees Names](https://www.hackerrank.com/challenges/name-of-employees/problem)
```SQL
Select name from employee
order by name asc ;
```
## [Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees)
```SQL
Select name from emplyee
where salary > 2000 and months < 10
order by employee_id asc ;
```
## [Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle)
```SQL
Select CASE
When 2*greatest(A,B,C) >= (A+B+C) Then "Not A Triangle"
When A = B and A = c Then "Equilateral"
When A = B or B = C or A = C Then "Isosceles"
Else "Scalene"
End
from Triangles ;
```
## [The Pads](https://www.hackerrank.com/challenges/the-pads)
```SQL
Select concat(name ,'(',left(occupation),')') from occupations
order by name ;
Select concat('There are a total of ',count(occupation),' ',lower(occupation),'s.') from occupations
group by occupation
order by count(occupation) ;
```
## [Revising Aggregations - The Count](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function)
```SQL
Select count(name) from city where population > 100000;
```
## [Revising Aggregations - The Sum Function](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem)
```SQL
Select sum(population) from city
where city = 'California' ;
```
## [Revising Aggregations - Averages](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem)
```SQL
Select avg(population) from city
where district = 'California' ;
```
## [Average Population](https://www.hackerrank.com/challenges/average-population/problem)
```SQL
Select round( avg(population)) from city ;
```
## [Japan Population](https://www.hackerrank.com/challenges/japan-population/problem)
```SQL
Select sum(population) from city
where countrycode = 'JPN' ;
```
## [Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem)
```SQL
Select (max(population) - min(population)) from city ;
```
## [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem)
```SQL
Select ceil(avg(salary) - (select avg(replace(salary,0,"")) from employees) ) from employees ;
```
## [Top Earners](https://www.hackerrank.com/challenges/earnings-of-employees/problem)
```SQL
Select salary*months as earnings ,count(*) from city
group by earnings
order by earnings desc
limit 1 ;
```
## [Weather Observation Station 2](https://www.hackerrank.com/challenges/weather-observation-station-2/problem)
```SQL
Select round(sum(lat_n) ,2), round(sum(long_w), 2) from station ;
```
## [Weather Station 13](https://www.hackerrank.com/challenges/weather-observation-station-13/problem)
```SQL
Select round(sum(lat_n), 4) from station
where lat_n > 38.7880 and lat_n < 137.2345 ;
```
## [Weather Station 14](https://www.hackerrank.com/challenges/weather-observation-station-14/problem)
```SQL
Select round(max(lat_n) ,4) from station
where lat_n < 137.2345 ;
```
## [Weather Station 15](https://www.hackerrank.com/challenges/weather-observation-station-15/problem)
```SQL
Select round(long_w,4) from station
where lat_n < 137.2345
order by 137.2345
limit 1 ;
```
## [Weather Observation Station 16](https://www.hackerrank.com/challenges/weather-observation-station-16/problem)
```SQL
Select round(lat_n, 4) from station
where lat_n > 38.7780
order by lat_n asc
limit 1 ;
```
## [Weater Observation Station 17](https://www.hackerrank.com/challenges/weather-observation-station-17/problem)
```SQL
Select round(lat_n, 4) from station
where lat_n > 38.7780
order by lat_n asc
limit 1 ;
```
## [Weather Observation 18](https://www.hackerrank.com/challenges/weather-observation-station-18/problem)
```SQL
Select round(((max(lat_n) - (min(lat_n))) + (max(long_w)-min(long_w))),4) from station ;
```
## [Weather Observation Station 19](https://www.hackerrank.com/challenges/weather-observation-station-19/problem)
```SQL
Select round(sqrt((pow(max(lat_n)-min(lat_n)),2) + pow((max(long_w)-min(long_w)),2)),4) from station ;
```
## [Asian Population](https://www.hackerrank.com/challenges/weather-observation-station-19/problem)
```SQL
Select sum(city.population)
from city inner join country
on city.countrycode = country.code
where country.continent = 'Asia' ;
```
## [African Cities](https://www.hackerrank.com/challenges/african-cities/problem)
```SQL
Select city.name
from city inner join country
on city.countrycode = country.code and country.continent = 'Africa' ;
```
## [Average Population of Each Continent](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem)
```SQL
Select country.continent ,floor(city.population)
from city inner join country
on city.countrycode = country.code
group by country.continent ;
```
## [Draw The Triangle 1](https://www.hackerrank.com/challenges/draw-the-triangle-1/problem)
```SQL
set @number = 21;
select repeat('* ', @number := @number - 1) from information_schema.tables ;
```
## [Draw The Triangle 2](https://www.hackerrank.com/challenges/draw-the-triangle-2/problem)
```SQL
set @number = 0 ;
select repeat('* ', @number := @number + 1) from information_schema.tables
where @number < 20;
```
Think of the information_schema.tables as a dummy table with no real use in the statement except to satisfy the MySQL condition that every SELECT must have a FROM ;
Also, it contains as many rows as you could possibly need so it is a neat trick for incrementing variables. Just select the incrementing variable and specify the where condition on your incrementing variable.

## [Weather Observation Station 20](https://www.hackerrank.com/challenges/weather-observation-station-20/problem)
### Code To Find Median
```SQL
select round(x.lat_n,4) from station x, station y
group by x.lat_n
having sum(sign(1-sign(x.lat_n - y.lat_n))) = (count(*)+1)/2 ;
```
#### Having Clause was used because the WHERE keyword cannot be used with aggregate functions.
#### Sign() Function returns the sign of the number.

## [Ollivander's Inventory](https://www.hackerrank.com/challenges/harry-potter-and-wands/problem)
```SQL
select wands.id , wands_property.age, wands.coins_needed ,wands.power
from wands join wands_property
on wands.code = wands_property.code
where (wands_property.age, wands.power, wands.coins_needed) in (
    select wands_property.age , wands.power, min(wands.coins_needed)
    from wands join wands_property
    on wands.code = wands_property.code
    where is_evil = 0
    group by wands_property.age ,wands.power)
order by wands.power desc, wands_property.age desc ;
```
## [Symmetric Pairs](https://www.hackerrank.com/challenges/symmetric-pairs/problem)
```SQL
Select a.x, a.y
from functions a, functions b
where a.x = b.y and a.y = b.x
group by a.x, a.y
having count(a.x) > 1 or a.x<a.y
order by a.x asc ;
```
### The criteria in the having clause allows us to prevent duplication in our output while still achieving our goal of finding mirrored pairs. We have to treat our pairs where a.x = a.y and a.x <> a.y differently to capture both. The first criteria handles pairs where a.x = a.y and the 2nd criteria handles pairs where a.x <> a.y, which is why the or operator is used.
### The first part captures records where a.x = a.y. The 'count(a.x) > 1' requires there to be at least two records of a mirrored pair to be pulled through. Without this a pair would simply match with itself (since it's already it's own mirrored pair) and be pulled through incorrectly when you join the table on itself.
### The 2nd part matches the remaining mirrored pairs. It's important to note that for this challenge, the mirrored match of (a.x,b.y) is considered a duplicate and excluded from the final output. You can see this in the sample output where (20, 21) is outputted, but not (21,20). The 'or a.x < a.y' criteria allows us to pull all those pairs where a.x does not equal a.y, but where a.x is also less than a.y so we don't end up with the mirrored paired duplicate.

# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


# License
[MIT](https://choosealicense.com/licenses/mit/)
