# 📘 SQL Assignment: Students Table

## 📌 Table Used for ALL Questions

**Table Name:** `students`

### Table Structure

```sql
students (
    id INT,
    name VARCHAR(50),
    age INT,
    city VARCHAR(50),
    email VARCHAR(100)
);
```

---

## 🧾 Initial Data Provided

```sql
INSERT INTO students (id, name, age, city, email) VALUES
(1, 'Amit', 21, 'Delhi', 'amit@gmail.com'),
(2, 'Neha', 20, 'Mumbai', 'neha@yahoo.com'),
(3, 'Ankit', 23, 'Delhi', 'ankit@gmail.com'),
(4, 'Rohan', 19, 'Pune', 'rohan@gmail.com'),
(5, 'Riya', 22, 'Jaipur', 'riya@gmail.com'),
(6, 'Suman', NULL, 'Delhi', NULL),
(7, 'Kunal', 24, 'Mumbai', 'kunal@gmail.com'),
(8, 'Ayaan', 18, 'Pune', 'ayaan@gmail.com'),
(9, 'Nitin', 25, 'Delhi', 'nitin@outlook.com'),
(10, 'Varun', 20, 'Noida', NULL),
(11, 'Aarti', 21, 'Delhi', 'aarti@gmail.com'),
(12, 'Pankaj', NULL, 'Jaipur', 'pankaj@gmail.com'),
(13, 'Mohan', 22, 'Mumbai', 'mohan@yahoo.com'),
(14, 'Raman', 23, 'Pune', 'raman@gmail.com'),
(15, 'Arjun', 19, 'Delhi', 'arjun@gmail.com');
```

---

## 🟢 PART A: INSERT (Questions 1–8)

1. Insert a student with all column values

```sql
INSERT INTO students VALUES (16, 'Kriti', 22, 'Delhi', 'kriti@gmail.com');
```

2. Insert a student without email

```sql
INSERT INTO students (id, name, age, city) VALUES (17, 'Rahul', 21, 'Pune');
```

3. Insert a student with NULL age

```sql
INSERT INTO students VALUES (18, 'Sneha', NULL, 'Mumbai', 'sneha@gmail.com');
```

4. Insert three students in one query

```sql
INSERT INTO students VALUES
(19, 'Tina', 20, 'Delhi', 'tina@gmail.com'),
(20, 'Ravi', 23, 'Jaipur', 'ravi@gmail.com'),
(21, 'Aman', 24, 'Pune', 'aman@gmail.com');
```

5. Insert using different column order

```sql
INSERT INTO students (name, id, city, age, email)
VALUES ('Vikas', 22, 'Mumbai', 25, 'vikas@gmail.com');
```

6. Insert only id and name

```sql
INSERT INTO students (id, name) VALUES (23, 'Mehul');
```

7. Insert two students from same city

```sql
INSERT INTO students VALUES
(24, 'Pooja', 21, 'Delhi', 'pooja@gmail.com'),
(25, 'Nikhil', 22, 'Delhi', 'nikhil@gmail.com');
```

8. Insert student with lowercase city name

```sql
INSERT INTO students VALUES (26, 'Isha', 20, 'delhi', 'isha@gmail.com');
```

---

## 🟢 PART B: BASIC SELECT (Questions 9–14)

9. Display all records

```sql
SELECT * FROM students;
```

10. Display name and email

```sql
SELECT name, email FROM students;
```

11. Students with age > 21

```sql
SELECT * FROM students WHERE age > 21;
```

12. Students not from Delhi

```sql
SELECT * FROM students WHERE city != 'Delhi';
```

13. Students with age = 20

```sql
SELECT * FROM students WHERE age = 20;
```

14. Students with id ≤ 10

```sql
SELECT * FROM students WHERE id <= 10;
```

---

## 🟢 PART C: CONDITIONS & FILTERING (Questions 15–21)

15. Age between 18 and 25

```sql
SELECT * FROM students WHERE age BETWEEN 18 AND 25;
```

16. From Delhi or Mumbai

```sql
SELECT * FROM students WHERE city IN ('Delhi', 'Mumbai');
```

17. City in Delhi, Pune, Jaipur

```sql
SELECT * FROM students WHERE city IN ('Delhi', 'Pune', 'Jaipur');
```

18. Name starts with A

```sql
SELECT * FROM students WHERE name LIKE 'A%';
```

19. Name ends with n

```sql
SELECT * FROM students WHERE name LIKE '%n';
```

20. Email contains gmail

```sql
SELECT * FROM students WHERE email LIKE '%gmail%';
```

21. Name with exactly 5 characters

```sql
SELECT * FROM students WHERE LENGTH(name) = 5;
```

---

## 🟢 PART D: NULL, DISTINCT, SORTING (Questions 22–30)

22. Age is NULL

```sql
SELECT * FROM students WHERE age IS NULL;
```

23. Email is NOT NULL

```sql
SELECT * FROM students WHERE email IS NOT NULL;
```

24. Distinct cities

```sql
SELECT DISTINCT city FROM students;
```

25. Order by age (ascending)

```sql
SELECT * FROM students ORDER BY age ASC;
```

26. Order by name (descending)

```sql
SELECT * FROM students ORDER BY name DESC;
```

27. First 5 records

```sql
SELECT * FROM students LIMIT 5;
```

28. Youngest 3 students

```sql
SELECT * FROM students ORDER BY age ASC LIMIT 3;
```

29. Delhi students ordered by name

```sql
SELECT * FROM students WHERE city = 'Delhi' ORDER BY name;
```

30. Age NOT NULL and city Delhi

```sql
SELECT * FROM students WHERE age IS NOT NULL AND city = 'Delhi';
```

---

## ✅ Conclusion

This assignment covers **INSERT**, **SELECT**, **filtering**, **pattern matching**, **NULL handling**, **sorting**, and **limiting results**, helping build strong SQL fundamentals.

---

## 👩‍💻 Author

**Tripti**
B.Tech CSE Student
