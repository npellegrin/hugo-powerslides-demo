# Agent Instructions

## Project

- Demo site for the `hugo-powerslides` Hugo theme, linked to the neighboring repository through `replace` in `go.mod`.
- Put editorial content in `content/` and configuration in `hugo.toml`. Do not edit generated files in `public/`.
- For shared theme behavior or styling, edit `../hugo-powerslides` instead of duplicating its templates or assets here.
- Write all project-authored material in English, including code comments, documentation, slide content, and user-facing text, unless explicitly asked otherwise.

## Efficient Work

- Keep investigation and responses concise. Read only the files needed to understand the change; avoid repeated searches, rereads, and restating context.
- Make the smallest complete change and run the narrowest useful check.
- Do not add comments that repeat what the code does. Comment only to clarify non-obvious intent or constraints.

## Hugo and Content

- Use the theme's documented shortcodes and conventions. Keep slide IDs stable for direct links.
- Write clear Markdown with a consistent heading hierarchy, useful alternative text, and descriptive link labels.
- Keep Hugo configuration minimal and aligned with the local module. Add no dependency or override without a concrete need.

## Design and Accessibility

- Demonstrate real theme usage; keep slides readable in projection and responsive on small screens.
- For added colors, meet WCAG contrast ratios: at least 4.5:1 for normal text and 3:1 for large text and relevant UI components.
- Never distinguish content or states through color alone. Add a shape, label, pattern, or icon, and check usability for users with color-vision deficiencies.
- Preserve semantic HTML, text alternatives, visible focus, keyboard operation, and reduced-motion support.

## Verification

- Run `hugo` from this directory to build with the local theme; use `hugo server` for visual checks.
- After content or presentation changes, check links, slide anchors, and mobile layout.