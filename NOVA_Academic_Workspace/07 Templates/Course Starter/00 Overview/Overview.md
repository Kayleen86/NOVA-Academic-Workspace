---
type: course
course_name: ""
semester: ""
course_type: ""
weekday: ""
start_time: ""
end_time: ""
location: ""
instructor: ""
course_url: ""
credits:
status: active
exam_date:
exam_format: ""
exam_registered: false
exam_taken: false
grade: ""
---
# 🎓 Course Overview

[[01 Courses/Course Catalog|← All courses]] · [[02 Schedule/Weekly Timetable|Timetable]] · [[06 Exams/Exam Dashboard|Exams]]

> [!important] Complete the Properties above
> Set **`course_name`** to the exact name of this course; set **`semester`** (same format across courses, e.g. `2027 Spring`), weekly meeting details, instructor and assessment information. Leave unannounced dates blank. `status` should be `active` during the semester and `archived` when it is finished.

## Course information

- **Course / learning platform:** Open `course_url` from the Properties above.
- **Learning outcomes:** 
- **Assessment requirements:** 
- **Important contacts:** 

## Lecture notes

[Open this course's Notes Index](../Notes/Index.md)

Make a new Markdown file inside **`Notes/`** with a descriptive name such as `YYYY-MM-DD Topic`. Apply the **Lecture Note** core template. The Notes Index lists it automatically.

## Materials

Put PDFs, handouts and slides in **`Materials/`**. Use `[[Filename.pdf]]` to link to a PDF without embedding a full preview; use `![[Filename.pdf]]` only when you want an embedded preview.

## Tasks

[Open this course's Tasks file](../Tasks/Tasks.md) · [[03 Tasks & Deadlines/Task Dashboard|All tasks]]

> Add or complete tasks in the course task file. They appear automatically on the [[03 Tasks & Deadlines/Task Dashboard|Task Dashboard]].

## Related reading

The `related_course` property on paper notes must match this course's `course_name`.

```dataview
TABLE WITHOUT ID
  file.link AS "Source",
  year AS "Year",
  reading_status AS "Status"
FROM "04 Library"
WHERE (type = "paper" OR type = "reading-note") AND related_course = this.course_name AND this.course_name != ""
SORT year DESC, file.name ASC
```

## Exam preparation notes

- **Topics to review:**
- **Practice questions / exercises:**
- **Resources and past exams:**
- **Registration notes:**

## Ongoing notes and questions
