# Contributing

Thanks for helping improve `travel-photo-sort-edit`.

This project is a Codex skill, so the most important rule is: keep the agent instructions useful, concise, and safe.

## Good Contributions

- Clarify the plan-first workflow.
- Improve JPG+RAW/NEF pairing and mismatch handling.
- Add safer validation steps.
- Improve guidance for natural skin tones, cohesive travel color palettes, and better post-ready image quality.
- Add support notes for additional RAW formats or editing tools.
- Add small, non-private examples that explain expected outputs.

## High Priority: Editing Quality

The current skill is strongest at safe sorting, culling, pairing, and preservation. Its image-editing guidance still needs more real-world testing and better recipes.

Please contribute ideas that make edited outputs feel more beautiful, natural, and emotionally coherent, especially for:

- skin tones that stay warm and believable;
- local face and subject adjustments instead of flat global brightening;
- romantic travel color palettes that work across a full set;
- tone curves, HSL, and white balance guidance;
- practical validation for spotting chalky faces, harsh contrast, or inconsistent colors.

## Before You Open A Pull Request

1. Keep `SKILL.md` focused on what Codex needs at runtime.
2. Put user-facing explanation in `README.md`, not in `SKILL.md`.
3. Do not commit personal photos, RAW files, exported edits, contact sheets, or manifests.
4. Do not add workflows that delete, overwrite, upload, or publish user photos without explicit approval.
5. Update `agents/openai.yaml` if the skill purpose or default prompt changes.
6. Add a note to `CHANGELOG.md` for user-visible changes.

## Style

- Use direct, practical language.
- Prefer checklists and short workflow steps.
- Use ASCII unless a file already needs another character set.
- Keep examples generic and privacy-safe.
- Avoid tool-specific promises unless the workflow has been tested.

## Validation

Before submitting:

```bash
git status -sb
```

If you have access to the Codex skill validation helper, run it against this folder:

```bash
scripts/quick_validate.py .
```

If the validator is unavailable, manually check:

- `SKILL.md` has valid YAML frontmatter with `name` and `description`.
- The skill folder name matches the `name`.
- `agents/openai.yaml` still describes the skill accurately.
- No personal photo artifacts are staged.

## Pull Request Checklist

- [ ] The change preserves original-photo safety.
- [ ] The change keeps JPG and RAW/NEF pairing explicit.
- [ ] The change does not add destructive behavior without approval.
- [ ] The change keeps `SKILL.md` concise.
- [ ] The change includes docs or changelog updates when useful.
