# 📚 All Course Materials

[[START HERE|← Home]] · [[01 Courses/Course Catalog|Course catalog]] · [[08 Attachments/Unsorted Attachments|Unsorted attachments]]

Automatically lists **PDFs from the `Materials/` directories of all courses**, grouped by course folder. Visit a course's **Overview → Course materials** for all types of files, including Markdown cheat sheets and images.

```base
filters:
  and:
    - 'file.inFolder("01 Courses")'
    - 'file.folder.contains("/Materials")'
    - 'file.ext == "pdf"'
formulas:
  material: 'file.asLink(file.name)'
properties:
  formula.material:
    displayName: "PDF"
  file.folder:
    displayName: "Course / materials folder"
views:
  - type: table
    name: "PDFs by course"
    groupBy:
      property: file.folder
      direction: ASC
    order:
      - formula.material
      - file.folder
```

**Add a course PDF:** Save it under `01 Courses/<YOUR COURSE>/Materials/`. It then appears both here and on the matching course Overview. The global `08 Attachments/` directory is for pasted images and unassigned files, not course handouts.
