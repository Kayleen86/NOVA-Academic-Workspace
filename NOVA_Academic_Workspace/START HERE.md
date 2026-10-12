---
cssclasses:
  - home
---
# ✦ NOVA · Academic Workspace

*Your home base for courses, notes, reading, deadlines and exams.*

> [!important] New here? Start with the setup guide.
> **[[docs/USER_GUIDE|Read the complete setup guide]]** · [[SETUP CHECKLIST|Open the setup checklist]]

## Navigate

| 🎓 Study | 📅 Organize | 📚 Learn |
|---|---|---|
| [[01 Courses/Course Catalog\|Course catalog]] | [[02 Schedule/Weekly Timetable\|Weekly timetable]] | [[04 Library/Reading Library\|Reading library]] |
| [[06 Exams/Exam Dashboard\|Upcoming exams]] | [[03 Tasks & Deadlines/Task Dashboard\|Tasks & deadlines]] | [[05 Knowledge Base/Glossary\|Knowledge base]] |
| [[07 Templates/Course Starter/00 Overview/Overview\|New-course starter]] | [[09 Planning/Weekly Review\|Weekly review]] | [[01 Courses/All Course Materials\|All course PDFs]] |

## Active courses

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  semester AS "Semester",
  course_type AS "Type"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND course_name != ""
SORT course_name ASC
```

## Upcoming tasks

```tasks
not done
has due date
due on or after today
path includes 01 Courses/
sort by due
limit 12
hide toolbar
hide task count
```

## Quick actions

- 📄 [[01 Courses/All Course Materials|Browse all course PDFs]] — files from each course’s `Materials/` folder, grouped by course.
- 📥 [[08 Attachments/Unsorted Attachments|Review unsorted attachments]] — files still in the shared attachments folder.

- ✍️ Put ideas in [[00 Inbox/Quick Capture|Quick Capture]], then organize them during your weekly review.
- ➕ Duplicate **[[07 Templates/Course Starter/00 Overview/Overview|Course Starter]]** as a **folder**, not just the Overview file.
- 🗂️ Use [[09 Planning/Weekly Review|Weekly Review]] to review unfinished work once a week.

> [!tip] Nothing showing up yet?
> The dashboards are deliberately empty until you create a course and install **Dataview** and **Tasks**. Follow the [[SETUP CHECKLIST|setup checklist]] first.
