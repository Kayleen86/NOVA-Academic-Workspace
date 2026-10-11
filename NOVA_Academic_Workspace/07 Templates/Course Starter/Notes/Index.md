# 📝 Lecture Notes Index

[[01 Courses/Course Catalog|← Course Catalog]] · [[START HERE|Home]]

Create lecture notes in this **same `Notes` folder** and use the **Lecture Note** template. This index works without inserting any particular course name into the query.

```dataview
TABLE WITHOUT ID
  file.link AS "Note",
  date AS "Date",
  topic AS "Topic"
FROM "01 Courses"
WHERE type = "lecture-note" AND file.folder = this.file.folder
SORT date DESC, file.name ASC
```
