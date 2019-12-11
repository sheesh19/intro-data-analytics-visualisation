# Intro to Data Analytics & Visualisations 

- [Slide Deck from today](https://bit.ly/38nMPBo)

- [SQL Compiler](https://www.db-fiddle.com/)

- Download [Tableau Public for free](https://public.tableau.com/en-us/s/) for data visualisation. 

- Resources to embed [Tableau Visualisations in a website](https://github.com/tableau/embedding-playbook/blob/master/pages/01_embedding_and_jsapi.md)



### Challenge 1 | SQL - DB Creation & Additional Students
1. Head to the [SQL Compiler](https://www.db-fiddle.com/) and make sure the top tab has "MySQL 5.7".
2. In a new tab, up the [text file containing our practice database- meetup-db.txt](https://github.com/sheesh19/intro-data-analytics-visualisation/blob/master/meetup-db.txt).
3. Copy the text from the `meetup-db.txt` file and paste it on the left side of the SQL Compiler.
4. Press the "Run" button to create the database.
5. Congratulations! You've built a database. 
6. Let's create a new row in the database. Underneath the following line (probably around line 50 in your SQL Compiler).

``` 
INSERT INTO students (first_name, profession, age, gender) 
VALUES ('Johnny', 'Marketer', 32, 'M');
```

Add in a new student to the database. The syntax should follow the above example. 
7. Make sure to run the query for the student to be added. 

### Challenge 2 | SQL - Returning data
1. Let's return all of the students. `SELECT` and `FROM` will be helpful. 
2. Next, return all of the meetups. 
3. Next, return all of the students who are female. Make sure to use `WHERE`. 
4. Refine your last query: return all of the students who are female- but only return their `first_name` and `profession`. 
5. Next, let's use `COUNT` and `GROUP BY` together. Return the number of students who have the same age. Make sure to `COUNT` the `students.age` column and `GROUP BY` `age` within the query. 

### Challenge 3 | Join Tables - Advanced
1. Let's write a `JOIN` query. We need to join our tables together:

```
SELECT *
FROM meetups
JOIN meetup_students
	ON meetups.id = meetup_students.meetup_id
JOIN students
	ON meetup_students.student_id = students.id;

```
2. Return only the `meetups.title` and the `students.first_name`.
3. Next, let's run a query to `COUNT` the number of students per each meetup. Remember to use `GROUP BY`. 

```
SELECT meetups.title, COUNT(meetup_students.student_id)
FROM meetups
JOIN meetup_students ON meetups.id = meetup_students.meetup_id
GROUP BY meetups.title;
```

### Challenge 4 | Tableau 
1. Download [Tableau Public](https://public.tableau.com/en-us/s/). 
2. Open up Tableau Public on your laptop. 
3. Import an excel spreadsheet or connect to a Google Sheet. 
4. Create a custom visualisation:
- Try to drag different `Dimensions` & `Measures` into the `Columns` & `Rows` at the top of your view. 
- Once you're ready, at the bottom of the Tableau view there should be an icon that lets you Create a New Dashboard. 
- Open the new dashboard, and drag your visualisation from the sidebar on the left of your screen under `Sheets`. 
5. You're ready to publish! Click on `File`at the top of the navbar & click `Save to Tableau Public As...`. This will let you post your visualisation on the Public Tableau Server- and will let share the link or embed it in a website. Saving this should open your Tableau Visualisation in a new tab in your browser. 
6. Congratulations! You have a live data visualisation. 


### Challenge 5 | Tableau - Share It
1. Once your visualisation is on Tableau Public's Server, in your broswer scroll to the bottom of your visualisation. There should be an icon with three bubbles connected by lines. Click on this icon. 
2. You'll see a pop-up window with two fields. The `Link` you can copy directly and share with others. Please note: if there is an error sharing, they may need to also have a Tableau Public account. 

3. IF you would like to embed the visualisation in a website, the pop-up window has an `Embed Code` option. Copy this. 
4. If you are starting a fresh website, you can create an `index.html` file. Within your `<body>` tags, post the text from the `Embed Code` option. That should be everything you need. 

In your `index.html` it should look similar to this:
```
<html>
<body>
   -- paste the text from the Embed Code field -- 

</body>
</html>
```
5. Open your `index.html` file in a browser- your visualisation should be there! 

### Challenge 6 | Google Analytics - Getting Started 
1. Sign up for Google Analytics. 
2. Create an Account. 
3. Create a Property. 
4. Click `Admin` at the bottom left of your page. Once there, under `Property`, click `Data Streams`.
5. Under `Data Streams` in the right pane, you should see an option to add a Web/your website.
6. Once completed, you'll see a bar with your website information. Click this. 
7. A new window will open, and you'll see `Tagging Instructions` part way down. 
8. Expand the `Global Site Tag (gtag.js)` tab. 
9. In the expanded area under `Global Site Tag (gtag.js)`, copy the code. 
10. Paste this code into the `<head>` of your main HTML page/`index.html`. 
11. It will look similar to this: 
```
<html>
<head>
	-- Your pasted Google Analytics Tag scripts --
</head>
</html>
```
12. Congratulations! Now you can track how your users are interacting with your app. 





#### Further Resources: 

- [Tableau Videos](https://www.tableau.com/learn/training)
- [Tableau Documentation](https://www.tableau.com/support/knowledgebase)

- [SQL Documentation + Examples](https://www.w3schools.com/sql/)
- [SQL Online Exercises](https://www.codecademy.com/catalog/language/sql)

- [Google Analytics Documentation- Set up Analytics Tag](https://support.google.com/analytics/answer/1008080)
- [Google Analytics Help Center + Documentation](https://support.google.com/analytics/?hl=en#topic=3544906)


If you need any help, feel free to reach out to me at:

[LinkedIn](https://www.linkedin.com/in/sheilaleveille/)
[Personal Website](www.sheilaleveille.com)

The [Slide Deck](https://bit.ly/38nMPBo) from today. 
