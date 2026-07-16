# Learning Library Project Specification

## Purpose

This repository contains the complete authoring system for the Learning Library.

The goal is to create expandable educational HTML lessons that can be iteratively improved over time without rewriting existing content.

---

# Repository Structure

learning-library/

    textbooker/
        PROJECT_SPEC.md
        START-HERE.md

        config/
            ruleset.json

        docs/
            author-guide.md
            CHANGELOG.md

        templates/
            lesson-template.html

        snippets/

        css/

        js/

    lessons/

---

# Responsibilities

PROJECT_SPEC.md

Defines the structure of the entire project.

ruleset.json

Defines how lessons are built.

lesson-template.html

Defines the starting HTML structure for every lesson.

author-guide.md

Explains how to use the authoring system.

CHANGELOG.md

Records changes to the authoring system.

START-HERE.md

Quick reference for using the project.

---

# Design Principles

- One source of truth for each type of information.
- Lessons are permanently expandable.
- Existing lesson content is preserved.
- Templates reduce repetitive work.
- The repository should be self-documenting.

---

# Updating the Project

When changing the authoring system:

1. Upload the current project files.
2. Describe the desired change.
3. Review the proposed changes.
4. Approve the changes.
5. Replace the affected files.
6. Update the CHANGELOG.