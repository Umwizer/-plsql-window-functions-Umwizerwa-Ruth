1. Insert Students
   INSERT INTO students VALUES (1001, 'Alice', 'Mukamana', DATE '2024-01-15', 'Computer Science');
   INSERT INTO students VALUES (1002, 'Bob', 'Habimana', DATE '2024-01-15', 'Computer Science');
   INSERT INTO students VALUES (1003, 'Claire', 'Uwase', DATE '2024-01-15', 'Information Systems');

2. Insert Courses
   INSERT INTO courses VALUES (2001, 'INSY8311', 'Database Development', 'Eric Maniraguha', 'Fall 2024');
   INSERT INTO courses VALUES (2002, 'INSY8312', 'Advanced PL/SQL', 'Eric Maniraguha', 'Fall 2024');
   INSERT INTO courses VALUES (2003, 'INSY8313', 'Data Warehousing', 'Eric Maniraguha', 'Fall 2024');

3. Insert Student Grades (Multiple assessments for window functions)
   Student 1001
   INSERT INTO student_grades VALUES (3001, 1001, 2001, DATE '2024-09-10', 'Quiz 1', 85.5, 100);
   INSERT INTO student_grades VALUES (3002, 1001, 2001, DATE '2024-09-20', 'Midterm Exam', 92.0, 100);
   INSERT INTO student_grades VALUES (3003, 1001, 2001, DATE '2024-10-15', 'Final Exam', 88.5, 100);

-- Student 1002
INSERT INTO student_grades VALUES (3004, 1002, 2001, DATE '2024-09-10', 'Quiz 1', 78.0, 100);
INSERT INTO student_grades VALUES (3005, 1002, 2001, DATE '2024-09-20', 'Midterm Exam', 82.0, 100);
INSERT INTO student_grades VALUES (3006, 1002, 2001, DATE '2024-10-15', 'Final Exam', 85.0, 100);

-- Student 1003
INSERT INTO student_grades VALUES (3007, 1003, 2001, DATE '2024-09-10', 'Quiz 1', 92.5, 100);
INSERT INTO student_grades VALUES (3008, 1003, 2001, DATE '2024-09-20', 'Midterm Exam', 95.0, 100);
INSERT INTO student_grades VALUES (3009, 1003, 2001, DATE '2024-10-15', 'Final Exam', 94.0, 100);

-- 4. Verify data insertion
SELECT 'Students inserted: ' || COUNT(_) FROM students;
SELECT 'Courses inserted: ' || COUNT(_) FROM courses;
SELECT 'Grades inserted: ' || COUNT(\*) FROM student_grades;
