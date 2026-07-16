# Learning Library Expandable Authoring Standard

The Learning Library Expandable Authoring Standard (LL-EAS) defines the structure, navigation, metadata, accessibility, visual, and expansion requirements for Learning Library course and lesson pages.

The standard is designed around a simple principle:

> Every document should teach its core idea clearly while remaining permanently expandable.

The ruleset applies to complete course pages, lesson pages, diagrams, image placeholders, embedded metadata, navigation, and permanent learning-prompt cards.

## Current version

**LL-EAS 4.5**

The current ruleset file is:

```text
ruleset-v4.5.json
```

## Core authoring principles

- Keep first drafts compact and useful.
- Preserve existing content during later expansion.
- Insert new semantic HTML fragments before permanent learning-prompt cards.
- Do not rewrite the entire page when expanding one section.
- Use accessible inline SVG for diagrams.
- Use reserved image placeholders for later raster-image generation.
- Keep every page usable without JavaScript.
- Preserve readable print output.
- Maintain clear navigation between the Learning Library, course overview pages, and lessons.

## Required document structure

Course and lesson pages should include:

- embedded JSON metadata;
- a reading-progress indicator;
- a persistent navigation bar;
- a header or hero area;
- an optional table of contents;
- the main educational content;
- permanent expansion prompts;
- footer navigation.

## Expansion model

Each section remains expandable through permanent prompt cards.

Typical prompt types include:

- explanation;
- practice;
- visual.

Expansion prompts must request only the new semantic HTML fragment. They must preserve existing IDs, classes, content, and insertion locations.

---

# v4.5

Version 4.5 is a minor delivery and workflow update built on the navigation changes introduced in version 4.4.

## Latest changes

### ZIP delivery for complete HTML documents

Complete downloadable HTML documents must now be delivered inside ZIP archives rather than as raw HTML downloads.

This requirement exists to:

- preserve the exact intended repository filename;
- prevent browser or platform renaming;
- reduce manual file-renaming work;
- reduce the chance of path and filename typographical errors.

For example:

```text
course-06-systems-operations-and-control.zip
```

should contain:

```text
course-06-systems-operations-and-control.html
```

The HTML file should appear exactly once inside the archive and should retain its intended repository filename.

### ZIP validation requirements

Before delivery, the archive should be checked to confirm that:

- the ZIP opens successfully;
- the expected HTML filename is present exactly once;
- the HTML is encoded as UTF-8;
- linked asset paths were not rewritten unintentionally.

### Exceptions to ZIP delivery

The ZIP rule does not apply when:

- an expansion prompt requests an HTML fragment only;
- the user explicitly requests inline source code;
- the user explicitly requests another delivery format.

### Navigation rules retained from v4.4

Version 4.5 retains the navigation distinction introduced in version 4.4:

- **Learning Library** refers to the site-level course catalog.
- **Course Overview** refers to the overview page for a lesson's own course.

Course overview pages must include a visible Learning Library link.

Lesson pages must include:

1. Learning Library;
2. Course Overview.

These labels must not be used interchangeably.

### Metadata retained from v4.4

Course and lesson metadata should include:

```json
{
  "site_home": "https://kevinlinstrum001.github.io/learning-library/",
  "course_overview": null
}
```

For lesson pages, `course_overview` should contain the relative or absolute URL of the lesson's course overview page.

### Migration guidance

Existing HTML content does not need to be rewritten solely because of version 4.5.

To migrate a document:

1. Update `authoring_standard` to `LL-EAS 4.5`.
2. Add or verify `site_home`.
3. Add or verify `course_overview`.
4. Ensure navigation follows the course-page or lesson-page contract.
5. Preserve all existing content, IDs, classes, links, visuals, and expansion cards.
6. Deliver the completed HTML file inside a ZIP archive using its exact repository filename.

## Validation additions in v4.5

A conforming workflow should verify that:

- complete downloadable HTML documents are delivered in ZIP archives;
- the exact repository filename is preserved;
- every course and lesson page includes a Learning Library link;
- every lesson page includes a Course Overview link;
- Learning Library and Course Overview are labeled distinctly;
- persistent navigation links open in the same tab.

---

## Version history

### v4.5

Added ZIP delivery and validation requirements for complete downloadable HTML documents.

### v4.4

Separated site-level Learning Library navigation from course-level Course Overview navigation and added corresponding metadata requirements.

### v4.3

Established the expandable authoring structure, permanent prompt-card workflow, accessible SVG rules, metadata requirements, and preservation-first expansion model.
