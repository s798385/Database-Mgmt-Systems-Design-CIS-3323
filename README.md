# Database Mgmt Systems Design (CIS-3323)
The repository contains scripts for creating three example database.

## Battleships Database
This World War II capital ships database has the following schema:

* **Ships(name, class, launched):** This relation records the name of the ship, the name of its class, and the year in which the ship was launched. Ships are built in "classes" from the same design, and the class is usually named for the first ship of that class.
* **Classes(class, type, country, numGuns, bore, displacement):** This relation records the name of the class, the type ('bb' for battleship and 'bc' for battlecruiser), the country that built the ship, the number of main guns, the bore (diameter of the gun barrel, in inches) of the main guns, and the displacement (weight, in tons).
* **Battles(name, date):** This relation gives the name and date of battles.
* **Outcomes(ship, battle, result):** This relation gives the result (sunk, damaged, or ok) for each ship in each battle.

## Social Database
Students at your hometown high school have decided to organize their social network using databases. So far, they have collected information about sixteen students in four grades, 9-12. Here's the schema:

* **Highschooler ( ID, name, grade ):** there is a high school student with unique ID and a given first name in a certain grade.
* **Friend ( ID1, ID2 ):** the student with ID1 is friends with the student with ID2. Friendship is mutual, so if `(123, 456)` is in the Friend table, so is `(456, 123)`.
* **Likes ( ID1, ID2 ):** the student with ID1 likes the student with ID2. Liking someone is not necessarily mutual, so if `(123, 456)` is in the Likes table, there is no guarantee that `(456, 123)` is also present.

## Movies Database
* **Movie (mID, title, year, director ):** there is a movie with ID number mID, a title, a release year, and a director. 
* **Reviewer (rID, name ):** the reviewer with ID number rID has a certain name. 
* **Rating ( rID, mID, stars, ratingDate ):** the reviewer rID gave the movie mID a number of stars rating (1-5) on a certain ratingDate. 

<img src="https://github.com/s798385/Database-Mgmt-Systems-Design-CIS-3323/blob/main/Images/movies_db.png">

The following graph shows the various connections between the students in our database. 9th graders are blue, 10th graders are green, 11th graders are yellow, and 12th graders are purple. Undirected black edges indicate friendships, and directed red edges indicate that one student likes another student.

<img src="https://github.com/sbunivedu/db_example_database/blob/master/images/social.png">

## How to Experiment
Got to https://sqliteonline.com/ and click on "Click to connect" under "MariaDB". Select a script (`.sql` file) you want and copy-paste the content to the "script tab" on https://sqliteonline.com/. Click on the "Run" button to execute the script, which creates and populates the example database. Then, you can open another "script tab" to run SQL queries on this database.
