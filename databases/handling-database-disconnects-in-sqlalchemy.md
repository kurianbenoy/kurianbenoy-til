# Handling Database disconnects in SQLAlchemy

Have you heard about connection pool?

> A connection pool is a standard technique used to maintain long running connections in memory for efficient re-use, as well as to provide management for the total number of connections an application might use simultaneously.Particularly for server-side web applications, a connection pool is the standard way to maintain a “pool” of active database connections in memory which are reused across requests.

Connection pool is a bed rock for handling database connection. And if the database connection is full it can be messy at times.

> A common use case is allow the connection pool to gracefully recover when the database server has been restarted, and all previously established connections are no longer functional. There are two approaches to this.
>
> 1. Disconnet Handling - Pessimistic&#x20;
> 2. Disconnect Handling - Optimistic

1. **Pessimistic Disconnect Handling**

Let's look at how we can implement pessimistic disconnection in flask-sqlalchemy package. In config, all you need to set is two configurations. In flask setting configuration you will need to set just the following option:



```
    SQLALCHEMY_ENGINE_OPTIONS = {
        "pool_pre_ping": True,
        "pool_recycle": 300,
    }
```

> The pessimistic approach refers to emitting a test statement on the SQL connection at the start of each connection pool checkout, to test that the database connection is still viable. Typically, this is a simple statement like “SELECT 1”, but may also make use of some DBAPI-specific method to test the connection for liveness. The approach adds a small bit of overhead to the connection checkout process, however is otherwise the most simple and reliable approach to completely eliminating database errors due to stale pooled connections.\
> \
> The “pre ping” feature will normally emit SQL equivalent to “SELECT 1” each time a connection is checked out from the pool; if an error is raised that is detected as a “disconnect” situation, the connection will be immediately recycled, and all other pooled connections older than the current time are invalidated, so that the next time they are checked out, they will also be recycled before use.
>
> If the database is still not available when “pre ping” runs, then the initial connect will fail and the error for failure to connect will be propagated normally. In the uncommon situation that the database is available for connections, but is not able to respond to a “ping”, the “pre\_ping” will try up to three times before giving up, propagating the database error last received.

**2. Optimistic DB disconnection**\
****

> When pessimistic handling is not employed, as well as when the database is shutdown and/or restarted in the middle of a connection’s period of use within a transaction, the other approach to dealing with stale / closed connections is to let SQLAlchemy handle disconnects as they occur, at which point all connections in the pool are invalidated, meaning they are assumed to be stale and will be refreshed upon next checkout. This behavior assumes the [`Pool`](https://docs.sqlalchemy.org/en/14/core/pooling.html#sqlalchemy.pool.Pool) is used in conjunction with a [`Engine`](https://docs.sqlalchemy.org/en/14/core/connections.html#sqlalchemy.engine.Engine). The [`Engine`](https://docs.sqlalchemy.org/en/14/core/connections.html#sqlalchemy.engine.Engine) has logic which can detect disconnection events and refresh the pool automatically.\
> \
> &#x20;When the [`Connection`](https://docs.sqlalchemy.org/en/14/core/connections.html#sqlalchemy.engine.Connection) attempts to use a DBAPI connection, and an exception is raised that corresponds to a “disconnect” event, the connection is invalidated. The [`Connection`](https://docs.sqlalchemy.org/en/14/core/connections.html#sqlalchemy.engine.Connection) then calls the [`Pool.recreate()`](https://docs.sqlalchemy.org/en/14/core/pooling.html#sqlalchemy.pool.Pool.recreate) method, effectively invalidating all connections not currently checked out so that they are replaced with new ones upon next checkout. This flow is illustrated by the code example below:

```
from sqlalchemy import create_engine, exc
e = create_engine(...)
c = e.connect()

try:
    # suppose the database has been restarted.
    c.execute(text("SELECT * FROM table"))
    c.close()
except exc.DBAPIError, e:
    # an exception is raised, Connection is invalidated.
    if e.connection_invalidated:
        print("Connection was invalidated!")

# after the invalidate event, a new connection
# starts with a new Pool
c = e.connect()
c.execute(text("SELECT * FROM table"))
```
