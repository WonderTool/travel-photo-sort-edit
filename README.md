# Travel Photo Sort Edit

`travel-photo-sort-edit` is a Codex skill for safely sorting, culling, preserving, and lightly editing travel photo folders.

It is built for trips where you want a small set of polished, post-ready images and a larger set of meaningful core-memory keepers, while keeping JPG and RAW/NEF pairs together and protecting originals.

## Current Status: Please Test And Improve

The culling and preservation workflow is useful now, but the image-editing quality is still limited. In particular, automated edits can miss the nuance of skin tones, local contrast, color balance, and the emotional mood of a travel set.

Please try it on real but privacy-safe photo folders, compare the outputs with your own editing taste, and contribute better prompts, validation checks, editing recipes, or tool-specific workflows. The goal is to make this skill genuinely helpful for romantic, beautiful, post-ready travel sets instead of just producing "technically edited" images.

## What It Helps With

- Plan-first travel photo culling with user-approved counts.
- JPG+RAW/NEF pairing by filename stem.
- Contact sheets, manifests, mismatch reports, and reviewable selections.
- Balanced post-ready and core-memory picks across portraits, landscapes, architecture, details, and travel moments.
- Non-destructive organization under a sorting workspace such as `_photo_sort/`.
- Cohesive, skin-safe travel edits with natural faces, intentional crops, local adjustments, HSL tuning, tone curves, and perspective correction.
- Disk-space cleanup planning that moves or deletes extras only after explicit approval.

## Why This Exists

Travel photo culling is easy to make messy: originals can get moved, RAW pairs can be separated, faces can get over-brightened, and one beautiful scene can crowd out the full story of the trip.

This skill gives Codex a repeatable workflow that is calm, explicit, and reviewable. It favors preservation first, edit copies only, and human approval before cleanup.

## Install

Clone the repo into your Codex skills folder:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/WonderTool/travel-photo-sort-edit.git "${CODEX_HOME:-$HOME/.codex}/skills/travel-photo-sort-edit"
```

Then restart Codex so it can discover the skill.

## Use

Ask Codex something like:

```text
Use travel-photo-sort-edit to sort this trip folder. I want 20 post-ready pictures and 50 core-memory keepers. Keep JPG and NEF pairs together, make contact sheets first, and do not delete anything without asking.
```

The skill should start in a planning step by asking or confirming:

- how many post-ready pictures you want;
- how many core-memory pictures you want;
- what story or color palette the edits should communicate.

## Workflow Summary

1. Inventory the folder read-only.
2. Pair JPG and RAW/NEF files by filename stem.
3. Flag mismatches clearly.
4. Build contact sheets and manifests for review.
5. Rank and curate for quality, memory value, portraits, landscapes, and variety.
6. Organize selected source pairs non-destructively.
7. Edit only copies for post-ready outputs.
8. Validate counts, pairs, manifests, and edited files.
9. Propose cleanup only after the user reviews the selections.

## Privacy And Safety

Do not commit personal photo folders, RAW files, contact sheets, manifests, or edited exports to this repository.

The skill is designed to work locally. It should not upload private photos to third-party services unless the user explicitly requests that workflow and understands the destination.

## Repository Layout

```text
.
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
|-- README.md
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- CHANGELOG.md
`-- LICENSE
```

## Contributing

Contributions are welcome, especially improvements to:

- safer culling and pairing workflows;
- better contact sheet and manifest conventions;
- skin-safe, cohesive travel editing guidance and higher-quality post-ready outputs;
- validation checklists;
- support for additional RAW formats;
- examples that do not include private or identifying photos.

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

MIT. See [LICENSE](LICENSE).
