# Public Documentation Instructions

This repository is the public TIMESAT GUI release repository. Its purpose is to host user-facing documentation, release notes, downloadable executable release information, examples, screenshots, and citation information.

## Repository Boundaries

The public repository must not contain:

- Private source code.
- Internal implementation details.
- Private repository names.
- Private file paths.
- Developer-only notes.
- Internal class names or function names.

The private TIMESAT GUI development repository may only be used as read-only reference. Do not modify the private development repository.

The private repository may be inspected only to understand user-facing GUI behavior, including:

- Visible windows, tabs, buttons, and menus.
- User-facing parameters.
- Input and output behavior.
- Common errors.
- Packaging and launch behavior.

Do not copy source code from the private repository.

Do not expose private paths, private repository names, internal class names, function names, or developer-only notes.

## Documentation Style

Write documentation for end users, not developers. Use formal, clear English suitable for scientific users.

Keep Markdown suitable for GitHub Pages:

- Use clear headings and short sections.
- Prefer relative links between documentation pages.
- Avoid local machine paths.
- Avoid developer-only comments.
- Mark uncertain information as `TODO: confirm`.

## Screenshots

Do not invent screenshots. Use screenshot placeholders only until verified public screenshots are available.

Screenshot placeholder paths must be under:

```text
docs/assets/screenshots/
```

When adding a screenshot placeholder, describe the intended public screenshot briefly and mark it as `TODO: confirm`.

## Preferred Documentation Structure

Use the following documentation structure unless there is a clear public documentation need to extend it:

```text
docs/index.md
docs/installation.md
docs/quick-start.md
docs/input-data.md
docs/parameters.md
docs/workflow.md
docs/output-results.md
docs/faq.md
docs/changelog.md
docs/screenshot-plan.md
```

## Review Checklist

Before proposing changes, confirm that:

- The content is user-facing.
- The Markdown is suitable for GitHub Pages.
- No private source code is included.
- No private implementation details are included.
- No private repository names or file paths are included.
- No internal class names or function names are included.
- No developer-only notes are included.
- Uncertain information is marked as `TODO: confirm`.
- Screenshot references are placeholders under `docs/assets/screenshots/` unless real public screenshots have been supplied.
