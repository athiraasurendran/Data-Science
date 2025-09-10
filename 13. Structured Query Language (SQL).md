# SQL JOIN
## Join and Natural Join
- combine data in mutiple tables
    For example 
    TableA
    ID  Name
    1   Alice
    2   Bob
    3   Charlie

    TableB
    ID  Course
    2   Math
    3   Science
    4   History


- INNER JOIN Example
    SELECT A.ID, A.name, B.course
    FROM TableA A
    INNER JOIN TableB B
    ON A.ID=B.ID

    ID  Name     Course
    2   Bob      Math
    3   Charlie  Science


- LEFT JOIN Example
    SELECT A.ID, A.name, B.course
    FROM TableA A
    LEFT JOIN TableB B
    ON A.ID=B.ID

    ID  Name     Course
    1   Alice    Null
    2   Bob      Math
    3   Charlie  Science


- RIGHT JOIN Example
    SELECT A.ID, A.name, B.course
    FROM TableA A
    RIGHT JOIN TableB B
    ON A.ID=B.ID

    ID  Name     Course
    2   Bob      Math
    3   Charlie  Science
    4   Null     History


- FULL OUTER JOIN Example
    SELECT A.ID, A.name, B.course
    FROM TableA A
    FULL OUTER JOIN TableB B
    ON A.ID=B.ID

    ID  Name     Course
    1   Alice    Null
    2   Bob      Math
    3   Charlie  Science
    4   Null     History



- Natural JOIN Example
    SELECT *
    FROM TableA
    NATURAL JOIN TableB;


SELECT m.name, g.genre
FROM movies m
JOIN movie_genre g
ON m.id=g.movie_id
LIMIT 20;

    - here m and g are table alises
    - Natural join: a join where the same column-names across two tables
    - T1: C1, C2
    - T2: C1, C3, C4
    - SELECT * FROM T1 JOIN T2;
    - SELCECT * FROM T1 JOIN T2 USING (C1);
    - returns C1, C2, C3, C4
    - no need to use the keyword "ON"

Practice with Hacker Rank

Sub-Queries or Nested Queris or Inner Queries
    - First inner query is executed then outer query is executed

SELECT actor_id FROM roles WHERE movie_id IN
(SELECT id FROM movies where name='Schindler's List')

IN, NOT IN, EXISTS, NOT EXISTS, ANY, ALL, Comparison operators
    - ANY operator retuns TRUE if any of the subquery values meet the condition
    - ALL operator returns TRUE if all of the subquery values meet the condition

    - e.g. SELECT * FROM movies WHERE rankscore>= ALL (SELECT MAX(rankscore) FROM movies);


## CREATE, READ, UPDATE, DELETE (CRUD)

CREATE
    - CREATE TABLE table_name (
    col1 col1_dtype,
    col2 col2_dtype,
    );

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    grade CHAR(1)
);



## INSERT

- INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7);

- INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7),
                                                        (412322, 'Iron Man', 2008, 7.9),
                                                        (412323, 'Iron Man 2', 2010, 7);
- INSERT INTO students (id, name, age, grade) 
    VALUES (1, 'John Doe', 20, 'A');
    
- INSERT INTO students (id, name, age, grade) 
    VALUES 
        (2, 'Jane Smith', 22, 'B'),
        (3, 'Mark Brown', 19, 'A');


## UPDATE

- UPDATE <TableName> SET col1=val1, col2=val2 WHERE condition;
- UPDATE movies SET rankscore=9 where id=412321;
- Can be used to update multiple rows at once

- UPDATE students 
    SET grade = 'A+' 
    WHERE id = 2;

- UPDATE students 
    SET age = 21, grade = 'B+' 
    WHERE name = 'Mark Brown';

## ALTER: The ALTER TABLE statement is used to modify the structure of the table.
- Adding new columns
    - ALTER TABLE students 
        ADD email VARCHAR(100);
- Rename column
    - ALTER TABLE students 
        RENAME COLUMN grade TO final_grade;

## DELETE
- DELETE FROM movies WHERE id=412321


## DROP
- Deletes both tableand all of the data permanently
- DROP TABLE Tablename;
- DROP TABLE tablename IF EXISTS;

## TRUNCATE
- TRUNCATE delete the contents of the table but the not the table
- where as DROP deletes the whole table itself
- TRUNCATE TABLE tablename; 
