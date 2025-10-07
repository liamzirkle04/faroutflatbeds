This is a Shopify Liquid theme.

## Development Commands

- `shopify theme dev --store=<store-domain>` spins up the local preview tunnel for rapid iteration. The store we're using is "esuwzi-3q.myshopify.com".
- `shopify theme check` runs Liquid linting—fix all offenses before committing. The Shopify dev server will sometimes show derivative errors in the frontend if there are linting errors, so if the user comes to you requesting an error be fixed, linting is a good first step.

## Coding Style & Naming Conventions

- Follow Liquid’s two-space indentation and wrap logic with `{% liquid %}` for multi-line assigns or conditionals.
- Use semantic, kebab-case class names (e.g., `fof-feature-card`) and keep dynamic styles out of `{% stylesheet %}` blocks—inject runtime values via inline style attributes instead.
- Centralize copy strings in `locales/en.default.json`; reference them in templates with `{{ 'key' | t }}`.

## Testing Guidelines

- Theme Check is the primary static analysis tool; address accessibility warnings (e.g., width/height on images) immediately.
- Verify storefront rendering by checking with the user. You can ask them to verify things visually or even provide screenshots.
