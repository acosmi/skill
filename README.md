# Acosmi Skill Registry

A curated open mirror of high-quality skills from the [Acosmi](https://acosmi.com) skill store. Each skill is a self-contained Markdown + JSON bundle that drops into the Acosmi agent stack — **CrabClaw** (desktop agent), **CrabCode** (coding agent CLI/GUI), or any runtime that follows the open SKILL.md convention.

## Quick Start

### Option A — Clone the whole registry

```bash
git clone https://github.com/acosmi/skill.git ~/acosmi-skill-registry
ls ~/acosmi-skill-registry/skills/
```

Symlink (or copy) any skill into the directory your CrabClaw / CrabCode client reads from:

```bash
ln -s ~/acosmi-skill-registry/skills/find_skills ~/.crabclaw/skills/find_skills
```

### Option B — Install one skill via CrabClaw CLI

```bash
go install github.com/acosmi/acosmi-sdk-go/cmd/crabclawskill@latest
crabclawskill install find_skills
# → installed to ~/.crabclaw/skills/find_skills/ (configurable, see `crabclawskill config`)
```

The CLI resolves by key against the live store at `https://acosmi.com` and downloads the same bundle that ships here.

### Option C — Raw file fetch

Every skill is plain Markdown + JSON. Fetch what you need:

```bash
curl -o SKILL.md https://raw.githubusercontent.com/acosmi/skill/main/skills/find_skills/SKILL.md
```

## Skill layout

Each skill lives at `skills/<key>/` and contains:

| File | Purpose |
| --- | --- |
| `SKILL.md` | YAML frontmatter + Markdown instruction body. This is the file the agent loads. |
| `README.md` | Human-readable documentation, examples, and edge cases. |
| `manifest.json` | Machine-readable metadata: key, name, version, author, category, license, tags. |
| `input-schema.json` | JSON Schema for skill inputs (optional). |
| `output-schema.json` | JSON Schema for skill outputs (optional). |

## License

All content in this registry is licensed under the [Apache License 2.0](./LICENSE) unless an individual skill's `manifest.json` declares otherwise. By submitting a skill to the Acosmi store you agree to release it under Apache 2.0 — see [CONTRIBUTING.md](./CONTRIBUTING.md).

## Provenance & AI disclosure

A subset of skills in the Acosmi store were drafted with LLM assistance during bootstrapping. To keep authorship honest, every machine-drafted skill carries `"author": "acosmi-bot"` in its manifest, and human-edited or human-authored skills carry the contributor's identifier. The `generatedBy` field in `manifest.json` reflects the source:

- `MANUAL` — written by a human contributor.
- `GENERATOR` — produced by the Acosmi skill generator.
- `IMPORT` — imported from a third-party catalog.

We deliberately do **not** publish skills with placeholder authors masquerading as named individuals.

## Sync cadence

This repo is updated nightly from the live Acosmi store. The sync window is roughly `02:00 UTC ±1h`. Each commit summarizes the skills changed since the previous run. See `scripts/sync-state.json` for the last sync watermark.

## Contributing

We do **not** accept pull requests directly against this repository — it is a generated mirror and edits would be overwritten on the next sync. Instead:

1. Sign up at [acosmi.com](https://acosmi.com) and publish your skill to the store.
2. Once your skill reaches `PUBLIC + APPROVED` status, the next nightly sync will mirror it here.
3. For corrections to an existing mirrored skill (typo, broken example), edit at source — the next sync will overwrite the file here.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full contribution and license-grant terms.

## Reporting issues

- Skill content bug (broken example, wrong schema): file at the source store, not here.
- Mirror/sync bug (missing skill, stale content): open an issue on this repo.

---

Mirror operated by [Acosmi](https://acosmi.com).
