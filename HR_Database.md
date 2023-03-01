# Task 1
```sql
SELECT E.first_name,
  E.last_name , 
  E.department_id,
  D.department_name 
FROM employees E
JOIN departments D 
  ON E.department_id = D.department_id;
```
![image](https://user-images.githubusercontent.com/81769242/222070511-9da4173a-c612-475f-b008-865f61e7804f.png)

# Task 2
```sql
SELECT
  E.first_name,
  E.last_name, 
  D.department_name,
  L.city,
  L.state_province
FROM employees E 
JOIN departments D  
  ON E.department_id = D.department_id  
JOIN locations L
  ON D.location_id = L.location_id;
```
![image](https://user-images.githubusercontent.com/81769242/222070967-5244e553-b7e9-4866-a2ec-a30dbc80d932.png)


# Task 3
```sql
SELECT
  E.first_name,
  E.last_name,
  E.salary,
  J.grade_level
FROM employees E 
JOIN job_grades J
  ON E.salary BETWEEN J.lowest_sal AND J.highest_sal;
```
![image](https://user-images.githubusercontent.com/81769242/222071938-927f61fb-b9e0-4342-86c9-08e7928c3512.png)


# Task 4
```sql
SELECT
  E.first_name,
  E.last_name , 
  E.department_id,
  D.department_name 
FROM employees E 
JOIN departments D 
  ON E.department_id = D.department_id 
    AND E.department_id IN (80 , 40)
ORDER BY E.last_name;
```
![image](https://user-images.githubusercontent.com/81769242/222072406-fe3786c3-b11a-43d2-a173-d98108a75aef.png)


# Task 5
```sql
SELECT
  E.first_name,
  E.last_name,
  D.department_name,
  L.city,
  L.state_province
FROM employees E
JOIN departments D
  ON E.department_id = D.department_id
JOIN locations L
  ON D.location_id = L.location_id
  WHERE E.first_name LIKE  '%z%';
```
![image](https://user-images.githubusercontent.com/81769242/222073785-6e91f877-ccdf-4bf4-81ab-9c3e6ab0964c.png)


# Task 6
```sql
SELECT
  E.first_name,
  E.last_name,
  D.department_id,
  D.department_name
FROM employees E
RIGHT JOIN departments D
  ON E.department_id = D.department_id;
```
![image](https://user-images.githubusercontent.com/81769242/222075310-d36f2427-2375-4b0a-8b1b-5f1d7d898bce.png)


# Task 7
```sql
SELECT
  E.first_name,
  E.last_name,
  E.salary
FROM employees E
JOIN employees S
  ON E.salary < S.salary AND S.employee_id = 182;
```
![image](https://user-images.githubusercontent.com/81769242/222078120-b35b635c-8789-4575-99c8-ecb792793d11.png)


# Task 8
```sql
SELECT
  E.first_name AS "Employee Name",
  M.first_name AS "Manager"
FROM employees E
JOIN employees M
  ON E.manager_id = M.employee_id;
```
![image](https://user-images.githubusercontent.com/81769242/222079270-b7c5a7eb-cb50-48c5-a88a-b046bcad6b71.png)


# Task 9
```sql
SELECT
  D.department_name,
  L.city,
  L.state_province
FROM  departments D
JOIN locations L
  ON D.location_id = L.location_id;
```
![image](https://user-images.githubusercontent.com/81769242/222079567-4ab75bad-bdb4-46cb-a905-05e221cbefd9.png)


# Task 10
```sql
SELECT
  E.first_name,
  E.last_name,
  E.department_id,
  D.department_name
FROM employees E
LEFT JOIN departments D
  ON E.department_id = D.department_id;
```
![image](https://user-images.githubusercontent.com/81769242/222079926-f0483417-39f6-4cdd-9bce-ae97d086b807.png)


# Task 11
```sql
SELECT
  E.first_name AS "Employee Name",
  M.first_name AS "Manager"
FROM employees E
LEFT JOIN employees M
  ON E.manager_id = M.employee_id;
```
![image](https://user-images.githubusercontent.com/81769242/222080275-b3a1cf63-e66b-4967-915d-0a829ddb7ffc.png)


# Task 12
```sql
SELECT
  E.first_name,
  E.last_name,
  E.department_id
FROM employees E
JOIN employees S
  ON E.department_id = S.department_id AND S.last_name = 'Taylor'
```
![image](https://user-images.githubusercontent.com/81769242/222094100-65a29d6d-2ff6-4039-99f6-5ded410b6cca.png)


# Task 13
```sql
SELECT
  job_title,
  department_name,
  first_name || ' ' || last_name AS employee_name,
  start_date 
FROM job_history 
JOIN jobs USING (job_id) 
JOIN departments USING (department_id) 
JOIN  employees USING (employee_id) 
WHERE start_date >= '1993-01-01' AND start_date <= '1997-08-31';
```
![image](https://user-images.githubusercontent.com/81769242/222094653-1c4292d3-1e0d-4633-962c-1f205940e04a.png)


# Task 14
```sql
SELECT
  job_title,
  first_name || ' ' || last_name AS employee_name,
  max_salary-salary AS salary_difference
FROM employees
NATURAL JOIN jobs;
```
![image](https://user-images.githubusercontent.com/81769242/222096460-014f97f1-4730-407b-89df-962c7d2eb577.png)


# Task 15
```sql
SELECT
  department_name,
  ROUND(AVG(salary), 2),
  COUNT(commission_pct)
FROM departments 
JOIN employees USING (department_id) 
GROUP BY department_name;
```
![image](https://user-images.githubusercontent.com/81769242/222103465-2e1525bb-74d0-44a7-86f6-29e0bbcfdbd5.png)


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


# Task 
```sql

```


