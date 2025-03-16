# Student Database - Relational Database Project: Part 2

This project is part of the "Learn SQL by Building a Student Database: Part 2" course offered by [freeCodeCamp](https://www.freecodecamp.org/). It involves creating and interacting with a PostgreSQL database that stores information about students, their majors, and the courses they take. The project includes a PostgreSQL schema and bash script for querying and managing the student data.

## Project Overview

In this project, you'll build and manage a relational database that tracks computer science students, their majors, and the courses they enroll in. The PostgreSQL portion creates tables for `students`, `courses`, and `majors`, along with sequences, constraints, and data insertion. The bash script portion allows you to run a variety of SQL queries to retrieve and manipulate data within the database.

## Features

### PostgreSQL Schema

The database schema consists of the following main components:

1. **students** - Stores information about students (e.g., student ID, first name, last name, major, GPA).
2. **courses** - Stores information about courses (e.g., course ID, course name).
3. **majors** - Stores information about the various majors available (e.g., major ID, major name).
4. **majors_courses** - A join table that maps majors to the courses they offer.
  
Additionally, the schema includes constraints, such as primary keys and foreign keys, to maintain referential integrity.

### Bash Script

The bash script is designed to interact with the PostgreSQL database and run specific SQL queries. The script performs operations like:

- Retrieving students with a GPA of 4.0.
- Querying courses whose names start with a letter before 'D'.
- Filtering students based on their last name and GPA.
- Generating aggregated data like average GPA and counts of students in each major.
- Identifying courses with specific conditions (e.g., courses that 'Obie Hilpert' is not taking).

## Requirements

Before running the project, make sure you have the following installed:

- PostgreSQL (version 12.6 or higher)
- Bash shell (for running the bash script)

## How to Run

### 1. Setting up the PostgreSQL Database

1. **Create the database and tables:**
   - Ensure you have PostgreSQL installed on your system.
   - Connect to your PostgreSQL instance and run the SQL commands provided in the PostgreSQL script portion of this project.
   - The commands will create the `students` database, tables, and insert sample data.

2. **Connect to the `students` database:**
   - Use the following command to connect to the database:
     ```bash
     psql -U freecodecamp -d students
     ```

3. **Verify the database:**
   - Run some queries to make sure the tables have been set up correctly. For example:
     ```sql
     SELECT * FROM students;
     ```

### 2. Running the Bash Script

1. **Make the script executable:**
   - Open your terminal and navigate to the folder where your script is located.
   - Run the following command to make the script executable:
     ```bash
     chmod +x script_name.sh
     ```

2. **Execute the script:**
   - Run the script using the following command:
     ```bash
     ./script_name.sh
     ```

3. **View Results:**
   - The script will output results of various SQL queries, such as lists of students, courses, and aggregated statistics.

## SQL Queries in the Script

The bash script executes the following SQL queries:

1. **Students with a GPA of 4.0:**
   - Retrieves the first name, last name, and GPA of all students with a 4.0 GPA.

2. **Courses Starting with 'A', 'B', or 'C':**
   - Retrieves courses whose names start with a letter before 'D'.

3. **Students with Specific GPA Conditions:**
   - Retrieves students whose last name starts with 'R' or later and whose GPA is greater than 3.8 or less than 2.0.

4. **Students with Specific Last Name Patterns:**
   - Retrieves students whose last names contain 'sa' or have 'r' as the second to last letter.

5. **Students Without a Major:**
   - Retrieves students who have not declared a major, where the first name starts with 'D' or they have a GPA greater than 3.0.

6. **Courses with Specific Letter Patterns:**
   - Retrieves courses where the second letter is 'e' or the course ends with 's', ordered in reverse alphabetical order.

7. **Average GPA of All Students:**
   - Calculates the average GPA of all students rounded to two decimal places.

8. **Statistics by Major:**
   - Retrieves the number of students and average GPA for each major with more than one student.

9. **Majors Without Students or with Specific Students:**
   - Retrieves majors that either have no students or have a student whose first name contains 'ma'.

10. **Courses Not Taken by 'Obie Hilpert':**
    - Retrieves a list of courses that 'Obie Hilpert' is not enrolled in.

11. **Courses with Only One Student:**
    - Retrieves courses that have exactly one student enrolled.

## License

This project is open-source and available under the MIT License.

## Conclusion

This project demonstrates the use of PostgreSQL for building a relational database with students, courses, and majors. By running the SQL queries in the bash script, you can gather insights and analyze the data in various ways.
