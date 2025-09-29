


-- 1. Create Students Table
CREATE TABLE students (
    student_id NUMBER PRIMARY KEY,
    first_name VARCHAR2(50) NOT NULL,
    last_name VARCHAR2(50) NOT NULL,
    enrollment_date DATE NOT NULL,
    department VARCHAR2(100) NOT NULL
);

-- 2. Create Courses Table
CREATE TABLE courses (
    course_id NUMBER PRIMARY KEY,
    course_code VARCHAR2(20) NOT NULL,
    course_name VARCHAR2(100) NOT NULL,
    instructor VARCHAR2(100) NOT NULL,
    academic_term VARCHAR2(50) NOT NULL
);

-- 3. Create Student Grades Table
CREATE TABLE student_grades (
    grade_id NUMBER PRIMARY KEY,
    student_id NUMBER NOT NULL,
    course_id NUMBER NOT NULL,
    assessment_date DATE NOT NULL,
    assessment_type VARCHAR2(50) NOT NULL,
    score NUMBER(5,2) NOT NULL,
    max_score NUMBER(5,2) NOT NULL,
    CONSTRAINT fk_student FOREIGN KEY (student_id) REFERENCES students(student_id),
    CONSTRAINT fk_course FOREIGN KEY (course_id) REFERENCES courses(course_id)
);

-- 4. Create Performance Indexes
CREATE INDEX idx_student_grades_student ON student_grades(student_id);
CREATE INDEX idx_student_grades_course ON student_grades(course_id);
CREATE INDEX idx_student_grades_date ON student_grades(assessment_date);

-- 5. Verify table creation
SELECT 'Students table created successfully' AS status FROM dual;
SELECT 'Courses table created successfully' AS status FROM dual;
SELECT 'Student_grades table created successfully' AS status FROM dual;