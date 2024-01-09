## CREATE A DATABASE AND CREATE A TABLE IN IT
<pre>CREATE DATABASE college;
  
USE college;

CREATE TABLE student(
	rollno INT PRIMARY KEY,
    name VARCHAR(50),
    marks INT NOT NULL,
    grade VARCHAR(1),
    city VARCHAR(20)
);</pre>


## INSERT VALUES INSIDE THE TABLE
<pre>INSERT INTO student
(rollno, name, marks, grade, city)
VALUES
(101, "anil", 78, "C", "Pune"),
(102, "bhumika", 93, "A", "Mumbai"),
(103, "chetan", 85, "B", "Mumbai"),
(104, "dhruv", 96, "A", "Delhi"),
(105, "emanuel", 12, "F", "Delhi"),
(106, "farah", 82, "B", "Delhi");</pre>

## USE OF SELECT QUERY
<pre>SELECT * FROM student;</pre>
<img width="205" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/bab87cf3-adfd-4285-992d-dfb86f1155b4">
<pre>SELECT name, marks from student;</pre>
<img width="103" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/6fa111c1-3282-41d3-b801-5302cb1b314f">
<pre>SELECT DISTINCT city FROM student;</pre>
<img width="69" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/08db0ded-a330-46eb-b9ef-dcace5bab370">

## USE OF WHERE CLAUSE WITH SELECT QUERY
<pre>SELECT * FROM student 
WHERE marks>80;</pre>
<img width="201" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/b7ac2b71-4c5f-4a71-8867-cbca05b01065">

## USE OF OPERATORS IN WHERE CLAUSE
<pre>SELECT * FROM student 
WHERE marks>80 AND city="Mumbai";</pre>
<img width="199" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/a22120e5-4309-44af-a5ed-43870534aa5d">
<pre>SELECT * FROM student 
WHERE marks>80 OR city="Mumbai";
</pre>
<img width="202" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/bf3782a6-bac6-4f59-bd42-ebfbc324cc47">
<pre>SELECT * FROM student 
WHERE marks BETWEEN 80 AND 90;</pre>
<img width="197" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/1ceffbff-25a8-4827-86b7-789c3eb87928">
<pre>SELECT * FROM student 
WHERE city IN ("Pune", "Delhi");</pre>
<img width="193" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/1da3fc73-52fe-4566-b163-f1904fdd6a88">
<pre>SELECT * FROM student 
WHERE city NOT IN ("Mumbai", "Delhi");</pre>
<img width="183" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/4ee46339-d673-4149-bd62-5529f852979b">

