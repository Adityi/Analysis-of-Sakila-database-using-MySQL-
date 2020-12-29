## Sakila-database-using-SQL-
##start using Sakila database
use sakila;

Display first and last names of all actors
select first_name, last_name
from actor;

What are the names of all the languages in the database (sorted alphabetically)?

select distinct name
from language
order by 1;

# Return the full names (first and last) of actors with “SON” in their last name, ordered by their first
name.

select concat(first_name ," ", last_name) full_name
from actor
where last_name like "%son%"
order by first_name;

# Return the first and last names of actors who played in a film involving a “Crocodile” and a “Shark”,
along with the release year of the movie, sorted by the actors’ last names.

select first_name, last_name, release_year
from actor
join film_actor using(actor_id)
join film using(film_id)
join film_text using(film_id)
where film_id in (select film_id
from film_text
where description like "%shark%" and description like "%crocodile%")
order by 2;

# How many films involve a “Crocodile” and a “Shark”?

select count(distinct(film_id))
from film_text
where description like "%shark%" and  description like "%crocodile%";

ans = 10

# Find all the film categories in which there are between 55 and 65 films. Return the names of these
categories and the number of films per category, sorted by the number of films.

select name, count(*)number_of_films
from category
join film_category
using(category_id)
group by category.category_id
having number_of_films between 55 and 65
order by 2;

# In how many film categories is the average difference between the film replacement cost and the
rental rate larger than 17?

select count(*) as cat_count
from (select category_id
from film
join film_category
using(film_id)
group by category_id
having avg(abs(rental_rate - replacement_cost))>17) temp

ans = 8

# Find the names (first and last) of all the actors and costumers whose first name is the same as the
first name of the actor with ID 8. Do not return the actor with ID 8 himself.

select a.first_name actor_firstname, a.last_name actor_lastname, c.first_name customer_firstname, c.last_name customer_lastname
from actor a
join customer c
on a.first_name = c.first_name
where a.first_name  in (select first_name from actor where actor_id  = "8") and actor_id<>8

# The top 5 categories which had the most average rental rate, with average (rounde to 2 digits)

select category.name, avg(rental_rate) average
from film
join film_category
using(film_id)
join category
using(category_id)
group by category.name
order by average 
limit 5;









