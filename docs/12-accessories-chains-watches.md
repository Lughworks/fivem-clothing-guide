# Accessories: Chains, Watches & Wearables

Accessories in FiveM are **props**, not standard clothing components.
They attach to bones and use prop slots instead of drawable components.

This includes:
- Chains
- Watches
- Bracelets
- Glasses
- Hats (covered separately in masks & helmets)

---

## How Accessories Work

Accessories use:
- `.ydd` → prop model
- `.ytd` → textures
- Prop slot index

They are attached to bones such as:
- `SKEL_Neck_1`
- `SKEL_L_Hand`
- `SKEL_R_Hand`
- `SKEL_Head`

---

## Common Prop Slots

| Slot | Item |
|----|----|
| p0 | Hats |
| p1 | Glasses |
| p2 | Ears |
| p7 | Watches |
| p8 | Bracelets |
| p9 | Chains |

> Slot numbers are critical.  
> Wrong slot = invisible or misplaced prop.

---

## Editing Existing Accessories (Recommended)

### Workflow
1. Export prop `.ydd` + `.ytd` from OpenIV
2. Import into Blender via Sollumz
3. Edit mesh or texture
4. Preserve bone attachment
5. Re-export

---

## Chains (Neck Accessories)

### Bone
- `SKEL_Neck_1`

### Rules
- Keep geometry lightweight
- Avoid excessive physics expectation
- Slight clipping is unavoidable in extreme animations

### Pro Tip
Chains should sit **slightly above** the chest to avoid deep torso clipping.

---

## Watches & Bracelets

### Bones
- `SKEL_L_Hand`
- `SKEL_R_Hand`

### Best Practices
- Align with neutral T-pose hand
- Avoid oversized geometry
- Test steering wheel & weapon animations

---

## Weighting Rules (Very Important)

Accessories must:
- Be fully weighted
- Use **single-bone weighting** in most cases
- Avoid blended weights unless absolutely required

Unweighted props will float or detach.

---

## Optimization Guidelines

- Target under 3k polys
- One material per prop
- 1024px textures max
- No unnecessary normal maps

---

## Testing Checklist

- Male & female alignment
- No wrist rotation clipping
- No neck distortion
- Correct prop slot assignment
