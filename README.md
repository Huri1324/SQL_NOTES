# 01. Truncate 
TRUNCATE
-- TRUNCATE removes all rows from a table.
-- It cannot be used with a WHERE condition.
-- In SQL Server, it resets the IDENTITY counter
-- to the table's seed value.

TRUNCATE TABLE Products
----------------------------------------------
TRUNCATE vs DELETE

DELETE:
- Removes rows
- Can use WHERE
- Identity value is not automatically reset

TRUNCATE:
- Removes all rows
- Cannot use WHERE
- Resets IDENTITY counter in SQL Server

Example:
*/

DELETE FROM Products;

-- Reset identity counter
DBCC CHECKIDENT ('Products', RESEED, 0);

-- Alternative:
TRUNCATE TABLE Products;
