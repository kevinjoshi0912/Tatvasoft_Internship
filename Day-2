CREATE TABLE student (
   student_id serial PRIMARY KEY,
   first_name character varying(100) NOT NULL,
   last_name character varying(100) NOT NULL,
   email character varying(255) UNIQUE NOT NULL
);

INSERT INTO student(first_name, last_name, email )
	VALUES 
('Kartik','Nayani','kartik@gmail.com'),
('Akash','Bhutka','akash@gmail.com'),
('Dhruvit','Gadhiya','dhruvit@gmail.com'),
('Sunny','Vagadiya','sunny@gmail.com'),
('d2','d','d2d@gmail.com');


-- Select Statement
SELECT * FROM student where student_id = 1;

-- Update Statement
UPDATE student
SET first_name='Radhe',
last_name='Karna', 
email='karna@gmail.com'
WHERE student_id = 2;


-- Delete Statement
DELETE FROM student
WHERE student_id = 6;

-- sort
SELECT
	first_name,
	last_name
FROM
	student
ORDER BY
	first_name ASC;



SELECT
       first_name,
       last_name
FROM
       student
ORDER BY
       last_name DESC;


--filter
SELECT
	first_name,
	last_name
FROM
	student
WHERE
	first_name = 'Akshay';


SELECT
	first_name,
    last_name
FROM
	student
WHERE
	first_name LIKE '%u%';



--new table
CREATE TABLE order1 (
    order_id SERIAL PRIMARY KEY,
    student_id INTEGER NOT NULL REFERENCES student(student_id),
    order_date timestamp with time zone NOT NULL DEFAULT now(),
    order_number CHARACTER VARYING(50) NOT NULL,
    order_amount DECIMAL(10,2) NOT NULL
);


-- insert into the order
INSERT INTO order1 (student_id, order_date, order_number, order_amount) VALUES
  (1, '2024-01-01', 'ORD001', 50.00),
  (2, '2024-01-01', 'ORD002', 35.75),
  (3, '2024-01-01', 'ORD003', 100.00),
  (4, '2024-01-01', 'ORD004', 30.25),
  (5, '2024-01-01', 'ORD005', 90.75),
  (1, '2024-01-02', 'ORD011', 55.00),
  (1, '2024-01-03', 'ORD012', 80.25),
  (2, '2024-01-03', 'ORD013', 70.00),
  (3, '2024-01-04', 'ORD014', 45.00),
  (1, '2024-01-05', 'ORD015', 95.50),
  (2, '2024-01-05', 'ORD016', 27.50),
  (2, '2024-01-07', 'ORD017', 65.75),
  (2, '2024-01-10', 'ORD018', 75.50);


--join
SELECT * FROM order1 as o
INNER JOIN student as s
ON o.student_id = s.student_id

--left join
select * FROM student as c
LEFT JOIN order1 as o
ON c.student_id = o.student_id