## USE OF LIMIT CLAUSE
<pre>SELECT * FROM student
LIMIT 3;</pre>
![image](https://github.com/shwetasng/Coding-Practice/assets/103261868/5574cf09-b8b2-41fb-92c1-39c61ad2dce8)
<pre>SELECT * FROM student
WHERE marks>90
LIMIT 2;</pre>
<img width="203" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/4ae2ca16-ad26-41a3-b8a1-c6acdd6a1e39">

## USE OF ORDER BY CLAUSE

<pre>SELECT * FROM student
ORDER BY city
ASC;
</pre>
<img width="202" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/e2d08138-8069-4118-9e47-81ddfbbc10d3">
<pre>SELECT * FROM student
ORDER BY marks
DESC;</pre>
<img width="199" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/0c073f7d-36c6-4df5-964d-ac2529378285">

## USE OF AGGREGATE FUNCTIONS
<pre>SELECT MAX(marks)
FROM student;</pre>
<img width="79" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/fb25af8b-2f47-4f3f-9da4-3be484d9a8b9">
<pre>SELECT MIN(marks)
FROM student;</pre>
<img width="73" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/646647cd-cd20-49cf-9611-a2a7ae3aa76e">
<pre>SELECT AVG(marks)
FROM student;</pre>
<img width="82" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/296bb8f2-8c54-4c4f-9fc4-8212c629adb7">
<pre>SELECT COUNT(name)

FROM student;</pre><img width="89" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/67991655-9223-4873-a228-c895b3b765d3">


## USE OF GROUP BY CLAUSE
Groups rows that have the same values into summary rows. It collects data from multiple records and groups the result by one or more column.
<pre>SELECT city, COUNT(name)
FROM student 
GROUP BY city;</pre>
<img width="127" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/70f0eb41-aac6-43bd-a499-aa5ff3305b55">

<pre>SELECT city, AVG(marks)
FROM student 
GROUP BY city;</pre>
<img width="118" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/053af7c7-af61-42c8-8cce-f05252215861">

<pre>SELECT city, AVG(marks)
FROM student 
GROUP BY city
ORDER BY AVG(marks);</pre>
<img width="119" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/6ea644a3-2633-4683-ab80-2fb01afcda9e">

<pre>SELECT grade, COUNT(rollno)
FROM student
GROUP BY grade;</pre>
<img width="118" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/72667f19-6246-4e76-a7db-dabc23b496ae">

<pre>SELECT grade, COUNT(rollno)
FROM student
GROUP BY grade
ORDER BY grade;</pre>
<img width="122" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/ded4e653-022c-4d62-ba0d-860d23b03f0e">


## USE OF HAVING CLAUSE
Similar to Where Clause i.e., applies some condition on rows. Used when we want to apply any condition after grouping.

<pre>
SELECT city, count(rollno)
FROM student 
GROUP BY city
HAVING MAX(marks)>90;	
</pre>
<img width="122" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/1f080310-5829-49f3-949c-3d00f59332fd">

## GENERAL ORDER OF A SQL QUERY

<pre>
SELECT columns(s)
FROM table_name
WHERE condition              // WHERE puts condition on ROWS
GROUP BY columns(s)
HAVING condition	     // HAVING puts condition on GROUPS
ORDER BY column(s) ASC;
</pre>

Example:
<pre>
SELECT city
FROM student
WHERE grade="A"
GROUP BY city
HAVING MAX(marks)>=93
ORDER BY city DESC;
</pre>
<img width="64" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/fcd580c0-af48-4958-b552-70415927e791">


## USING UPDATE 
This is used to update existing rows
<pre>
UPDATE table_name
SET col1=val1, col2=val2
WHERE condition;
</pre>

<pre>UPDATE student
SET GRADE="O"
WHERE grade="A";</pre>
On running this query we get an error code:1175, which basically means that our SAFE MODE is turned on that restricts us from performing certain actions on tables.
We can turn this SAFE MODE off using SQL Query.

<pre>SET SQL_SAFE_UPDATES=0; // 0 means off and 1 means on.</pre>
Now table becomes,

<img width="206" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/a3ae578e-0a41-477d-ba26-5f577cb009dd">

<pre>UPDATE student
SET marks=marks+1;</pre>
<img width="201" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/78452386-28ba-4931-b3cc-a792ab41944b">

## USING DELETE
This is used to delete existing rows.

<pre>DELETE FROM table_name
WHERE condition;</pre>

<pre>DELETE FROM student
WHERE marks<30;</pre>
<img width="203" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/ac9902b9-faa4-49f7-bad9-f02c47bad073">


##  REVISITING FOREIGN KEYS

<pre>CREATE TABLE dept(
id INT PRIMARY KEY,
name VARCHAR(20)
);

CREATE TABLE teacher(
id INT PRIMARY KEY,
name VARCHAR(20),
dept_id INT,
FOREIGN KEY (dept_id) REFERENCES dept(id)
);</pre>
To visualize this in MySQL we will reverse engineer our database.

<img width="483" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/dac82d28-e54a-48b1-9763-ec18a5920623">
<img width="170" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/d57e4a99-c789-40b8-90be-b7b51373ae83">

we can clearly see how our two tables are related using Foreign key.

## CASCADING ON FOREIGN KEYS
This basically means if there is a change done in one table then it should be reflected in its related tables.
- ON DELETE CASCADE: when we create a FK using this option, it deletes the referencing rows in the child table when the referenced row is deleted in the parent table which has a primary key.
- ON UPDATE CASCASE: when we create a FK using this option, the referencing rows are updated in the child table when the referenced row is updated in the parent table which has a primary key.

<pre>CREATE TABLE student(
id INT PRIMARY KEY,
courseID INT,
FOREIGN KEY (courseID) REFERENCES cource(id)
ON DELETE CASCADE
ON UPDATE CASCADE
);</pre>

EXAMPLE:
So basically we have a FK dept_id in teachers table which is basically Primary Key of dept table named id...now what we do is update the id value in dept table and then check teacher table again so that change gets reflected there as well which basically tells that cascading is successful.

<img width="157" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/98b94e08-c635-4bcb-9baf-d10d411b1f11">
<img width="249" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/9673155f-84f9-4bd0-9b51-a331444c0649">

NOTE: always think about using cascading wherever Foreign Key is involved.

## TABLE RELATED QUERIES

1. Alter: to change the schema

** ADD COLUMN
<pre>
ALTER TABLE table_name
ADD COLUMN column_name datatype constraint;
</pre>


** DROP COLUMN
<pre>
ALTER TABLE table_name
DROP COLUMN column_name;
</pre>

** RENAME TABLE
<pre>
ALTER TABLE table_name
RENAME TO new_table_name;
</pre>

** CHANGE COLUMN(RENAME)
<pre>
ALTER TABLE table_name
CHANGE old_column_name new_column_name new_datatype new_constraint;
</pre>

** MODIFY COLUMN (MODIFY DATATYPE/CONSTRAINT)
<pre>
ALTER TABLE table_name
MODIFY col_name new_datatype new_constraint;
</pre>

EXAMPLE:

<img width="237" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/6028a39d-1edf-4e5c-902a-a16b071b08e8">
<pre>
ALTER TABLE student
ADD COLUMN age INT NOT NULL DEFAULT 19;
</pre>
<img width="245" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/ffac7252-df94-4519-835b-f4eb56a065f0">

<pre>
ALTER TABLE student
MODIFY COLUMN age VARCHAR(2);
</pre>

Now using this command will not reflect any error as such but when you try to add new entry into table and try to put age as 100 lets say then in that case there will be an error occurrence which will be that "Data too long for Columne age..."

<pre>
ALTER TABLE student 
CHANGE age stu_age INT;
</pre>

This will now again modify the "age" column to INT type but will also change its name to stu_age.

<img width="249" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/5e208095-e956-4f95-b728-0c7617023b8a">

<pre>
ALTER TABLE student
DROP COLUMN stu_age;
</pre>
<img width="219" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/d1071143-b8b3-44d7-bbaf-8664cc4ab1a4">

<pre>
ALTER TABLE student 
RENAME TO stu;
</pre>
<img width="148" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/a453db1e-d88c-49b2-bd51-8d4b71c1a396">


2. Truncate: to delete table's data

<pre>
TRUNCATE TABLE table_name;
</pre>

Difference b/w Truncate and Drop is that is Drop whole table is deleted whereas in Truncate only it's data is deleted.


## SQL JOINS

- Join is used to combine rows from two or more tables, based on a related column between them.

1. Inner Joins: returns records that have matching values in both the tables.

SYNTAX:
<pre>
SELECT column(s)
FROM tableA
INNER JOIN tableB
ON tableA.col_name=tableB.col_name;
</pre>
NOTE: In this we can replace tableA with tableB and no change occurs.

EXAMPLE:

<img width="113" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/a98ae268-4c9e-4a96-86e7-0dfc2a1df563">
<img width="120" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/9c6196a1-8ba3-4e60-afe3-2937d5fdac66">

Now applying Inner Join on this:

<pre>
SELECT * 
FROM student
INNER JOIN courses
ON student.student_id=courses.student_id;
</pre>

<img width="205" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/2a04014a-6583-4357-b079-85c309a3092a">

** Aliases: alternative name- these are used when table names are big for repeated use hence these short names can be given to tables and then used.

2. Left Join: Returns all the records from the left table and matched records from the right table.

SYNTAX:
<pre>
SELECT column(s)
FROM table_left
LEFT JOIN table_right
ON table_left.col_name=table_right.col_name;
</pre>

Applying on the last example onle we get
<pre>
SELECT *
FROM student
LEFT JOIN courses
ON student.student_id=courses.student_id;
</pre>

<img width="208" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/e8e3569f-d992-4764-8ffc-ccdd120588e4">


3. Right Join: Returns all records from the right table and the matched records from the left table.

SYNTAX:
<pre>
SELECT *
FROM tableA
RIGHT JOIN tableB
ON tableA.col_name=tableB.col_name;	
</pre>

Applying on the last example:

<img width="397" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/d02f4ece-52ee-4e88-a03b-9bad81664dfb">
<img width="321" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/a96f523d-3610-4c9b-8916-1de93720b9cc">


4. FULL JOIN: Returns all records when there is a match in either left or right table.
   - So there is no such concept of FULL JOIN in MySql hence we use UNION for this purpose i.e.,
     <pre>
     Left Join
     UNION
     Right Join
     </pre>

<pre>
SELECT * FROM student as a
LEFT JOIN courses as b
ON a.student_id=b.student_id
UNION
SELECT * FROM student as a
RIGHT JOIN courses as b
ON a.student_id=b.student_id;
</pre>

<img width="211" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/ccb937df-fc9b-45fe-aaaa-b659fed818d3">


5. Left exclusive join: In this only the data of left table is returned and not the common data of left and right table.

For doing this we just put a condition on Left Join in which table.col data from right table is null.

Applying on above example:
<pre>
SELECT *
FROM student
LEFT JOIN courses
ON student.student_id=courses.student_id
WHERE courses.student_id IS NULL;
</pre>
<img width="207" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/b54d89e5-018a-43d7-86bc-1ce4a1dc910f">


6. Right exclusive join: In this only the data from the right table is returned and not the common data from the left and right table.

For doing this we simply just put a condition in Right join in which table.col data from the left table is null.

Applying on above example:
<pre>
SELECT *
FROM student
RIGHT JOIN courses
ON student.student_id=courses.student_id
WHERE student.student_id IS NULL;
</pre>
<img width="204" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/75dfbe22-549f-4ae0-bf50-fa960e4d794a">

7. Full exclusive Join: In this only the data of full outer join is returned excluding the common data between two tables

Applying on above example:
<pre>
SELECT * FROM student as a
LEFT JOIN courses as b
ON a.student_id=b.student_id
WHERE b.student_id IS NULL
UNION
SELECT * FROM student as a
RIGHT JOIN courses as b
ON a.student_id=b.student_id
WHERE a.student_id IS NULL;
</pre>
<img width="207" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/38616d20-38a9-41bf-bb81-1effc759ee86">

8. Self Join: It is a regular join where the table is joined with itself.

- It is used is special cases such as when in a table emplyee id and that employee's manager id is given but not explicitly mentioned which employee is manager of which employee . To get such info we use self joins
- Let us understand with an example:

	<img width="194" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/334c5aa7-db30-4c3a-81e3-74fc6ae25a2a">
 	<img width="330" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/5c186d78-4b7d-44c6-bbc7-86c96aae42d4">
	<img width="197" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/d764be2d-cf60-4068-b227-ce60deb74812">
	<img width="292" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/9d6adb73-b9dd-41be-b488-f8aa3c0e56aa">
## UNION
- it is used to combine the result set of two or more SELECT statements. It gives Unique records.
- TO USE IT:
  	- every SELECT should have same number of columns
  	- columns must have similar data types.
  	- columns in every SELECT should be in same order.

  SYNTAX:
<pre>
SELECT column(s) FROM tableA
UNION
SELECT column(s) FROM tableB
</pre>
<img width="249" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/0a70df77-e57e-4d98-bb2f-605c45b09862">


### UNION ALL: 
- just like UNION this also combines the result set of two or more SELECT statements but this gives all the duplicate values.
<img width="239" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/6e2c10d6-1508-408b-b161-7a3cbd2c1651">

## SQL SUB-QUERIES

- A subquery or inner query or nested query is a query within another SQL query.
- it involves 2 SELECT statements and can be written in 3 ways i.e., either i) inside SELECT ii) Or Inside FROM iii) Or Inside WHERE--> this is mostly used.

