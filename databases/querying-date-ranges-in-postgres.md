# Querying Date ranges in postgres

When we are trying to query a Date with an PostgresSQL query like:

```
SELECT d, name from table1
where d between '2021-10-01' and '2021-11-31';
```

You will notice your query in Postgres is not including the upper bond ie **2021-11-31.** &#x20;

**I**norder to resolve this you can query it like below using DATE field with <= and >= operator. This will ensure both the dates are included in the upper bound and lower bound.

```
SELECT d, name from table1
where DATE(d) >= '2021-10-01' and DATE(d) <= '2021-11-31';
```

This query can be implemented in SQLAlchemy as following:



```
db.query(table1.d, table1.name)
.filter(
    func.date(table1.d)>='2021-10-01',
    func.date(table1.d)<='2021-11-31'
    )
```
