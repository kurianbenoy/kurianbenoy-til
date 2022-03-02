# Analysing Performance of DB Queries

How can you understand if your Database queries are actually being indexed or not and how efficiently they are searching?

### PostgreSQL

Let's look at how we can analyze the queries in PostgreSQL:



```
explain analyze select id, name from employees where id = 12
```

### MongoDB

In case of mongodb as well there is an explain after collection name which you can use to understand the query performance:

You can use the `cursor.explain()` method or the `db.collection.explain()` method to determine whether or not a query uses an index. On using explain in mongodb queries you can notice that in case of query which requires full search will be in `COLLSCAN status.`

``![](<../.gitbook/assets/image (29).png>)``



Now in case of efficient searching with indexes, it will be in the stage: IXSCAN

**References**

{% embed url="https://database.guide/find-out-if-a-query-uses-an-index-in-mongodb" %}

{% embed url="https://youtu.be/-qNSXK7s7_w" %}
