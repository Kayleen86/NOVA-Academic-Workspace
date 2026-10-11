# ✅ Tasks & Deadlines

[[START HERE|← Home]] · [[01 Courses/Course Catalog|Courses]] · [[06 Exams/Exam Dashboard|Exams]] · [[09 Planning/Weekly Review|Weekly review]]

> [!info] How this dashboard works
> Add and complete tasks in each course's `Tasks/Tasks.md` file. This page automatically collects **unfinished tasks** from your courses without requiring JavaScript permissions. Completed tasks are counted in the table below but do not clutter the dashboard.

## 🔥 Overdue

```tasks
not done
has due date
due before today
path includes 01 Courses/
sort by due
group by folder
hide backlink
hide toolbar
hide task count
```

## 📅 Upcoming deadlines

```tasks
not done
has due date
due on or after today
path includes 01 Courses/
sort by due
sort by priority
group by folder
hide backlink
hide toolbar
hide task count
```

## 📝 Tasks without a due date

```tasks
not done
no due date
path includes 01 Courses/
sort by priority
group by folder
hide backlink
hide toolbar
hide task count
```

## 📊 Task progress by course

```dataview
TABLE WITHOUT ID
  link(file.path, split(file.folder, "/")[1]) AS "Course",
  length(filter(file.tasks, (t) => !t.completed)) AS "Open",
  length(filter(file.tasks, (t) => t.completed)) AS "Done"
FROM "01 Courses"
WHERE file.name = "Tasks" AND contains(file.path, "/Tasks/") AND length(file.tasks) > 0
SORT length(filter(file.tasks, (t) => !t.completed)) DESC, file.folder ASC
```

> [!tip] No tasks showing?
> If the open-task sections are empty, you may simply have no unfinished tasks. The table lists only courses that contain tasks. To create one, open the course from [[01 Courses/Course Catalog|Course Catalog]] and add a line to its `Tasks/Tasks.md` file, such as `- [ ] Read chapter 2 📅 2027-03-15`.

### Task syntax (example, not an active task)

```markdown
- [ ] Read lecture notes 📅 2027-03-15
- [ ] Submit assignment 🔺 📅 2027-03-22
```

`📅` sets the due date; `🔺` marks the highest priority. Checking off a task updates its source file and the dashboard.
