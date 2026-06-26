# University Management System
### B103 Databases & Big Data — Individual Project
**Gisma University of Applied Sciences | School of Computer Science**

---

## Project Overview

This project is a relational database system for a University Management System, built using SQL (MySQL). It models the core academic entities of a university — departments, instructors, students, courses, enrollments, and grades — and demonstrates a full range of database operations including schema design, data insertion, querying, and modification.

---

## Repository Contents

```
├── university_db.sql      # Full SQL script (schema + data + queries)
└── README.md              # This file–––
└── er_diagrame            # fila containing the entity relationship diagrame
```

---

## Database Schema

The database consists of 6 tables:

| Table | Description |
|---|---|
| `departments` | Academic departments (e.g. Computer Science, Engineering) |
| `instructors` | Teaching staff, linked to a department |
| `students` | Enrolled students, linked to a department |
| `courses` | Courses offered, linked to a department and instructor |
| `enrollments` | Junction table linking students to courses |
| `grades` | Grade record for each completed enrollment |

### Entity Relationships

```
departments ──< instructors
departments ──< students
departments ──< courses
instructors ──< courses
students    ──< enrollments >── courses
enrollments ──< grades
```

---

## How to Run

### Requirements
- MySQL 
- Any SQL client (MySQL Workbench, DBeaver, command line, etc.)

### Steps

1. Clone or download this repository
2. Open the file in your SQL client
3. Run the  script 

The script will automatically:
- Create the `Uni_management` schema
- Create all 6 tables with constraints
- Insert sample data (5 departments, 8 instructors, 12 students, 12 courses, 31 enrollments, 19 grades)
- You can then execute each query to filter, display, update, or verify data.


> **Note:** The last line of the script (`DROP DATABASE Uni_management;`) is included for cleanup during development. Comment it out or remove it if you want to keep the data after running.

---

## Sample Data

| Table | Records |
|---|---|
| departments | 5 |
| instructors | 8 |
| students | 12 |
| courses | 12 |
| enrollments | 31 |
| grades | 19 |

---

## Queries Included

The script demonstrates 18 queries covering:

- **SELECT + JOIN** — students with departments, courses with instructors, grade reports
- **WHERE filters** — students by department, courses by credits, GPA threshold, active enrollments
- **GROUP BY + aggregations** — student counts per department, average GPA, grade statistics, instructor workload, payroll summary
- **UPDATE with subqueries** — department transfer, salary increase, enrollment status change

---

## Author

| Field | Detail |
|---|---|
| Name | Pranav Tokhi |
| Student ID | GH1045521 |
| Module | B103 Databases & Big Data |
| Institution | Gisma University of Applied Sciences |

---

