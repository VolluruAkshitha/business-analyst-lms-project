\# 08 - Sample SQL Queries for LMS



\## 1. Get all enrolled students

SELECT student\_name, course\_name

FROM enrollments;



\## 2. Count number of students per course

SELECT course\_name, COUNT(student\_id)

FROM enrollments

GROUP BY course\_name;



\## 3. Get unpaid enrollments

SELECT student\_name, course\_name

FROM enrollments

WHERE payment\_status = 'Unpaid';



\## 4. Get total revenue

SELECT SUM(payment\_amount)

FROM payments;



\## 5. List instructors with number of courses

SELECT instructor\_name, COUNT(course\_id)

FROM courses

GROUP BY instructor\_name;

