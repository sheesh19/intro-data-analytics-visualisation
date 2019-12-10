# Intro to Data Analytics & Visualisations 


Download [Tableau Public for free](https://public.tableau.com/en-us/s/) for data visualisation. 

Resources to embed [Tableau Visualisations in a website](https://github.com/tableau/embedding-playbook/blob/master/pages/01_embedding_and_jsapi.md)


### Challenge 1 | SQL - DB Creation & Additional Students
1. Head to the [SQL Compiler](http://sqlfiddle.com/) and make sure the top tab has "MySQL 5.6".
2. In a new tab, up the [text file containing our practice database- meetup-db.txt](https://github.com/sheesh19/intro-data-analytics-visualisation/blob/master/meetup-db.txt).
3. Copy the text from the `meetup-db.txt` file and paste it on the left side of the SQL Compiler.
4. Press the "Build Schema" button to create the database.
5. Congratulations! You've built a database. 
6. Let's create a new row in the database. Underneath the following line (probably around line 50 in your SQL Compiler).

``` 
INSERT INTO students (first_name, profession, age, gender) 
VALUES ('Johnny', 'Marketer', 32, 'M');
```

Add in a new student to the database. The syntax should follow the above example. 
7. Make sure to rebuild the schema for the student to be added. 

### Challenge 2 | SQL - Returning data
1. Let's return all of the students. `SELECT` and `FROM` will be helpful. 
2. Next, return all of the meetups. 
3. Next, return all of the students who are female. Make sure to use `WHERE`. 
4. Refine your last query: return all of the students who are female- but only return their `first_name` and `profession`. 
5. Next, let's use `COUNT` and `GROUP BY` together. Return the number of students who have the same age. Make sure to `COUNT` the `students.age` column and `GROUP BY` `age` within the query. 

### Challenge 3 | Join Tables
1. Let's write a `JOIN` query. We need to join our tables together:

```
SELECT *
FROM meetups, students;
JOIN meetup_students ON meetups.id = meetup_students.meetup_id
JOIN students ON students.id = meetup_students.student_id;
```
2. Return only the `meetups.title` and the `students.first_name`.
3. Next, let's run a query to `COUNT` the number of students per each meetup. Remember to use `GROUP BY`. 

