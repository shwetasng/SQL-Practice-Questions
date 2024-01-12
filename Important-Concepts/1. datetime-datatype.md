## datetime-datatype:

```
# USE OF datetime DATA TYPE

Create Database Practice;
USE Practice;

CREATE TABLE EXAMPLETABLE(
EventdateTime datetime
);

# Used to check the schema of the table
DESCRIBE EXAMPLETABLE;

INSERT INTO EXAMPLETABLE VALUES('2000-10-12 10:34:00'),('2001-11-29 11:23:00'),('2000-10-11 14:45:00');

SELECT * FROM EXAMPLETABLE;

# This is to select records from table after a specific date and time
SELECT * FROM ExampleTable WHERE EventDateTime > '2000-10-12 12:00:00';

# This is used to extract the year from EventDateTime column.
SELECT YEAR(EventdateTime) FROM EXAMPLETABLE;

SELECT DATEDIFF('2000-10-12','2001-12-12') AS DateDifference;
```
