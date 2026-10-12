# 📥 Unsorted Attachments

[[START HERE|← Home]] · [[01 Courses/All Course Materials|All course PDFs]]

This shared folder is the default destination for **pasted images** and files that have not yet been assigned to a course.

**For PDFs and lecture materials belonging to a course:** Move or copy them into that course's own `Materials/` folder. They will then appear automatically on the course Overview and (for PDFs) in the global course-materials index.

```base
filters:
  and:
    - 'file.inFolder(this.file.folder)'
    - 'file.ext != "md"'
formulas:
  attachment: 'file.asLink(file.name)'
properties:
  formula.attachment:
    displayName: "File"
  file.ext:
    displayName: "Type"
views:
  - type: table
    name: "Unsorted files"
    order:
      - formula.attachment
      - file.ext
```

> [!note] Pasted images
> Obsidian may save pasted images in `08 Attachments` by default. That's fine. Move only files you want associated with a specific course. Obsidian normally updates links when files are moved using its own File explorer, provided **Automatically update internal links** is enabled.
