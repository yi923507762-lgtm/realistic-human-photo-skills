# Region Prompt Guide

Use the shared lock for every image, then append only the target region guidance. Describe the result as a close crop of the intact person, never as a standalone body part.

## Shared reference lock

Treat the supplied master image as the authoritative source for the same person. Preserve identity, facial structure, age, body proportions, skin tone and texture, hair, visible moles or tattoos, clothing, accessories, anatomical left-right orientation, pose logic, lighting direction, white balance, camera character, and setting. Repeat the region-relevant identity anchors from the master in this prompt. Do not horizontally flip or mirror the subject. Create one photorealistic contextual close-up centered on the requested region. The person remains intact and naturally connected outside the crop. Use ordinary camera realism: natural asymmetry, subtle pores and fine hair where visible, mild tonal variation, plausible joints and weight, coherent shadows, real fabric weave and folds, and slight optical softness. No beauty filter, airbrushing, plastic skin, studio glamour, redesign, cloned features, extra parts, missing parts, fused anatomy, floating anatomy, or text.

If the reference does not visibly establish a requested feature, do not invent it. If an object or another person hides part of a region, preserve that occlusion and generate only the visible portion. Keep covered areas covered and preserve the exact garment or footwear.

## Target guidance

- **Head and face:** Preserve exact face shape, eye spacing, nose, mouth, ears, hairline, hairstyle, and expression. Retain natural pores, under-eye texture, small asymmetries, and flyaway hair without exaggerating blemishes.
- **Neck, shoulders, upper torso:** Preserve head-to-neck and shoulder proportions, collar shape, garment seams, fabric tension, and natural clavicle or neck definition only where already visible.
- **Torso, waist, clothed hips:** Preserve body volume and posture beneath the same clothing. Keep garment length, waistband, buttons, seams, folds, and compression coherent; do not reveal covered anatomy.
- **Arm:** Preserve the correct left or right side, garment sleeve, elbow structure, wrist alignment, skin texture, and natural bend. Include a small amount of shoulder and hand context when helpful.
- **Hand:** Preserve the anatomical left or right hand, original gesture, jewelry, visible finger count, and every overlap or occlusion. Keep visible knuckles, nails, creases, finger lengths, and wrist attachment coherent. Never expose or invent fingers hidden in the master merely to display all five.
- **Leg:** Preserve the correct left or right leg, clothing, hip-to-knee-to-ankle alignment, fabric tension at joints, stance, and weight distribution. Include adjacent torso or foot context when helpful.
- **Foot:** Preserve the correct left or right foot, footwear, socks, straps, laces, wear, and floor contact. If the reference shows a bare foot, keep five plausible toes and natural ankle attachment; otherwise do not remove footwear.

## Group handling

Use the original group image as the master, but name the target subject by position plus clothing in every prompt. Crop tightly enough to emphasize only that subject's requested region while retaining enough context to distinguish them. Do not borrow face, clothing, skin, or body traits from another person in the group.

## Negative prompt

AI-generated look, beauty filter, airbrushed skin, plastic skin, wax skin, cloned face, changed identity, changed age, changed body type, changed clothing, different accessories, horizontal flip, mirrored subject, swapped left and right, moved identity marks, removed occluder, invented hidden detail, duplicated people, duplicate limbs, extra arms, missing arms, extra hands, missing hands, extra fingers, missing fingers, fused fingers, warped wrists, broken elbows, distorted joints, disconnected limbs, malformed knees, malformed feet, extra toes, missing toes, impossible posture, inconsistent lighting, isolated body part, severed limb, floating anatomy, anatomical diagram, text, watermark
