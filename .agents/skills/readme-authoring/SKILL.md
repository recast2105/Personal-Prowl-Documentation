---
name: readme-authoring
description: Create, improve, translate, and maintain repository README files using clear, conventional Markdown structure. Use when documenting a project's purpose, contents, setup, usage, links, images, or language variants; preserve verified facts and validate relative links.
---

# Repository README Authoring

When asked to create or update a repository README, follow these instructions. Treat the README as the project's landing page for people browsing the repository and for AI tools that need a concise, reliable project overview.

## Before editing

1. Read the existing README and inspect the relevant project files so descriptions, commands, features, and links are grounded in the repository.
2. Identify the intended audience, supported languages, and whether the README is for a library, application, documentation collection, or another project type.
3. Do not invent setup steps, features, compatibility claims, badges, licenses, status, or guarantees. If important facts are unavailable, omit them or ask the user when necessary.
4. Make focused changes. Preserve useful existing content and do not modify unrelated files or Git configuration, history, remotes, or other Git-related settings.

## Recommended structure

Adapt the sections to the project; do not add empty or irrelevant headings. A typical README uses this order:

1. **Project name** — a concise H1 title.
2. **Summary** — what the project is, what it is for, and who it serves, in a few sentences.
3. **Status or scope note** — include only when needed to explain that content is experimental, unofficial, incomplete, or otherwise limited.
4. **Contents or features** — a scannable list linking to the most useful areas of the repository.
5. **Getting started / usage** — include only verified steps and commands when applicable.
6. **Configuration or requirements** — include only when relevant and confirmed.
7. **Images and assets** — explain asset locations or usage when images are important to understanding the project.
8. **Contribution, support, license, or acknowledgements** — include only when the repository provides verified information or the user requests it.

Keep the opening concise. Prefer descriptive headings, short paragraphs, and lists over long blocks of prose. Use fenced code blocks for commands and code, with a language identifier where applicable.

## Markdown and links

- Use standard Markdown that renders in common repository viewers, including GitHub.
- Use relative links for files and folders inside the repository. Encode spaces and special characters in link destinations when needed (for example, `%20` and `%28`).
- Link to existing files only. Resolve each relative link from the directory containing the Markdown file and confirm that its target exists.
- For images, use standard syntax with useful alternative text: `![Description of the image](relative/path/image.png)`. Do not use editor-specific embeds such as Obsidian's `![[image.png]]` when broad compatibility is expected.
- Keep image paths relative to the README or document that embeds them. Do not use local absolute paths, machine-specific paths, or remote image URLs unless the user explicitly wants them.
- Do not assume an image will be available to repository visitors unless its file is included in the repository. Mention asset folders where useful.
- Ensure links between language versions and links in contents lists point to the actual filenames and locations.

## Multiple languages

- Keep each language version semantically equivalent: preserve caveats, scope, navigation, and factual details in translation.
- Use a clear language switch near the top of each README, linking to the other version with a relative path.
- Use consistent, recognizable names for language variants, such as `README.md` for the primary language and `README.en.md` for English (a language-code suffix before `.md`) when that convention is already in use. Follow the repository's established naming convention rather than renaming files without need.
- Translate explanatory prose naturally; preserve product names, code identifiers, commands, and technical terms when translation would reduce clarity.
- When updating one version, check whether the corresponding translation also needs updating. Do not silently leave conflicting information between languages.

## Validation and completion

1. Re-read the resulting README files for spelling, clarity, consistent heading levels, and accurate claims.
2. Check every local file, folder, and image link in the edited README(s); confirm the target exists after URL-decoding encoded path characters.
3. Confirm images use portable relative links and that no editor-specific embed syntax remains in the edited README(s).
4. Report which files were changed and which checks were performed. State clearly if any check could not be completed.
5. Do not run Git commands or change Git-related settings unless the user explicitly requests it.
