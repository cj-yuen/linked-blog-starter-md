#language
## Keywords
- <u>SELECT</u>: grab data for specific columns from database
	$*$ (asterisk): used after SELECT to grab ==all columns== from table
	column_name(s): select specific columns
- <u>FROM</u>: specify which table(s) we care about
	can list multiple tables separated by $,$ (commas)
- <u>WHERE</u>: filter results by specific criteria 
	- <u>AND</u>: string together multiple filtering criteria 
	- <u>OR</u>: string together multiple optional criteria
- $\%$ (percentage): "wildcards" = unknown information
	ie. 'Ca%a' matches "Canada" & "California"
```SQL
SELECT DISTINCT place
FROM places_report
WHERE name like 'Ca%a'
```
- $\_$ (underline): "wildcard" = unknown but amount known
	ie. 'B_b' matches "Bob" & "Bub"
		does not match "Babe" or "Bb"
- $>$ (less than) & $<$ (greater than): numeric comparisons
	<u>BETWEEN</u> & <u>AND</u>: comparison for strings
```SQL
SELECT DISTINCT city 
FROM crime_scene_report
WHERE city BETWEEN 'W%' AND 'Z%'; 
```
- <u>UPPER()</u>: apply uppercase
- <u>LOWER()</u>: apply lowercase

## Aggregate Functions
- <u>MAX</u>: find max value
- <u>MIN</u>: find min value
- <u>SUM</u>: calculate sum of column values
- <u>AVG</u>: calculate avg. of column values
- <u>COUNT</u>: count # of column values
- <u>ORDER BY</u>: sort column values
	- <u>ASC</u>: ascending (smallest $\rightarrow$ largest or A $\rightarrow$ Z)
	- <u>DESC</u>: descending (largest $\rightarrow$ smallest or Z $\rightarrow$ A)
- <u>LIMIT</u>: limits the results return by certain amount 

## Joining Tables
- <u>INNER JOIN</u>: (most common) using primary key & foreign key columns
	![[Pasted image 20240521175912.png]]
	ie. 
	![[Pasted image 20240521180708.png]]
	```SQL
	SELECT person.name, income.annual_income 
	FROM income
	JOIN person
	ON income.ssn = person.ssn
	WHERE annual_income > 450000
	```
- <u>OUTER JOIN</u>: 
- <u>LEFT JOIN</u>: 
- <u>RIGHT JOIN</u>: 