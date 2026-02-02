# Advanced Clipping Mitigation Techniques

Clipping is unavoidable in FiveM — but it can be minimized intelligently.

This chapter covers proven techniques used in high-quality packs.

---

## Understand Where Clipping Comes From

Clipping happens due to:
- Body morphing
- Animation extremes
- Layered geometry overlap
- Overly tight meshes

Fixing clipping is about **damage control**, not perfection.

---

## Technique 1: Hidden Geometry Removal

Always delete:
- Torso faces under jackets
- Chest faces under armor
- Waist faces under long tops

This prevents internal clipping explosions.

---

## Technique 2: Strategic Mesh Offsetting

Slightly offset outer layers:
- Jackets: +0.5 to +1cm
- Hoodies: +1cm chest & arms

Do NOT overdo this or the item looks inflated.

---

## Technique 3: Sleeve Termination Zones

End sleeves:
- Before elbow bend
- Or well past it

Never end sleeves directly on a joint.

---

## Technique 4: Weighted Compromise Zones

Blend weights softly around:
- Shoulders
- Upper arms
- Waist

Hard transitions amplify clipping.

---

## Technique 5: Controlled Rigidity

For jackets & armor:
- Reduce arm influence
- Anchor more to spine/clavicle
- Let arms move inside the garment slightly

This mimics real-world clothing stiffness.

---

## Technique 6: Variant-Based Fixing

Professional packs often include:
- Tight variant
- Loose variant
- Heavy-body variant

Same texture, different mesh.

---

## Technique 7: Animation Stress Testing

Test with:
- Running
- Sprinting
- Entering vehicles
- Steering wheel
- Weapon aiming

Animations reveal issues idle stance never will.

---

## Technique 8: Acceptable Clipping Zones

Players tolerate clipping more in:
- Armpits
- Lower back
- Inner thighs

Players notice clipping most at:
- Chest
- Hands
- Face
- Shoulders

Prioritize accordingly.

---

## Transparency Is NOT a Fix

Avoid:
- Alpha masking to hide clipping
- Invisible geometry hacks

These cause:
- Z-fighting
- Sorting issues
- Multiplayer desync artifacts

---

## Performance vs Perfection

Every mitigation technique costs:
- Extra geometry
- Extra variants
- Extra testing

Balance effort vs benefit.

---

## Final Mitigation Checklist

- Hidden faces removed
- Sleeves avoid joints
- Offsets applied subtly
- Tested stress animations
- No alpha hacks
- Variants documented
