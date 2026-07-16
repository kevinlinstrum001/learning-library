# Learning Library Author Guide

## Purpose

The Learning Library uses expandable HTML lessons. A lesson is not expected to be complete on its first draft. It should explain the core idea clearly and retain permanent prompts for deeper explanation, practice, and visuals.

## Working method

1. Open the lesson HTML in VS Code.
2. Preview it with Live Server or Live Viewer.
3. Read one section at a time.
4. When more detail is needed, open the relevant learning-prompt card.
5. Copy the prompt into ChatGPT.
6. During the original creation conversation, the existing context may be enough.
7. During a later conversation, paste the current section HTML beneath the copied prompt.
8. Request an HTML fragment only.
9. Paste the returned fragment immediately before the matching learning-prompt card.
10. Save the file and refresh the preview.
11. Leave the learning-prompt card in place so the section can be expanded again.

## Required section ending

Every section ends with:

- Expand explanation
- Expand practice
- Expand visual, when a visual exists or is planned

Practice problems are demand-driven. The first draft does not need a large permanent problem set.

## Smart prompts

Each learning prompt should name its section and topic. It must say:

- preserve existing IDs and CSS classes;
- do not remove or rewrite existing content;
- return only semantic HTML;
- insert immediately before this card.

## Visual policy

Use inline SVG when the visual explains structure, sequence, mappings, systems, or relationships.

Use an image placeholder when an optional illustration may be useful later. Reserve filenames in document order:

`document_name_image01.png`

`document_name_image02.png`

Keep the reserved filename unchanged when the real image is generated.

## Navigation

Every navbar must contain a visible link to:

https://kevinlinstrum001.github.io/learning-library/

The footer should repeat the Course Index link and may include Back to top, Previous lesson, and Next lesson.

## Project files

- `config/` contains machine-readable rules and the project manifest.
- `templates/` contains canonical reusable HTML.
- `docs/` contains human-readable workflow and prompt guidance.
- Individual lesson folders may contain their HTML and an `images/` subfolder.
