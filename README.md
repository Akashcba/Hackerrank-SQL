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
