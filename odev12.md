``` SQL 
1.  SELECT COUNT(*) FROM film
    WHERE length > 
    (SELECT MAX(length) FROM film);

2.  SELECT COUNT(*) FROM film
    WHERE rental_rate = 
    (SELECT MAX(rental_rate) FROM film);

3.  SELECT * FROM film
    WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) AND replacement_cost = (SELECT MIN(replacement_cost) FROM film);

4.  SELECT customer_id, first_name, last_name FROM customer
    WHERE customer_id = 
    (
    SELECT customer_id FROM payment
    GROUP BY customer_id
    HAVING  COUNT(customer_id) =

    (
    SELECT COUNT(customer_id) FROM payment
    GROUP BY customer_id
    LIMIT 1
    )

    );