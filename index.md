SQL Lesson 1: SELECT queries 101
Exercise 1 — Tasks
1.Find the title of each film 
SELECT title FROM movies;

2.Find the director of each film
SELECT 	Director FROM movies;

3.Find the title and director of each film
SELECT Title, Director FROM movies;

4.Find the title and year of each film
SELECT Title, Year FROM movies;

5.Find all the information about each film
SELECT * FROM movies;
=======================================================
//SQL Lesson 2: Queries with constraints (Pt. 1)
Exercise 2 — Tasks
1.Find the movie with a row id of 6 
SELECT Id, Title FROM movies WHERE Id =6;

2.Find the movies released in the years between 2000 and 2010
SELECT Title FROM movies WHERE Year BETWEEN 2000 AND 2010;

3.Find the movies not released in the years between 2000 and 2010
SELECT Title FROM movies WHERE Year NOT BETWEEN 2000 AND 2010;

4.Find the first 5 Pixar movies and their release year
SELECT title, year FROM movies WHERE year <= 2003;
======================================================

SQL Lesson 3: Queries with constraints (Pt. 2)
Exercise 3 — Tasks
1.Find all the Toy Story movies
SELECT Title FROM movies WHERE Title LIKE "Toy Story%";

2.Find all the movies directed by John Lasseter
SELECT Title, Director FROM movies WHERE Director LIKE "John Lasseter";
SELECT Title, Director FROM movies WHERE Director NOT LIKE "John Lasseter";
SELECT Title, Director FROM movies WHERE Director NOT LIKE "John Lasseter";

3.Find all the movies (and director) not directed by John Lasseter

4.Find all the WALL-* movies
SELECT * FROM movies WHERE title LIKE "WALL-_"
======================================================

SQL Lesson 4: Filtering and sorting Query results

1.List all directors of Pixar movies (alphabetically), without duplicates
SELECT DISTINCT director FROM movies ORDER BY director ASC;

2.List the last four Pixar movies released (ordered from most recent to least)
SELECT title, year FROM movies ORDER BY year DESC LIMIT 4;

3.List the first five Pixar movies sorted alphabetically
SELECT title FROM movies ORDER BY title ASC LIMIT 5;

4.List the next five Pixar movies sorted alphabetically
SELECT title FROM movies ORDER BY title ASC LIMIT 5 OFFSET 5;