---
name: realistic-human-detail-views
description: Generate a coordinated set of separate photorealistic close-up images for visible human regions from one master reference image. Use when the user wants consistent face, hands, arms, torso, legs, or feet detail views; do not use for a single complete portrait or medical anatomy.
---

# Realistic Human Detail Views

Create separate contextual close-up images of one person's visible external body regions while keeping the master image authoritative for identity and appearance. Each requested region is one image, not a collage or a detached anatomical cutout.

## Required source

- Prefer one approved full-body or sufficiently complete master reference image.
- If the user has no reference and requests a fictional person, first generate one master full-person image, then use that exact image for every detail view.
- If a requested region is hidden, cropped out, or too unclear in the master, ask for a suitable reference or omit that region. Do not reconstruct identity-specific details that are not visible.
- If only part of a combined view is hidden, generate the visible subregion and omit only the unavailable part. Preserve the occluding person or object; do not reveal what is behind it.
- For groups, label subjects by stable visible traits such as position and clothing, then process one subject at a time. Never infer identity from the face alone. Unless the user explicitly requests the full set for everyone, default to each subject's face, upper body, and visible hands so the run does not silently multiply into a large batch.

## View sets

Use only the regions needed by the user. If they request a standard set, generate:

1. Head and face
2. Neck, shoulders, and upper torso
3. Left arm and hand
4. Right arm and hand
5. Waist, hips, and lower torso as clothed in the reference
6. Left leg and foot
7. Right leg and foot

If the user explicitly requests every region separately, split arms from hands and legs from feet, producing: head/face, neck/shoulders, torso/waist, left arm, right arm, left hand, right hand, clothed hips, left leg, right leg, left foot, and right foot.

## Workflow

1. Identify the master reference, target subject, requested set, output destination, and any framing constraints. Build a short identity-anchor list from visible evidence, such as an anatomical-right facial mark, anatomical-left wristwatch, hairstyle, garment wear, or tattoo placement; do not infer missing anchors.
2. Read [references/region-prompts.md](references/region-prompts.md) before generating images.
3. State the planned image list. When the user has already asked for every region, proceed without asking them to confirm the list.
4. Generate or edit one image per region. Supply the original master reference and repeat every relevant identity anchor in every call; do not use a generated detail view as the next reference because identity and proportions will drift.
5. Keep identity, age, body type, skin tone, hair, visible moles or tattoos, clothing, accessories, anatomical left-right orientation, lighting direction, camera color, and environmental context unchanged unless the user requests a change. Do not horizontally flip or mirror the subject.
6. Inspect every output for subject consistency, correct target region, natural anatomy, intact clothing, and absence of duplicated or fused parts. Retry a failed region once with a targeted correction; if it still fails, report that region instead of looping.
7. Return the images in the planned order with clear region labels. Save and report paths when the images are intended as reusable files.

## Boundaries

- This skill covers ordinary clothed people photography and visible external features, not medical, diagnostic, internal-anatomy, or forensic reconstruction.
- A crop may show nearby body context so the target looks naturally attached. Never depict an isolated, severed, floating, or diagram-like body part unless the user explicitly requests an anatomical illustration, which belongs to another workflow.
- Clothing must remain on covered regions; never invent what is underneath it.
- Prompting improves the odds of anatomical realism but cannot guarantee perfect hands, feet, or identity consistency. Treat the master reference and visual inspection as the controls.
