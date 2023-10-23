# find-max-number-using-different-methods-in-SQL
FIND SENCOND NUMER USING DIFFRENT TINGS IN SQL 


  QUESTION ----write a query to find max salary given to male and female employee

  ANS BY USING JOINS ---

  select g.gender as gender,
	max(e.salary) as max_salary_ML
from employee e
join gender as g 
on g.id = e.genderid 
group by g.gender;


ANS -- BY USING SUBQUERY 

select max(salary) as max_salary_male from employee
where genderid = 2 
(select max(salary) as max_salary_female from employee 
where genderid = 1)
