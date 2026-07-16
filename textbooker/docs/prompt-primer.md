# Learning Library Prompt Primer

This project follows the Learning Library Expandable Authoring Standard, LL-EAS v4.

When creating a new lesson:

- Follow `config/learning-library-expandable-html-ruleset-v4.json`.
- Start from `templates/lesson-template.html`.
- Keep the first draft compact and clear.
- Every navbar must include the Course Index link:
  https://kevinlinstrum001.github.io/learning-library/
- Every section must end with smart learning-prompt cards for explanation and practice.
- Add a visual learning-prompt card when a visual exists or is planned.
- Use accessible inline SVG for diagrams, systems, mappings, processes, and relationships.
- For optional non-diagram artwork, insert a placeholder using:
  `document_name_image01.png`
- Preserve stable IDs, classes, figure names, and image filenames.
- Expansion responses must contain only the new HTML fragment to paste immediately before the matching card.
- Do not regenerate or rewrite the entire page during an expansion.
