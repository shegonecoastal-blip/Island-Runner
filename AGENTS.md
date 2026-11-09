# Development Guidelines

These guidelines apply to development work in the Island Runner repository.

## Product and scope

- Follow approved requirements recorded by the Product Owner. Do not introduce, infer, or ship new product features without approved requirements.
- Treat `PRODUCT.md` as the product vision and `BACKLOG.md` as the record of approved and future work. If implementation details are unclear or a change would expand scope, ask the Product Owner before proceeding.
- Keep changes small and focused on the approved task.
- Do not add new dependencies, services, or automation workflows without explaining the tradeoffs and obtaining approval.

## Development workflow

- Before modifying code, check the current Git branch. Make development changes on an appropriate feature branch, not directly on `main`. If the current branch is `main`, stop and report that before editing code.
- Follow this release workflow: feature branch -> implementation -> testing -> Product Owner review -> explicit approval -> merge/publish.
- Do not merge or publish without explicit Product Owner approval. Never commit or push unless the user explicitly asks.

## User experience

- Prioritize a simple, accessible experience that works well on small screens and with assistive technology.
- Use clear language, semantic HTML, visible keyboard focus, and appropriately labeled controls.
- Avoid adding complexity or dependencies unless an approved requirement calls for them.

## Quality and production protection

- After code changes, proactively run relevant available tests and checks. Report which checks ran and their results, and identify tests that could not be performed. Never claim an unexecuted test passed.
- Protect production behavior and customer data. Avoid exposing secrets, changing production integrations, or altering submission and payment flows without explicit approved requirements.
- Preserve existing files and behavior outside the requested scope. In particular, do not modify `index.html` unless the user explicitly authorizes that change.

## Handoff

After every development task, provide a concise handoff summary with:

- Changes made.
- Files modified.
- Tests performed and results, including tests that could not be performed.
- Known issues or limitations.
- Acceptance criteria status.
