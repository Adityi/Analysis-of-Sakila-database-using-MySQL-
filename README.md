# Analysis-of-Sakila-database-using-MySQL-
This included using various queries for exploring sakila database and creating stored procedures and stored functions.

## The queries are created to solve varius questions like:
1) What are the names of all the languages in the database (sorted alphabetically)?
2) Return the full names (first and last) of actors with “SON” in their last name, ordered by their first name.
3) Return the first and last names of actors who played in a film involving a “Crocodile” and a “Shark”, along with the release year of the movie, sorted by the actors’ last names.
4) How many films involve a “Crocodile” and a “Shark”?
5) Find all the film categories in which there are between 55 and 65 films. Return the names of these categories and the number of films per category, sorted by the number of films.
6) In how many film categories is the average difference between the film replacement cost and the rental rate larger than 17?
7) Find the names (first and last) of all the actors and costumers whose first name is the same as the first name of the actor with ID 8. Do not return the actor with ID 8 himself.
8) The top 5 categories which had the most average rental rate, with average (rounde to 2 digits)
9) Can we know how many distinct users have rented each genre?
10) Most demanded genres with total sales (top 5)
11) List the total amount paid by each customer, display top 5 customers.
12) You want to run an email marketing campaign in Canada, for which you will need the names and email addresses of all Canadian customers.
13) Sales have been lagging among young families, and you wish to target all family movies for a promotion. Identify all movies categorized as family films.
14) Display the most frequently rented movies in descending order.
15) Write a query to display how much business, in dollars, each store brought in.
16) Create view for top 5 movies
17) In which countries do Rent A Film have a presence in and what is the customer base in each country? What are the total sales in each country?
18) Count total number of films which were returned on time, late and early.
19) Category wise distribution of movies rental duration
20) Average rental duration of movies based on category

## So far I jhave created 3 stored procedures to ans:

1) Create a stored procedure to get the category of a movie.
2) Create a stored procedure to get total rentals and average sales for a customer, aslo the category as <100 = Silver, between 100 and 150 = Gold, and above 150 as Platinum.
3) A stored procedure to find total rentals and sales of a film using film_id.



