---
name: travel-photo-sort-edit
description: Plan-first workflow for sorting, culling, preserving, and lightly editing travel photo folders, especially JPG+RAW/NEF shoots. Use when the user asks to sort photos, cull trip pictures, pick post-ready images, choose core-memory keepers, save disk space from a photo folder, pair JPG and RAW files, create contact sheets/manifests, or apply a cohesive travel/photo-story edit across selected images.
---

# Travel Photo Sort Edit

Use this skill to turn a travel photo folder into a safe, reviewable set of post-ready images and core-memory keepers. The workflow is deliberately plan-first and non-destructive.

## Plan First

Before executing any file changes, ask or confirm:

1. How many post-ready pictures should be selected?
2. How many core-memory pictures should be preserved?
3. What story or palette should the edits communicate? If the user does not specify, propose a cohesive palette based on the trip, such as warm rose-gold highlights, natural skin, softened blues, sage greens, and gentle contrast for a romantic trip.

Describe the process to the user before executing:

- read-only inventory and JPG+RAW pairing;
- contact sheets and review gallery;
- first-pass ranking and human/visual curation;
- non-destructive keeper organization;
- skin-safe cohesive edits;
- validation counts and mismatch report;
- no deletion until explicit approval.

If Plan Mode is active, complete this as a `<proposed_plan>` before implementation. If Plan Mode is not active, still pause after the process description if the user has not already approved execution.

## Safe Inventory And Pairing

- Inventory images read-only first. Count JPG/JPEG, RAW/NEF/CR2/ARW/etc., total size, dates, and folder layout.
- Pair JPG and RAW by filename stem. Keep pairs together for every selected image.
- Flag mismatches explicitly, such as JPG-only or RAW-only files. Never silently drop them.
- Treat originals as protected. Write generated artifacts under a clearly named workspace like `_photo_sort/`.
- Do not delete, overwrite, or move non-selected files without explicit confirmation. Moving extras to a review folder is safer than deletion.

Recommended workspace:

- `_photo_sort/contact_sheets/`
- `_photo_sort/manifests/`
- `_photo_sort/post_ready_<N>/source_pairs/`
- `_photo_sort/post_ready_<N>/edited/`
- `_photo_sort/core_memory_<N>/source_pairs/`
- `_photo_sort/review_extras/`

## Curation Workflow

Create reviewable artifacts before final selection:

- contact sheets grouped by day/time and a top-candidates sheet;
- a review gallery if useful;
- CSV/Markdown manifests for all files, selected post-ready, selected core-memory, extras, and mismatches.

Cull for both quality and story:

- technical quality: focus, blur, exposure, highlights, composition;
- emotional value: portraits, interactions, distinctive memories, place/story context;
- variety: portraits/person-in-place, landscapes, architecture, details, food/objects, transitions;
- duplicates: keep the best from repeated bursts instead of letting one scene dominate;
- sequence: make the final set feel like a coherent trip, not just individual high-scoring frames.

Post-ready picks should be stricter and visually cohesive. Core-memory picks may include softer but meaningful story images.

## Editing Workflow

Edit copies only. Start from the selected JPG unless the user asks for RAW development and the toolchain supports it.

For every post-ready image:

1. Define purpose and focal point: identify the subject or story the viewer should connect with.
2. Crop with intent: remove distracting edge elements and strengthen the emotional frame.
3. Correct lens/perspective where needed: straighten architecture and reduce obvious wide-angle distortion.
4. Balance exposure with tone curves: recover highlights, lift shadows, set whites/blacks gently, and avoid flat global exposure boosts.
5. Set white balance before stylizing: keep skin tones natural.
6. Apply local masks/layers: brighten faces or focal areas with masks, not the whole image.
7. Protect skin: use luminance-based lifts and skin-tone masks that preserve warmth and saturation; avoid chalky/white face casts.
8. Fine-tune HSL/color: create a shared palette across the set while keeping skin and key memory colors believable.
9. Use spot healing/cloning only for clear distractions, dust, or blemishes. Ask first if removing a person/object could change the memory or meaning.
10. Add subtle vignette or local contrast only when it guides the eye.

When coding edits, simulate non-destructive layers by keeping intermediate masks separate in logic and writing only new output files. Preserve previous edit versions if doing major revisions.

## Validation

Before reporting completion:

- confirm selected counts match the requested post-ready and core-memory numbers;
- confirm no post-ready/core-memory overlap unless the user explicitly wants overlap;
- confirm each selected JPG has its RAW pair or is marked as an exception;
- verify edited outputs open, have expected dimensions, and are new files;
- visually inspect contact sheets for orientation, color casts, blown faces, repeated scenes, and inconsistent palette;
- report exact output folders, key manifests, mismatches, and what was not done.

If cleanup is requested later, show the exact extras list and estimated disk savings before moving or deleting anything.
