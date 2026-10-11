# 🧠 Glossary & Knowledge Base

[[START HERE|← Home]] · [[04 Library/Reading Library|Reading library]]

Create one note per durable concept under `05 Knowledge Base/Concepts` with the **Concept Note** template. Use Obsidian `[[wikilinks]]` to connect related ideas; a glossary term can then link to its own detailed note.

## Concept notes (automatic)

```dataview
TABLE WITHOUT ID
  file.link AS "Concept",
  summary AS "Summary",
  related_course AS "Course"
FROM "05 Knowledge Base/Concepts"
WHERE type = "concept"
SORT file.name ASC
```

## Quick glossary

| Term | Short explanation | Detailed note or source |
|---|---|---|

> [!tip] Permanent notes
> Write each concept in your own words and include a source. Link concepts to papers and lecture notes when relevant.
