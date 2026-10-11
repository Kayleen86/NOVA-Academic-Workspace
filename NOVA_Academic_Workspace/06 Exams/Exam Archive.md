# 🗂️ Exam Archive

[[06 Exams/Exam Dashboard|← Active exams]] · [[01 Courses/Course Catalog|Courses]]

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  semester AS "Semester",
  exam_date AS "Exam date",
  exam_format AS "Format",
  grade AS "Grade"
FROM "01 Courses"
WHERE type = "course" AND status = "archived" AND course_name != ""
SORT semester DESC, course_name ASC
```

Changing a course's `status` to `archived` moves it here while preserving the course folder, lecture notes, files and task history.
