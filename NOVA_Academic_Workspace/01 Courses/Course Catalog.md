# 🎓 Course Catalog

[[START HERE|← Home]] · [[02 Schedule/Weekly Timetable|Timetable]] · [[06 Exams/Exam Dashboard|Exams]]

> [!tip] Add a course
> Copy the **entire folder** `07 Templates/Course Starter` into `01 Courses`, rename the copied folder to your course name, then edit `00 Overview/Overview.md`. You do not need to edit any of the tables below.

## Active courses

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  semester AS "Semester",
  course_type AS "Type",
  instructor AS "Instructor",
  weekday AS "Day"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND course_name != ""
SORT semester DESC, course_name ASC
```

## Archived courses

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  semester AS "Semester",
  grade AS "Grade"
FROM "01 Courses"
WHERE type = "course" AND status = "archived" AND course_name != ""
SORT semester DESC, course_name ASC
```
