# Learning Library Authoring System Changelog

All notable changes to the Learning Library Authoring System are documented in this file.

The format is based on semantic versioning of the authoring system itself, not the lessons it produces.

---

# Version 4.1

**Release Date:** YYYY-MM-DD

## Purpose

Introduce project-wide variables to eliminate duplicated configuration values and establish a single source of truth for project-wide settings.

## Files Updated

- `textbooker/config/ruleset.json`

## Added

### Project Variables

Added a new top-level `project_variables` section containing:

- `SITE_NAME`
- `SITE_ROOT_URL`
- `COURSE_INDEX_URL`
- `LESSON_STYLESHEET_PATH`
- `IMAGE_DIRECTORY`
- `DEFAULT_LANGUAGE`

## Changed

### Site Configuration

- `site.name` now references `SITE_NAME`.
- `site.course_index_url` now references `COURSE_INDEX_URL`.

### Navigation

- Navbar rules now reference `COURSE_INDEX_URL` instead of embedding a hard-coded URL.
- Navbar HTML now uses a project variable placeholder instead of a fixed URL.

### Image Configuration

- Image placeholder rules now reference `IMAGE_DIRECTORY` instead of embedding `"images/"`.

### Version

- Updated authoring system version from **4.0** to **4.1**.

## Breaking Changes

None.

Existing lessons remain valid.

The new variable system applies to newly generated lessons and to templates updated to support project variables.

---

## Future Work

- Update `lesson-template.html` to consume project variables.
- Continue replacing duplicated configuration values with project variables where appropriate.
- Investigate additional project-wide variables that reduce maintenance overhead while keeping the ruleset readable.