# Body Size & Shape Compatibility

FiveM freemode peds support multiple body shapes and weight variations.
Clothing must accommodate these differences or it will clip, stretch, or break immersion.

This chapter explains how to build clothing that works across body types.

---

## Freemode Body Variations

Freemode peds change shape based on:
- Weight sliders
- Fitness sliders
- Face blend values
- Gender differences

These changes affect:
- Chest depth
- Arm thickness
- Waist width
- Shoulder breadth

Clothing does NOT auto-adjust safely.

---

## The Reality (Important)

There is no way to make clothing fit *every* extreme body type perfectly.

Your goal is:
> **Acceptable behavior across 80–90% of player builds**

---

## Design for the Median Body

### Best Practice
- Design clothing around **default freemode body**
- Slightly bias toward average-to-heavy
- Avoid skin-tight geometry unless intentional

Extreme skinny bodies are less forgiving than heavier ones.

---

## Thickness Buffer Rule

Always leave:
- 1–2cm clearance around chest
- Extra space at armpits
- Slight looseness at waist

This buffer absorbs body morphing.

---

## Gender-Specific Differences

Male and female freemode peds:
- Have different shoulder widths
- Different chest curvature
- Different hip placement

### Rule
**Never reuse the same mesh for both genders.**

Always:
- Model separately
- Weight separately
- Test separately

---

## Sleeves & Arm Tolerance

Arms are the #1 clipping source.

### Safer Sleeve Designs
- Straight-cut sleeves
- Slight taper toward wrist
- Avoid tight bicep fits

### High-Risk Designs
- Skin-tight sleeves
- Short sleeves near deltoid
- Heavy folds near elbows

---

## Torso Compatibility Strategy

For layered clothing:
- Provide multiple torsos if needed
- Use slightly thicker sleeves
- Avoid aggressive muscle definition

Neutral anatomy performs best.

---

## Testing Body Shape Coverage

Test with:
- Minimum weight
- Maximum weight
- Average build
- Male & female

If it survives these, it’s safe for release.

---

## Known Limitations (Accept Them)

- Extreme sliders WILL clip
- Sitting poses exaggerate issues
- Some animations break realism

Document this in your pack if selling.

---

## Release Checklist (Body Compatibility)

- Tested min / max weight
- Sleeves survive arm bend
- Chest doesn’t collapse
- Waist doesn’t tear open
- Male & female verified
