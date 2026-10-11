# {{title}}

type:: paper
title:: {{title}}
authors:: {{authors}}
{% if date %}year:: {{date | format("YYYY") }}{% endif %}
citekey:: {{citekey}}
{% if DOI %}doi:: {{DOI}}{% endif %}

> [!info] Reference information
> **Authors:** {{authors}}
> **Publication:** {{publicationTitle}}
> **Zotero:** [Open item]({{desktopURI}})
{% if DOI %}> **DOI:** [{{DOI}}](https://doi.org/{{DOI}}){% endif %}

> [!cite]- Formatted bibliography
> {{bibliography}}

{% if abstractNote %}
## Abstract

{{abstractNote}}
{% endif %}

## My reading notes and course connections

{% persist "reading-notes" %}{% if isFirstImport %}
reading_status:: unread
related_course::

### Research question / purpose

### Methods and data

### Main findings

### Why this source matters

### Critical reflection and questions

{% endif %}{% endpersist %}

## PDF highlights and comments

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% for a in newAnnotations %}
{% if a.annotatedText %}
> [!quote]- Page {{a.pageLabel}}
> {{a.annotatedText}}
{% endif %}
{% if a.comment %}
> **Comment:** {{a.comment}}
{% endif %}
{% endfor %}
{% endpersist %}
