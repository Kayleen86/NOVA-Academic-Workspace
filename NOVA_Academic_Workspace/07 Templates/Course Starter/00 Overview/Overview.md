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

[[01 Courses/Course Catalog|← Courses]] · [[02 Schedule/Weekly Timetable|Timetable]] · [[03 Tasks & Deadlines/Task Dashboard|Task dashboard]] · [[06 Exams/Exam Dashboard|Exams]]

> [!info] First: complete the Properties
> Enter the course name, semester, instructor, course link, weekly schedule, credits and exam details **once in the Properties above**. Keep `type: course` and `status: active`. These values feed the shared dashboards; there is no need to repeat them below.

## Lecture notes

[Open lecture notes](../Notes/Index.md) · [Manage course tasks](../Tasks/Tasks.md)

Add your notes inside this course's `Notes/` folder. Apply the **Lecture Note** template to new notes; the Notes Index collects them automatically.

## Course materials

Store course-specific **PDFs, slides, handouts and cheat sheets** in the course's `Materials/` folder. Everything in that folder appears below automatically, even if it is not linked in a lecture note. You do **not** need to edit this query when you copy and rename the Course Starter folder.

```base
filters:
  and:
    - 'file.inFolder(this.file.folder.replace("/00 Overview", "") + "/Materials")'
    - 'file.ext != "base"'
formulas:
  material: 'file.asLink(file.name)'
properties:
  formula.material:
    displayName: "Document"
  file.ext:
    displayName: "Type"
views:
  - type: table
    name: "Course files"
    order:
      - formula.material
      - file.ext
```

## Tasks & deadlines

[Open the course task list](../Tasks/Tasks.md) · [[03 Tasks & Deadlines/Task Dashboard|View all open tasks]]

Enter new tasks in `Tasks/Tasks.md`. The shared Task Dashboard shows open items; completed checkboxes stay in the course task file.

## Related reading

Set `related_course` on reading notes to the **exact** `course_name` property above.

```dataview
TABLE WITHOUT ID
  file.link AS "Source",
  year AS "Year",
  reading_status AS "Status"
FROM "04 Library"
WHERE (type = "paper" OR type = "reading-note") AND related_course = this.course_name AND this.course_name != ""
SORT year DESC, file.name ASC
```

## Exam preparation

- **Topics to review:**
- **Practice questions / exercises:**
- **Resources and past exams:**
- **Registration notes:**

## Ongoing course notes

- 
