# ✦ NOVA — Academic Workspace · Complete User Guide

**A reusable, English-language Obsidian vault for students.** NOVA is based on a real academic workflow, rebuilt without any specific course names, university names, personal notes, PDFs, or academic records. You can use it for almost any degree, training program or multi-course learning plan.

**Project overview:** [GitHub README](../../README.md) · **Open in Obsidian:** [START HERE](../START%20HERE.md) · **One-time setup:** [SETUP CHECKLIST](../SETUP%20CHECKLIST.md)

> **How this documentation is organized:** The repository's `README.md` is the short public introduction, maintained directly on GitHub. **This document, `docs/USER_GUIDE.md`, is the full instruction manual** for installing, configuring, and using NOVA. It is part of the Obsidian vault and is also readable on GitHub.

---

## 1. What you get

NOVA includes a course catalog, a weekly timetable, an aggregated task dashboard, exam tracking, lecture note indexes, a Zotero-friendly reading library, a permanent knowledge base, quick capture and weekly review pages. All course overview data is edited in **one place**: the course's `00 Overview/Overview.md`.

**Design decisions:**

- No actual courses or semester dates are pre-filled. All dashboards begin empty by design.
- A new course is created by duplicating **one full folder** — no code or query rewriting is required.
- For your lecture notes, Obsidian's built-in **Templates** plugin is enough; **Templater is not needed**.
- **Dataview** shows automatic tables. **Tasks** aggregates ordinary Markdown checkboxes.
- Zotero support is optional. No Zotero library, attachments, login, or personal data is bundled.
- No third-party plugin executable files are included in the ZIP. Install current plugins from Obsidian's community plugin browser.

## 2. Folder guide

| Path | Purpose |
|---|---|
| `00 Inbox` | Capture notes or links before filing them |
| `01 Courses` | Your own course folders and the automatic course catalog |
| `02 Schedule` | Recurring weekly timetable and one-off changes |
| `03 Tasks & Deadlines` | Open, overdue and completed task queries |
| `04 Library` | Papers, reading notes, useful links and cross-course notes |
| `05 Knowledge Base` | Glossary and evergreen concept notes |
| `06 Exams` | Active exam view and archived results |
| `07 Templates` | Core templates, complete course starter, Zotero import template |
| `08 Attachments` | General PDFs and pasted images not assigned to a course |
| `09 Planning` | Weekly review and dated review archive |
| `.obsidian` | Core settings, safe visual snippets and optional Zotero import settings |

## 3. First-time installation (desktop)

