# What is difference with JSON documents in postgres and Mongodb

Mongodb under the hood actually stores the data not in JSON format, but in BSON(which is more efficient in terms of memory and stores the type as well).

While in postgres, what is actually happening under the hood is it's actually a string stored in JSON document. And any SQL engine is actually storing the data and parsing with a JSON parser, but is not internally stored actually as JSON.

So this makes Mongodb approach more faster, scalable when working with JSON or any unrepresented form of data than using postgres databases.
