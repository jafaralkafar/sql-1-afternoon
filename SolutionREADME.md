TABLE PERSON
1. CREATE TABLE person (
    person_id SERIAL,
    name VARCHAR,
    age INTEGER,
    height INTEGER,
    city VARCHAR,
    favorite_color VARCHAR
);
2. INSERT INTO person ( name, age, height, city, favorite_color ) VALUES 
    ('Grant', 38, 190, 'Apple Valley', 'green'),
    ('Bob', 29, 160, 'Provo', 'blue'),
    ('Billy', 25, 175, 'Lehi', 'yellow'),
    ('Ceri', 40, 165, 'Lubbock', 'yellow'),
    ('Brie', 44, 160, 'Morocco', 'pink');
3. SELECT * FROM person ORDER BY height DESC;
4. SELECT * FROM person ORDER BY height;
5. SELECT * FROM person ORDER BY age DESC;
6. SELECT * FROM person WHERE age > 20;
7. SELECT * FROM person WHERE age = 18;
8. SELECT * FROM person WHERE age < 20 OR age > 30;
9. SELECT * FROM person WHERE age <> 27;
10. SELECT * FROM person WHERE favorite_color <> 'red';
11. SELECT * FROM person WHERE favorite_color <> 'red' OR favorite_color <> 'blue';
12. SELECT * FROM person WHERE favorite_color = 'green' OR favorite_color = 'orange';
13. SELECT * FROM person WHERE favorite_color IN ('green', 'orange', 'blue');
14. SELECT * FROM person WHERE favorite_color IN ('yellow', 'purple')

TABLE ORDERS
1. CREATE TABLE orders (
    person_id SERIAL,
    product_name VARCHAR,
    product_price NUMERIC,
    quantity INTEGER
);
2. INSERT INTO orders ( person_id, product_name, product_price, quantity) VALUES 
    ( 0, 'Rice', 16.50, 2),
    ( 1, 'Beans', 7.50, 3),
    ( 0, 'Tortillas', 22.99, 6),
    ( 1, 'Steak', 35.99, 6),
    ( 2, 'Burritos', 7.99, 4);
3. SELECT * FROM orders;
4. SELECT SUM(quantity) FROM orders;
5. SELECT SUM(product_price * quantity) FROM orders;
6. SELECT SUM(product_price * quantity) FROM orders WHERE person_id = 0;

TABLE ARTIST
1. INSERT INTO artist ( name ) VALUES
    ( 'Beck' ),
    ( 'Bob Ross' ),
    ( 'John Flansburgh' );
2. SELECT * FROM artist ORDER BY name DESC LIMIT 10;
3. SELECT * FROM artist ORDER BY name LIMIT 5;
4. SELECT * FROM artist WHERE name LIKE 'Black%'
5. SELECT * FROM artist WHERE name LIKE '%Black%'

TABLE EMPLOYEE
1. SELECT first_name, last_name FROM employee WHERE city = 'Calgary';
2. SELECT MAX(birth_date) FROM employee;
3. SELECT MIN(birth_date) FROM employee;
4. SELECT employee_id FROM employee WHERE first_name LIKE '%Nancy%';
   SELECT * FROM employee WHERE reports_to = 2;
5. SELECT COUNT(*) FROM employee WHERE city = 'Lethbridge';

TABLE INVOICE
1. SELECT COUNT(*) FROM invoice WHERE billing_country = 'USA';
2. SELECT MAX(total) FROM invoice;
3. SELECT MIN(total) FROM invoice;
4. SELECT * FROM invoice WHERE total > 5;
5. SELECT COUNT(*) FROM invoice WHERE total < 5;
6. SELECT COUNT(*) FROM invoice WHERE billing_state IN ('CA', 'TX', 'AZ');
7. SELECT AVG(total) FROM invoice;
8. SELECT SUM(total) FROM invoice;