1. On the GitHub project page, choose **Code → Download ZIP**, **extract** the download (do not open the ZIP as a vault), and keep the extracted folder in a stable location. The folder name may differ depending on how you downloaded it. You can also create a copy using **Use this template** if the repository owner enabled that GitHub feature.
2. Install [Obsidian](https://obsidian.md/), then choose **Open folder as vault** and select that folder.
3. Open [START HERE](../START%20HERE.md) and [SETUP CHECKLIST](../SETUP%20CHECKLIST.md).
4. In **Settings → Community plugins**, choose to enable community plugins **only if you trust the installed plugin authors and source**. Use the plugin browser to install **Dataview** and **Tasks**, then enable each plugin. The first view may display literal `dataview` or `tasks` code blocks until the plugin is active.
5. In **Settings → Core plugins**, enable **Templates**; in **Settings → Templates**, select `07 Templates` as the folder. This vault already includes that path in its settings, but verify it after opening.
6. Optional: in **Settings → Appearance → CSS snippets**, enable `nova-dashboard` and `nova-tasks-clean`. The workspace remains usable without them.
7. Optional: install **Zotero Integration** and follow section 9 before importing your first item. **Drag & Drop Sort** is optional, not needed by the dashboard queries.
8. Create your first course as described in section 4. The automatic course, timetable and exam views will then populate.

**No JavaScript queries, Obsidian terminal commands, or external build tools are required.** Dataview uses standard `dataview` queries, not `dataviewjs`.

### About language and spelling

All included notes, headings, filenames and descriptions are English. Obsidian's spellcheck is initially disabled (`Settings → Editor → Spellcheck` can turn it back on). Some application UI labels may differ according to your Obsidian display language.

## 4. Create a course — the most important step

1. In your operating system's **file manager** (Windows File Explorer or macOS Finder), **copy the folder** `07 Templates/Course Starter`.
2. **Paste the folder inside** `01 Courses`, next to `Course Catalog.md`.
3. Rename the copy to your chosen course name, e.g. `My Course`. **Do not move the original starter**; it is needed for future courses. The example is just a placeholder; no course named My Course is included in this release.
4. Open `01 Courses/<YOUR COURSE>/00 Overview/Overview.md` and show its Properties at the top.
5. Set `course_name` to the course's real name. Fill `semester`, `course_type`, `weekday`, `start_time`, `end_time`, `location`, `instructor` and `course_url` as applicable. Leave unknown fields empty.
6. Keep `type: course` and `status: active` unchanged. The `type` value identifies the file to the dashboards; the `status` value controls whether it appears in *current* views.
7. Open [Course Catalog](../01%20Courses/Course%20Catalog.md), [Weekly Timetable](../02%20Schedule/Weekly%20Timetable.md) and [Exam Dashboard](../06%20Exams/Exam%20Dashboard.md). The new course should appear automatically where it has the relevant information.

### Course folder after copying

```text
01 Courses/
  <YOUR COURSE>/
    00 Overview/
      Overview.md         <- edit course metadata here
    Notes/
      Index.md            <- automatic lecture note index
    Materials/             <- PDFs, slides, handouts
    Tasks/
      Tasks.md            <- enter tasks here
```

**Important:** Some Obsidian versions do not support duplicating an entire folder from Obsidian's own File explorer. Use your operating system's file manager for this step. Obsidian normally detects the new folder automatically. Copying just `Overview.md` does not create the other folders. Copy the entire Course Starter folder each time. The course folder can be renamed later, but avoid nesting a course inside another course.

### Course property reference

| Property | Example | How it is used |
|---|---|---|
| `type` | `course` | Keep this exact value to include the note in course queries |
| `course_name` | `My Course` | Display name in the course catalog and timetable |
| `semester` | `2027 Spring` | Text label for chronological organization; choose one convention |
| `course_type` | `Lecture`, `Seminar`, `Lab` | Optional course category |
| `weekday` | `Monday` | **English full day name**; used by timetable filters |
| `start_time` / `end_time` | `09:00` / `11:00` | 24-hour `HH:mm` text for sorting and display |
| `location` | `Campus / online` | Shown on timetable |
| `instructor` | `Instructor name` | Shown in course catalog |
| `course_url` | `https://...` | Course's LMS or registration link |
| `credits` | `3` | Optional numeric credits / ECTS |
| `status` | `active` or `archived` | **Exactly** these values control active and archived views |
| `exam_date` | `2027-06-15` | Obsidian **Date** property; leave blank if unknown |
| `exam_format` | `Written`, `Oral`, `Project` | Free text |
| `exam_registered` / `exam_taken` | checkbox | Edit on the Overview page, not in the exam dashboard |
| `grade` | local grade format | Optional, entered after assessment |

**Dates:** `YYYY-MM-DD`. **Times:** use leading zeros (`09:00`, not `9:00`). **Weekdays:** `Monday`, `Tuesday`, `Wednesday`, `Thursday`, `Friday`, `Saturday` or `Sunday` — the timetable matches these literally.

### How to handle more than one weekly session

The starter intentionally has one regular `weekday/start_time/end_time/location` record per course, matching the simple setup in the original vault. For a second weekly lecture or lab, add a manual row to [Schedule Changes](../02%20Schedule/Schedule%20Changes.md) (clearly mark it as recurring) or customize the timetable for multiple meetings. NOVA does **not** automatically expand a course into several weekly sessions or detect time conflicts. Avoid creating fake duplicate course folders just to add a second time; that would duplicate tasks/exams.

## 5. Lecture notes and course material

1. Enter the new course's `Notes` folder.
2. Create a new note with a descriptive filename, e.g. `2027-03-15 First Lecture.md`.
3. Use **Ctrl+P → Templates: Insert template → Lecture Note** (menu wording may vary). You can also use the Templates command from Obsidian's ribbon.
4. Set `topic` in Properties; the `date` field uses the core template's `{{date}}` token, which resolves when inserted.
5. Write notes under Main points, Details, Open questions and Materials. The **Notes/Index.md** automatically lists notes marked `type: lecture-note` in the same folder.
6. Save course PDFs in that course's **Materials/** folder. For a clickable link only, use `[[Document.pdf]]`; for a large inline PDF preview use `![[Document.pdf]]`.

**Why the query is reusable:** Each copied Notes Index uses `file.folder = this.file.folder` to find notes next to itself, not a hard-coded original course name. **Do not manually rename** the `type` value or store all lecture notes in a shared folder if you want automatic per-course indexes.

If a lecture note date looks like a string instead of a date, open Properties and set the `date` field to Obsidian's **Date** type; the ISO value itself remains the same.

## 6. Tasks, deadlines and priorities

Each course contains **one** `Tasks/Tasks.md` file. Add one real Markdown checkbox per task:

```markdown
- [ ] Read the assigned paper 📅 2027-03-15
- [ ] Submit the project 🔺 📅 2027-03-22
- [ ] Organize lecture files
```

- `- [ ]` creates an open task and `- [x]` marks it complete.
- `📅 YYYY-MM-DD` is an optional due date recognized by Tasks.
- `🔺` indicates highest priority in the Tasks plugin.
- The [Task Dashboard](../03%20Tasks%20%26%20Deadlines/Task%20Dashboard.md) reads tasks from the **`01 Courses`** subtree (not the setup checklist or template folder). It displays **only unfinished tasks** under **Overdue**, **Upcoming deadlines**, and **Tasks without a due date**, grouped by their source folder.
- A Dataview table below the task lists shows **Open** and **Done** task counts for each course with tasks. **Completed tasks do not appear again as a long list on the dashboard**, but remain in the original `Tasks/Tasks.md` course files.
- Change a task in its course file (or mark it complete in the Tasks view); the dashboard is an automatic view, not a second task list. The query uses native Tasks grouping (`group by folder`) and **does not require enabling JavaScript inside the Tasks plugin**.

The Weekly Review checklist and Setup Checklist are organizational checklists, not course tasks and are excluded from the central Tasks query on purpose. To have a review action on the task dashboard, add it as a task under the relevant course.

## 7. Exams and assessments

Open a course's `00 Overview/Overview.md`. Enter `exam_date`, `exam_format`, `exam_registered`, `exam_taken` and `grade` in that note's **Properties**. The [Exam Dashboard](../06%20Exams/Exam%20Dashboard.md) reads them automatically for all `active` courses. Its ☑ / ☐ values are only visual indicators: **click the course name to edit the source Properties**.

For study prep, use the **Exam preparation notes** section inside the same Overview, or create real checkbox tasks in the course's `Tasks/Tasks.md` when you want reminders. If an exam date is not announced, leave it blank; do not invent a placeholder date.

## 8. Semesters, archiving and history

**Start a new semester:**

1. Ensure the old semester's notes and documents are saved.
2. For each completed course, change `status` from `active` to `archived` **on the course Overview**. Leave the course folder in `01 Courses`.
3. Create new course folders by duplicating the **Course Starter** again, and enter the new `semester` text in each new Overview. Use **one consistent label** across courses (e.g. `2027 Autumn`).
4. The timetable, active course list and exam dashboard automatically show only active courses. Past courses remain in the Course Catalog's **Archived courses** and in [Exam Archive](../06%20Exams/Exam%20Archive.md).
5. Keep using the same [Weekly Timetable](../02%20Schedule/Weekly%20Timetable.md) and [Exam Dashboard](../06%20Exams/Exam%20Dashboard.md); do **not** overwrite or delete old course folders or replace the main dashboard for each semester.
6. Optionally copy completed weekly review notes into `09 Planning/Reviews` so reflections remain dated.

**Tasks from archived courses:** By design, the Task Dashboard still searches the whole `01 Courses` folder, including archived courses, so you do not silently lose unfinished obligations. Before archiving, complete or cancel irrelevant tasks. If you explicitly prefer hiding archived tasks, that requires more advanced Tasks queries or moving archived course folders outside `01 Courses`; moving outside also removes them from course and exam archive indexes.

## 9. Zotero: importing papers and preserving your notes

This feature is **optional** and is only intended for the **Zotero Integration** community plugin (`obsidian-zotero-desktop-connector`), not the similarly named Zotero plugins. The data settings are included, but the plugin code, Zotero itself and any desktop database are **not** bundled.

### Installation

1. Install [Zotero](https://www.zotero.org/) on your computer and add one reference to test. For predictable citation keys, consider installing [Better BibTeX for Zotero](https://retorque.re/zotero-better-bibtex/) as well.
2. In Obsidian → **Settings → Community plugins**, install and enable **Zotero Integration** by `mgmeyers` (if listed). Restart/reopen Zotero and Obsidian as needed.
3. In **Zotero Integration settings**, check or recreate an **Import format** named `NOVA Paper Note` with the values below. The vault includes suggested settings, but plugin installation/version differences may require you to select them manually.

| Zotero Integration setting | Value |
|---|---|
| Name | `NOVA Paper Note` |
| Output path | `04 Library/Zotero Papers/{{citekey}}.md` |
| Template file | `07 Templates/Zotero Import Template.md` |
| Image output path | `04 Library/Zotero Papers/Images/{{citekey}}/` |
| Image basename | `image` |
| CSL citation style | `apa` (or another preferred style) |

4. With Zotero running, use **Ctrl+P → Zotero Integration: NOVA Paper Note** (the full command name may vary by version), search for one paper and import.
5. Open [Reading Library](../04%20Library/Reading%20Library.md). The imported note will be listed automatically after Dataview indexes it. You should **not** have to copy a Dataview query into every paper.

### Safely add reading notes and course connections

The **Zotero Import Template** uses **Nunjucks** (Zotero Integration's language), not Obsidian Core Templates. Never apply it with **Templates: Insert template**. It also uses Dataview `key:: value` inline fields, **not dynamic YAML frontmatter**. This avoids the YAML syntax errors that can occur if a raw Nunjucks template is misread as an ordinary Obsidian Properties block.

In the imported paper, find the generated section **My reading notes and course connections**, which contains a preserved region such as `%% begin reading-notes %%` ... `%% end reading-notes %%`.

- Change `reading_status:: unread` to `reading`, `read`, or another consistent value.
- Fill `related_course:: My Course` with **exactly the same text** as the corresponding `course_name` property. This makes the paper appear on that course's Overview under **Related reading**, as well as the global Reading Library.
- Add all *your own prose* between those two persistence markers. Zotero Integration preserves this region when the same paper is imported again.
- The annotation region uses a separate `persist` block to append newly imported highlights while retaining prior annotations. Highlights depend on your Zotero item actually containing annotations.

**Caution:** Content outside the `persist` blocks can be regenerated on re-import. Always back up valuable notes and test the import format using a nonessential Zotero item first. The inline `type:: paper`, `title::`, `authors::`, `year::`, `citekey::` and `doi::` values are maintained by the import template itself. If no paper title or author appears, check that you selected the `NOVA Paper Note` import format and the correct template file.

### No Zotero? No problem

Create a file in `04 Library/Reading Notes`, insert the **Reading Note** core template, fill Properties and your summary. Its `type: reading-note` causes it to appear in the manual notes section of the Reading Library. Set `related_course` to your exact course name for course-level linking.

## 10. Knowledge base and cross-linking

The [Glossary](../05%20Knowledge%20Base/Glossary.md) is intended for reusable concepts that outlast a single course. Create a new note in `05 Knowledge Base/Concepts` and insert **Concept Note**, then set its `summary` and `related_course` if applicable. The glossary's Dataview table updates automatically.

Use `[[wiki links]]` to connect a concept to other notes. Mention source links in the concept's **Sources** section; avoid copying large passages from papers without attribution.

The [Quick Capture](../00%20Inbox/Quick%20Capture.md) note is an intentionally simple temporary holding area. During [Weekly Review](../09%20Planning/Weekly%20Review.md), move ideas from Inbox to course notes, the reading library, tasks or concept notes. Inbox entries are not automatically sorted.

## 11. Personalization and optional additions

- **Home screen:** Bookmark [START HERE](../START%20HERE.md); Obsidian may reopen the last open note instead of automatically opening Home after a restart. An automatic home plugin is not required.
- **Folder order:** Numbered top-level folders stay predictably sorted. If you install **Drag & Drop Sort**, you can change local ordering, but it is not a dependency and custom order might not transfer to other devices without its settings.
- **Theme / snippets:** The default Obsidian theme works. Snippets only add subtle accents and spacing; disable them without breaking queries.
- **Date formats:** Keep metadata dates as ISO `YYYY-MM-DD`, even if your operating system displays another format.
- **Sync:** Choose your own sync or backup tool; NOVA does not include a sync service or accounts.
- **Multi-session courses:** A future extension could create one session note per lecture/lab for a more sophisticated timetable. This is deliberately not required for the starter experience.

## 12. Troubleshooting

| Symptom | Likely cause / fix |
|---|---|
| Dataview block displays as code | Install and enable **Dataview** in Community plugins. Switch to Reading view if needed. |
| Tasks block displays as code | Install and enable **Tasks**. Use a valid `- [ ]` checkbox in a course Tasks file. |
| Tasks warns that JavaScript queries are disabled | You likely have an older custom query using `group by function`. The bundled NOVA dashboard uses `group by folder` and requires **no JavaScript permission**. Replace the modified dashboard with the current repository version. |
| Only completed tasks exist, but the task lists look empty | This is intentional: the main lists show **open tasks only**. Completed tasks remain in each course and are counted in the **Task progress by course** table. |
| New course missing from catalog | Copy the **entire starter folder** into `01 Courses`; set `type: course`, `course_name`, `status: active` in its Overview. Do not paste the new course under `07 Templates`. |
| Course missing from timetable | Set `weekday` to a full **English** weekday such as `Wednesday`. Keep the course `active`; fill start and end as `HH:mm`. |
| Exam checkboxes cannot be clicked in the table | Edit `exam_registered` and `exam_taken` in the **course Overview Properties**; the Dataview table is read-only. |
| Lecture notes not in course Notes Index | The note must be stored under the same course's `Notes/` folder and have `type: lecture-note`. |
| Paper is missing from reading table | Ensure it was imported into `04 Library/Zotero Papers/` with `type:: paper`, and Dataview is active. |
| Paper title/authors show strangely | Inspect the **generated paper note** (not the Nunjucks template) for `title::` and `authors::`; check the selected import format and the Zotero metadata. |
| Course-linked papers are absent | `related_course::` must exactly match the course Overview `course_name`; put the field inside the preserved section of the imported paper. |
| Template shows Nunjucks `{% ... %}` or `{{title}}` | You opened the **Zotero import template itself**, rather than a generated paper. Use Zotero Integration to import a real item. |
| Templates placeholder remains `{{date}}` | Use **Templates: Insert template → Lecture Note** instead of copying raw template content; set the date manually if needed. |
| PDF displays as full embedded page | Replace `![[File.pdf]]` with `[[File.pdf]]` to use a link only. |
| Unexpected tasks from past semesters | The task dashboard deliberately includes archived course tasks. Complete/cancel obsolete tasks or adjust your workflow. |
| Nothing appears on first launch | The starter vault contains no real courses or papers; empty result sets are **expected** until you create some data. |

## 13. Privacy and sharing checklist

Before you publicly publish a personalized copy:

1. Remove names, grades, personal schedules, student numbers, emails, institution URLs, private documents and handwritten notes that you do not want to share.
2. Remove confidential PDFs or their annotations from `Materials`, `08 Attachments`, `04 Library` and course folders.
3. Inspect `.obsidian` and any installed plugin `data.json` files for tokens, local database paths or account-specific metadata. **NOVA's included plugin config contains no login credentials.**
4. Do not distribute third-party plugins as copied binary files; direct recipients to the official plugin browser.
5. Share a **copy**, not your live study vault. Keep backups before applying new plugin versions or changing a template.

This repository ships only generic template content and settings, with **no** user course data, source PDFs, exam results, Zotero library content, API keys or Obsidian workspace history. For maintainers, follow the [GitHub publishing guide](GITHUB_PUBLISHING.md) before making a repository public.

**GitHub documentation layout:** The repository's `README.md` is the short project introduction written on GitHub. This complete guide stays at `docs/USER_GUIDE.md`. The link `[Read the Complete User Guide](docs/USER_GUIDE.md)` in the GitHub README opens this guide automatically. Maintain the two files separately: updating one does not automatically rewrite the other.

## 14. How to verify NOVA yourself

Use the following minimal smoke test:

1. Install Dataview and Tasks.
2. Copy `Course Starter` into `01 Courses` and fill the `course_name`, `semester`, `weekday` and time properties.
3. Check the Course Catalog and the correct weekday in the Weekly Timetable.
4. Add an undated task in the copied `Tasks/Tasks.md`. It should appear under **No due date** on the Task Dashboard.
5. Add a dated task with `📅` and verify it appears under upcoming or overdue, depending on date.
6. Create a new lecture note under that course's `Notes/`, insert **Lecture Note**, set `topic` and verify the Notes Index.
7. Fill `exam_date` and `exam_registered` in course Properties and check the Exam Dashboard.
8. Mark a task completed; verify it disappears from the open-task lists but the course's **Done** count increases (the completed checkbox stays in the original course file).
9. If Zotero is installed, import one reference and check both the Reading Library and the generated `persist` sections. Set `related_course` to the exact `course_name` and check the course's Related Reading section.
10. Change the course `status` to `archived`. It should move to the archived course and exam views and disappear from the active timetable.

**Need to modify the dashboards?** Their query source is plain text inside fenced `dataview` or `tasks` blocks. All folder names and properties are documented above; no other files need to be generated.

---

### Built on well-documented Obsidian features

- [Obsidian documentation](https://help.obsidian.md/)
- [Dataview documentation](https://blacksmithgu.github.io/obsidian-dataview/)
- [Tasks documentation](https://publish.obsidian.md/tasks/)
- [Zotero Integration Nunjucks templating](https://github.com/mgmeyers/obsidian-zotero-integration/blob/main/docs/Templating.md)

*Welcome to NOVA. Build one course, capture your next lecture, and grow the knowledge base as you go.*
