---
type: timetable
---
# 🗓️ Weekly Timetable

[[START HERE|← Home]] · [[02 Schedule/Schedule Changes|Schedule changes]] · [[01 Courses/Course Catalog|Courses]]

> [!info] One source of truth
> Edit `weekday`, `start_time`, `end_time`, and `location` in each **course Overview**. Only courses with `status: active` appear. This is a **regular weekly timetable**, not a live calendar; date-specific changes belong in [[02 Schedule/Schedule Changes|Schedule Changes]].

## Monday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Monday"
SORT start_time ASC
```

## Tuesday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Tuesday"
SORT start_time ASC
```

## Wednesday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Wednesday"
SORT start_time ASC
```

## Thursday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Thursday"
SORT start_time ASC
```

## Friday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Friday"
SORT start_time ASC
```

## Saturday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Saturday"
SORT start_time ASC
```

## Sunday

```dataview
TABLE WITHOUT ID
  link(file.path, course_name) AS "Course",
  start_time + "–" + end_time AS "Time",
  course_type AS "Type",
  location AS "Location"
FROM "01 Courses"
WHERE type = "course" AND status = "active" AND weekday = "Sunday"
SORT start_time ASC
```

> [!warning] Limits
> Overlaps are **not detected automatically**, and the basic course template stores one recurring meeting per course. Add exceptional events in Schedule Changes; for multi-session modules, either maintain a second session manually or expand the system to a dedicated sessions database.
