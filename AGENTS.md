# Sonotide docs agent guide

Use this file to understand the documentation project quickly before editing it.

## What this repo is

- This is the Mintlify documentation site for the Sonotide framework.
- Pages are MDX files with YAML frontmatter.
- Global site configuration lives in `docs.json`.
- Shared branding and presentation live in `styles.css`, `scripts.js`, `favicon.svg`, and `logo/`.

## Repository shape

- `en/` contains the English documentation tree.
- `ru/` contains the Russian documentation tree.
- `en/` and `ru/` should stay structurally aligned unless there is a strong reason not to.
- `index.mdx` remains the language landing page at the top level.
- Within each language tree, content is grouped by section:
  - `start/` for setup and build entry points
  - `core/` for concepts and feature areas
  - `guides/` for migration and troubleshooting
  - `reference/` for API-style material
  - `examples/` for overview pages and per-example walkthroughs
- `examples/overview.mdx` is the landing page for the examples section.

## How to think about Sonotide here

- Write about Sonotide as an independent C++ audio framework, not as a sample app.
- Prefer real Sonotide API names such as `runtime`, `render_stream`, and `playback_session`.
- Treat the framework repo as the source of truth for behavior.
- Do not invent API behavior, unsupported platform claims, or hidden features.

## Writing style

- Use active voice and second person when giving guidance.
- Keep headings in sentence case.
- Keep paragraphs short and concrete.
- Prefer explanation over marketing language.
- Use code formatting for commands, file paths, type names, API names, and code identifiers.
- Use bold only for UI labels or emphasis that genuinely helps scanning.

## Terminology

- Always use the product name `Sonotide`.
- Use “framework” rather than “app” when describing the product itself.
- Use “render”, “capture”, “loopback”, “runtime”, and “playback session” consistently with the codebase.
- Do not replace concrete API names with vague paraphrases if the exact name is known.

## Localization rules

- Keep English and Russian page sets aligned in purpose and navigation.
- If you add a page in `en/`, add the matching page in `ru/`.
- If you rename, split, or reorder pages in one language, mirror that change in the other language.
- Keep localized copy natural, but preserve the same technical meaning and page structure.

## Navigation and page organization

- Update `docs.json` whenever you add, remove, rename, or reorder pages.
- Keep file layout and `docs.json` in sync. Do not move pages without updating navigation.
- Keep overview pages short when a section has grown large; push deep content into dedicated pages.
- Prefer one focused page per example or scenario over one oversized catch-all page.

## Content boundaries

- Document public behavior, usage patterns, build steps, troubleshooting, and architecture.
- It is fine to explain internal concepts when they help users understand the public API.
- Do not document speculative roadmap items as if they already exist.
- Do not duplicate the same explanation across multiple pages unless repetition improves wayfinding.

## Examples guidance

- Examples should teach a realistic task, not just dump code.
- Explain what each important call does and why it appears in that order.
- Use full, coherent snippets when the page is a walkthrough.
- Keep examples grounded in the real Sonotide API surface.

## Where to put changes

- Navigation, tabs, and sidebar structure: `docs.json`
- Shared visual styling: `styles.css`
- Shared client-side behavior: `scripts.js`
- Landing pages: `index.mdx`, `en/index.mdx`, `ru/index.mdx`
- Page content: `en/**/*.mdx` and `ru/**/*.mdx`
- Branding assets: `logo/` and `favicon.svg`

## Verification

- Preview locally with `mint dev`.
- Check links with `mint broken-links`.
- If Mintlify fails to run, verify the local Node version first. Mintlify expects an LTS Node release, not Node 25+.
- Before finishing, make sure new pages exist in both languages when required and that `docs.json` references the correct paths.

## What to avoid

- Template filler, placeholder notes, or generic AI-sounding copy.
- Mismatched English and Russian navigation trees.
- Large cosmetic style edits when the task is purely editorial.
- Claims that are not backed by the Sonotide codebase or docs.
