# TIL New SQL Operators - Except, UNION, Distinct

**Except Operator**

The `EXCEPT` operator returns distinct rows from the first (left) query that are not in the output of the second (right) query



**Eg: select \* from table1**

**except**

**select \* from table 2**

****

Returns all elements in table1 not present in table2

**UNION and Intersect Operator**

In case of two queries in two tables. The Union and Intersect operator does the union and intersection of two sets.



![](<../.gitbook/assets/image (30).png>)



**Distinct Operator**

In case of distinct operator, it returns all the unique values corresponding to a query value we want.



`SELECT DISTINCT(status) FROM employee;`
