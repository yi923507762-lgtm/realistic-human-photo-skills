---
name: realistic-id-photo
description: Create photorealistic, unretouched prompts for one or more people, from ID-style headshots to half-body, full-body, and group photos. Use when the user wants natural-looking people with believable facial, body, hand, pose, and clothing details rather than an airbrushed AI look.
compatibility: Portable to any agent that can read local files — no external API calls, proprietary runtime, or required tools.
---

# Realistic People Photo Prompt

## Usage

The template has one free-form slot, { }. Put the user's description of the person or people in the slot. It may include the number of people, each person's distinguishing features, clothing, action, setting, and framing.

1. Preserve the stated number of people and each person's distinguishing details. Do not invent, merge, duplicate, or omit subjects.
2. Follow a requested composition or backdrop. If neither is specified, use a plain white background; default to a single head-and-shoulders frame for one person, or a frame that keeps every person visible for a group.
3. Output the complete English prompt below, then the separate negative prompt. Keep the fixed wording unchanged; translate only the user's supplied description when necessary.
4. Detail only body parts that are visible in the requested framing. Do not claim to reveal, reconstruct, or alter unseen anatomy.

## Prompt Template

{ }, photorealistic unretouched people photo. Preserve the requested number of people, their distinct appearance, clothing, relative positions, and interactions. For two or more people, make every subject visually distinct and fully separate, with natural spacing, believable eye lines, and no duplicated faces or bodies.

Follow the requested backdrop and framing. If neither is specified, use a plain white background: a single person is framed head and shoulders, while a group is framed wide enough to include every person naturally. Natural and relaxed expressions, not a posed glamour shot, influencer selfie, portrait/fine-art session, commercial fashion photo, or high-end studio shoot.

Faces are human and individually varied, not completely symmetrical or standardized. Real skin, not airbrushed: fine visible pores, naturally uneven skin tone, mild redness around the nostrils, faint fine lines, subtle under-eye texture, occasional small blemishes, fine facial hair, and realistic highlights on the T-zone. Keep each subject's face proportionate to their own body and lighting.

When the framing shows the body, use believable anatomy and everyday posture: natural head-to-neck connection, shoulders, torso, hips, elbows, knees, and feet with realistic proportions; plausible weight distribution and clothing drape; coherent contact with nearby people or objects. When hands are visible, show two distinct hands with five anatomically plausible fingers each unless naturally hidden by the pose or crop. Keep limbs separate and joints, wrists, fingers, and feet undistorted.

Ordinary, unsophisticated lighting with no beauty lighting or soft focus. Phone-photo quality: slight compression artifacts, slight noise, very subtle blur, colors not very saturated, slightly warm white balance, low-to-moderate contrast, ordinary everyday camera photo, not retouched, no beauty filter.

Negative prompt: AI face, AI-generated look, cartoon, anime, illustration, painting, 3D render, CG, plastic skin, rubber face, ceramic skin, glass eyes, vacant gaze, over-airbrushed, flawless skin, smooth skin, perfect facial features, uniform features, influencer face, beauty filter, liquify/retouch traces, over-sharpened, ultra-sharp eyes, fake pores, fake texture, retouched portrait photos, magazine cover, perfect symmetry, artistic beautification, commercial lighting, high-end studio lighting, soft focus, creamy skin, cold pale skin, duplicate people, cloned faces, merged bodies, fused limbs, disconnected limbs, extra arms, missing arms, extra hands, missing hands, extra fingers, missing fingers, fused fingers, warped wrists, distorted joints, malformed feet, impossible posture, incorrect body proportions, floating body parts, tangled people
