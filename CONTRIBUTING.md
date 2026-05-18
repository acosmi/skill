# Contributing to the Acosmi Skill Registry

This repository is a **read-only generated mirror** of the live skill store at [acosmi.com](https://acosmi.com). All authoring happens at the source; this README explains how to get your skill into the mirror, what license terms apply, and how AI-assisted contributions are handled.

## How to contribute a skill

1. Create an account at [acosmi.com](https://acosmi.com).
2. Build a skill using the in-app skill generator, the desktop CrabClaw client, or the `crabclawskill publish` CLI command. Your skill must include:
   - A unique `key` (lowercase, underscore-separated).
   - A non-empty `name` and `description`.
   - A `SKILL.md` body with valid YAML frontmatter (the generator does this automatically).
3. Publish it to the public store. Once it passes review (`status: APPROVED`, `visibility: PUBLIC`), it enters the curation pool.
4. Curation runs nightly. The criteria are documented in [`scripts/sync-state.json`](./scripts/sync-state.json); roughly: real author identifier, non-trivial description, and either a non-zero download count or inclusion in the protected high-value set.
5. If your skill is selected, it appears in `skills/<your-key>/` on the next sync. If it isn't, raise an issue on this repo with the skill key and the curation criterion you believe it meets.

## License grant

By publishing a skill to the public Acosmi store, you grant Acosmi and the broader open-source community a perpetual, worldwide, non-exclusive, royalty-free license to redistribute and adapt the skill under the [Apache License 2.0](./LICENSE).

If your skill must ship under a different license (e.g., MIT, CC-BY), set the `license` field in your skill's manifest at publish time. The mirror will honor that declaration; skills without an explicit license declaration are treated as Apache 2.0.

## AI assistance disclosure

We expect that many skills are drafted with LLM help. That's fine and welcome. To keep authorship honest:

- If your skill was generated end-to-end by an LLM with minimal human review, set `author: "acosmi-bot"` and `generatedBy: "GENERATOR"`. Do **not** put a fabricated human name in the author field.
- If you reviewed and edited a machine draft into shape, attribute yourself in `author`. Reviewing IS authoring.
- Pre-existing skills that were bulk-imported with placeholder authors are excluded from this mirror by design.

## Editing a mirrored skill

You cannot fix a skill by opening a pull request here — the file will be overwritten on the next sync. Instead:

1. Edit at the source (acosmi.com or the CrabClaw desktop client).
2. Bump the version (`1.0.0` → `1.0.1`).
3. Wait for the next nightly sync, or contact ops to trigger an immediate sync.

## Reporting problems with the mirror itself

If a skill is missing, a file is malformed, or the sync appears stuck, open an issue here with:

- The skill `key` (if relevant).
- The expected vs actual state.
- A timestamp.

## Code of conduct

Be kind. Skills can do real damage on a user's machine — review your prompts and tool allow-lists carefully before publishing.
