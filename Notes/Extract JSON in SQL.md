---
title: Extract JSON in SQL
created: 2025-04-17
updated: 2025-04-17
description: 
aliases: 
---

A **JSON array** is _ordered by index_, starting at **0** — just like an array in most programming languages

To extract a nested value, using **mySQL**, such as a property of the *n*th object in a JSON array, we use  the `JSON_EXTRACT()` function with the path expression syntax:

```sql
JSON_EXTRACT(json_column, '$[n].property')
```

### Accessing Named Arrays in JSON Objects
If your JSON document contains multiple arrays under different keys, reference the key before indexing:

```sql
JSON_EXTRACT(json_column, '$.key[n].property')
```

#### Example: Parsing API JSON Response
Assume you store JSON responses from an external API in a column named `data_column`. An example response might look like:

```json
{
  "metrics": [
    {"value": 42},
    {"created": 2025-04-17}
  ],
  "users": [
    {"username": "alice"},
    {"email": "bob@example.com"}
  ]
}
```

To extract the first `value` from `metrics` (`n = 0`):

```sql
SELECT JSON_EXTRACT(data_column, '$.metrics[0].value') AS second_metric
FROM your_table;
```

To extract the first `username` from `users` (`n = 0`):

```sql
SELECT JSON_EXTRACT(data_column, '$.users[0].username') AS first_user
FROM your_table;
```

To extract the second `email` from `users` (`n = 1`):

```sql
SELECT JSON_EXTRACT(data_column, '$.users[1].email') AS second_user_email
FROM your_table;
```

### Notes
- `JSON_UNQUOTE()` can be used to remove quotation marks in MySQL if needed.
- Always tailor the path to the structure under each key, as different arrays may store different object types and properties.

---
## References

- [MySQL :: MySQL 8.4 Reference Manual :: 14.17.3 Functions That Search JSON Values](https://dev.mysql.com/doc/refman/8.4/en/json-search-functions.html#function_json-extract)