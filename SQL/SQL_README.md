#### 10. Explain Primary Key vs. Foreign Key in databases.
Answer: A primary key is a unique identifier for a record in a table, ensuring that no two rows have the same key. A foreign key is a field (or a collection of fields) in one table that uniquely identifies a row of another table, establishing a relationship between the two tables.
11. What’s the difference between the HAVING and WHERE clauses in SQL?
Answer: The WHERE clause is used to filter rows before any groupings are made, while the HAVING clause is used to filter groups after the GROUP BY operation has been performed. WHERE applies to individual rows, and HAVING applies to aggregated data.
#### 12. Explain different types of JOIN commands in SQL.
Answer:
INNER JOIN: Returns records that have matching values in both tables.
LEFT JOIN (or LEFT OUTER JOIN): Returns all records from the left table and the matched records from the right table; returns NULL for unmatched records in the right table.
RIGHT JOIN (or RIGHT OUTER JOIN): Returns all records from the right table and the matched records from the left table; returns NULL for unmatched records in the left table.
FULL JOIN (or FULL OUTER JOIN): Returns records when there is a match in either left or right table; returns NULL where there is no match.
#### 13. What’s the difference between DROP, TRUNCATE, and DELETE in SQL?
Answer:
DROP: Permanently removes a table or database from the database system.
TRUNCATE: Removes all rows from a table without logging individual row deletions, but retains the table structure for future use.
DELETE: Removes specific rows from a table based on a condition, with changes logged, allowing for potential rollback.
