# Masks & Helmets

Masks and helmets are also **props**, but have stricter rules due to head deformation.

They must:
- Align perfectly with the head
- Respect facial animations
- Avoid covering unintended areas

---

## Mask vs Helmet Differences

| Type | Notes |
|----|----|
| Masks | Follow facial structure |
| Helmets | More rigid, bulkier |
| Full-face | High clipping risk |

---

## Prop Slot

| Slot | Item |
|----|----|
| p0 | Hats / Helmets |
| p1 | Glasses |
| p2 | Masks (varies by asset) |

Always confirm slot usage via OpenIV reference.

---

## Bone Attachment

- `SKEL_Head`

Masks should **never** be weighted to facial bones.

---

## Creating Masks From Scratch

### Recommended Workflow
1. Import freemode head
2. Model mask over head mesh
3. Maintain head silhouette
4. Leave breathing room around jaw & eyes

---

## Facial Animation Safety

Avoid geometry that:
- Enters the mouth
- Covers eyelids
- Clips through cheeks

Test with:
- Talking animations
- Yawning
- Combat expressions

---

## Helmets (Hard Surface Rules)

Helmets should:
- Be rigid
- Not deform
- Have clean interior faces removed

Interior geometry that cannot be seen should be deleted.

---

## UV & Texture Notes

- Single texture set preferred
- Alpha masking for visors
- Avoid transparency stacking

---

## Common Issues

| Issue | Cause |
|----|----|
| Helmet floats | Incorrect bone |
| Mask clips | Too tight fit |
| Face pokes through | Missing depth |
| Invisible prop | Wrong slot |

---

## Performance Targets

- Masks: ≤5k polys
- Helmets: ≤8k polys
- Textures: 1024–2048 max

---

## Final Checklist

- Bone: `SKEL_Head`
- Correct prop slot
- No facial bone weighting
- Tested expressions
- Male & female validated
