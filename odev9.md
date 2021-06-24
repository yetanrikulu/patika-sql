 
``` SQL 
 1. SELECT city , country FROM country
    INNER JOIN city ON country.country_id = city.country_id;

 2. SELECT payment_id, first_name, last_name FROM payment
    INNER JOIN customer ON customer.customer_id = payment.customer_id;

 3. SELECT rental_id, first_name, last_name FROM customer 
    INNER JOIN rental ON customer.customer_id = rental.customer_id;
