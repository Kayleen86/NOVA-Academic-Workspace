# 📚 Reading Library

[[START HERE|← Home]] · [[04 Library/Links & Resources|Resources]] · [[05 Knowledge Base/Glossary|Knowledge base]]

> [!info] Automatic bibliography
> **Zotero Integration** imports a paper into `04 Library/Zotero Papers` using `07 Templates/Zotero Import Template.md`. The note includes Dataview-readable metadata, so it appears here automatically. Manual reading notes from the **Reading Note** template work too.

## Zotero papers

```dataview
TABLE WITHOUT ID
  link(file.path, choice(title, truncate(title, 65), file.name)) AS "Paper",
  authors AS "Authors",
  year AS "Year",
  related_course AS "Related course",
  reading_status AS "Status"
FROM "04 Library/Zotero Papers"
WHERE type = "paper"
SORT year DESC, file.name ASC
```

## Other reading notes

```dataview
TABLE WITHOUT ID
  file.link AS "Source",
  authors AS "Authors",
  year AS "Year",
  related_course AS "Related course",
  reading_status AS "Status"
FROM "04 Library/Reading Notes"
WHERE type = "reading-note"
SORT file.name ASC
```

## Reading workflow

1. Import a Zotero item, or create a note in `Reading Notes` using the **Reading Note** core template.
2. Change `reading_status` from `unread` to `reading` or `read`.
3. Set `related_course` to **exactly** the `course_name` shown in that course's Overview if you want the course's related-reading list to pick it up.
4. Write your summary, method, results and own thoughts. Cite original pages for direct quotations.

> [!warning] Re-importing Zotero items
> User-written text belongs **inside the generated `%% begin ... %%` / `%% end ... %%` blocks**. Those sections are preserved by Zotero Integration; changing metadata outside them may be overwritten on the next import.
