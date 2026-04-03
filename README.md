# Sonotide docs

This repository contains the Mintlify site for the Sonotide framework.

## What lives here

- `docs.json` for global site configuration;
- localized content under `en/` and `ru/`;
- section folders inside each locale: `start/`, `core/`, `guides/`, `reference/`, and `examples/`;
- branding assets in `logo/`, `favicon.svg`, and optional `images/`;
- styling in `styles.css` and optional `scripts.js`.

## Local preview

```bash
npm i -g mint
mint dev
```

If you use the Windows preset workflow from the framework repo, keep this
documentation repo open in a separate terminal so the navigation and page
structure stay easy to verify.

## Writing rules

- Keep the text factual and concrete.
- Prefer the actual Sonotide API names over paraphrases.
- Keep English and Russian sections aligned in structure.
- Avoid starter-kit filler or marketing copy.
