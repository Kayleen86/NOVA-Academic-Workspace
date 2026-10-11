# 🎯 Exam Dashboard

[[START HERE|← Home]] · [[01 Courses/Course Catalog|Courses]] · [[06 Exams/Exam Archive|Exam archive]]

> [!info] Edit on the course page
> Each active course's **Overview** stores `exam_date`, `exam_format`, `exam_registered`, `exam_taken`, and `grade`. This is a read-only view, not a second exam database. Dates can be empty if not announced yet.

## Exams for active courses

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  semester AS "Semester",
  exam_date AS "Date",
  exam_format AS "Format",
  choice(exam_registered, "☑", "☐") AS "Registered",
  choice(exam_taken, "☑", "☐") AS "Taken",
  grade AS "Grade"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND course_name != ""
SORT exam_date ASC, course_name ASC
```

> [!tip] Need revision support?
> Open the course Overview and fill its **Exam preparation notes** section. No extra plugin or duplicate exam card is needed.