SYNTAX for when written inside WHERE clause:
<pre>
SELECT column(s)
FROM table_name
WHERE col_name Operator
(SUBQUERY);
</pre>

Example1:

<img width="573" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/9fac2b8f-88c3-4b25-a5a8-509f1edc2768">

To solve this the query is:
<pre>
SELECT name, marks
FROM student
WHERE marks>(SELECT AVG(marks) FROM student);
</pre>

Example2:

<img width="582" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/869992a9-fab6-4b3d-9bd2-8b582c7515a9">

To solve this the query is: 
<pre>
SELECT name, rollno
FROM student
WHERE rollno IN (
	SELECT rollno
	FROM student
	WHERE rollno % 2 = 0
	);
</pre>

Example3:

<img width="604" alt="image" src="https://github.com/shwetasng/Coding-Practice/assets/103261868/79530643-6d18-4b32-bd71-7b495293a11e">

To solve this the query is:
<pre>
SELECT MAX(marks)
FROM(SELECT * FROM student WHERE city="Delhi") AS temp;
</pre>
NOTE: we use alias like "temp" in the FROM statement.

## MYSQL Views
- A view is a virtual table based on the result-set of an SQL statement.

SYNTAX:
<pre>
CREATE VIEW view1 AS
SELECT rollno, name FROM student;

SELECT * FROM view1;
</pre>

Note: A view always shows up-to-date data. The database engine recreates the view, every time a user queries it.
