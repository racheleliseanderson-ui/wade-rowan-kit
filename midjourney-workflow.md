# Midjourney Workflow for Wade Rowan v1.0

Status: Parallel to Kling Element binding. Identity authority remains WADE-A01-MASTER-v2.jpg + Realism Guardrail.

## Live Public References (Phase 0.1 complete)

- **Master face**: https://drive.google.com/uc?export=view&id=16nqM_wOVM6dRI302GCj39pYpI19_W951
- **Expression sheet**: https://drive.google.com/uc?export=view&id=1BnEYjlUx6yVIIEl-BuzF-VPD2gVDI50q

## 1. Required Prompt Structure (every generation)

**POSITIVE ANCHOR** (copy exactly):
Wade Rowan, disclosed fictional Hook the Horizon host. Photorealistic documentary portrait of a 19-year-old American man (reads 18-22), original non-celebrity face: broad rounded-square face with youthful fullness, friendly steady dark hazel-brown eyes, warm-neutral light-to-medium complexion with faint sun exposure, straight slightly rounded nose, easy natural smile or neutral listening expression, natural asymmetry and visible skin texture. Clean-shaven. Medium-brown short-to-medium slightly wavy textured hair with a clean taper and natural movement. 5 ft 11 in, about 200 lb: broad thick neck, wide solid shoulders, substantial torso, sturdy hips and legs, naturally athletic football build with believable softness, not cut, not slim.

**Realism Guardrail block**:
Preserve the master's broad rounded-square youthful face, dark hazel-brown eyes, slightly uneven brows, straight softly rounded nose, natural asymmetry, and broad approximately 200-pound build. Preserve real human micro-detail: visible pores, mild uneven cheek and nose redness, subtle under-eye variation, faint beard shadow and micro-stubble when present on master or request clean-shaven, fine facial hairs, natural lip texture, a small chin blemish, non-identical eye catchlights, and irregular hair flyaways. Use an unforced neutral listening expression or a moment-specific expression, never a default catalog half-smile. Documentary realism, plausible environmental light, restrained contrast, no beauty retouching.

**STYLE TAIL**:
Documentary outdoor realism, natural color, slight film grain, real skin texture with pores, no retouching, coherent weather, clothing, habitat and gear, environmental portrait, room above the head for headline crop.

## 2. Parameters (V7 preferred)

`--oref https://drive.google.com/uc?export=view&id=16nqM_wOVM6dRI302GCj39pYpI19_W951 --ow 150-300` (start at 200; raise for tighter face lock, lower for freer wardrobe/pose) `--v 7 --stylize 50-100 --style raw`

V6 fallback: `--cref [same URL] --cw 80-100`

## 3. Negative / --no

celebrity likeness, Luke Combs, Garth Brooks, Morgan Wallen, beard, full beard, mustache, goatee, middle-aged, wrinkles, grey hair, child, teenager under 17, slim waist, skinny, fashion model, bodybuilder, six-pack, muscle definition, tactical gear, rifle in hand, gun, cowboy hat, camouflage, trophy fish held to camera, waxy skin, airbrushed, beauty filter, plastic teeth, perfect symmetry, oversharpened, editorial fashion pose, pointing at camera, extra fingers, malformed hands, broken rod mechanics, logos, brand names, text, watermark, cartoon, illustration, 3D render, flawless skin, porcelain, glowing skin, hyperreal, razor-sharp jaw, chiseled, symmetrical face, perfect smile, sparkling eyes

## 4. Workflow Rules

1. Always start with identity block + realism block + scene + Style Tail.
2. Never generate face from text alone. Always include --oref on the locked master.
3. One Look / wardrobe description only (match Kling Lxx routing).
4. Audit every output against Realism Guardrail stop conditions. Reject on two or more.
5. Approved stills can become first frames for Kling I2V; do not promote into new Core/Master.
6. Prefer 3:4 or 4:5 for social talking-head / portrait; 16:9 for landscape B-roll.

## 5. Example

[POSITIVE ANCHOR] [REALISM] Head-and-shoulders, square to camera, eye level, attentive neutral expression with warmth, plain deep-water teal short-sleeve button-down, soft overcast daylight, blurred lakeshore background, 85mm, 3:4 [STYLE TAIL] --oref https://drive.google.com/uc?export=view&id=16nqM_wOVM6dRI302GCj39pYpI19_W951 --ow 220 --v 7 --style raw --no [NEGATIVES]

## Integration
After CONTENT-BRIEF + 8-gate, agent outputs the exact Midjourney prompt string. Prefer for high-quality stills / first frames; Kling Core + Look for motion.
