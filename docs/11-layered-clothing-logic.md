Absolutely — this is a **core FiveM pain point**, so let’s document it properly and save people *hours* of trial-and-error.

Below is a **drop-in chapter** for your repo that explains **how GTA/FiveM layering actually works**, how to build compatible items, and how to avoid the classic “why are my arms broken?” moments.

---

# 🧥 docs/14-layered-clothing-logic.md

![Image](https://img.gta5-mods.com/q75/images/mp-character-texture-edits/53d690-20201104222354_1.jpg)

![Image](https://img.gta5-mods.com/q75-w500-h333-cfill/images/denim-jacket-and-inside-hoodie/b3dac7-Grand%20Theft%20Auto%20V%2011_09_2018%2018_05_40.png)

![Image](https://forum-cfx-re.akamaized.net/original/4X/5/5/2/55256839b8e19fc04db93ae0564dd3d5bdcfcba2.jpeg)

````md
# Layered Clothing Logic (Jackets, Hoodies & Torsos)

Layered clothing in FiveM is not automatic.
It relies on **component pairing rules** that GTA V expects.

If these rules are broken, you’ll see:
- Invisible arms
- Floating hands
- Severe clipping
- Forced torso overrides

This chapter explains how to build clothing that layers correctly.

---

## The Core Rule (Read This Twice)

**Jackets do NOT contain arms.**  
**Torsos DO contain arms.**

Every upper-body outfit is a combination of:
- `jbib` → jacket / hoodie / coat
- `torsos` → arms + undershirt
- `undershirt` → chest layer (optional)

You must design these together.

---

## Upper Body Component Roles

| Component | Purpose |
|--------|--------|
| jbib | Jackets, hoodies, coats |
| torsos | Arms + skin / sleeves |
| undershirt | T-shirts, inner layers |

> A jacket without a matching torso WILL break animations.

---

## How GTA Expects Layering to Work

Example outfit:
- Hoodie (jbib)
- Long sleeve arms (torso)
- T-shirt (undershirt)

Each item is separate but **visually designed to fit together**.

---

## Creating a Jacket or Hoodie (Correct Method)

### DO:
- Remove arms from the jacket mesh
- Cut sleeves at shoulder seam
- Leave empty space where arms would be

### DO NOT:
- Model arms into jackets
- Weight jackets to arm bones
- Assume the game will “hide arms for you”

---

## Creating Matching Torsos (Mandatory)

For every jacket/hoodie you should create:
- A **matching torso**
- With correct sleeve length
- With correct skin coverage

### Torso Types
- Short sleeve
- Long sleeve
- Rolled sleeve
- Gloved variants

These are separate `.ydd` files.

---

## Naming & Pairing Strategy

Recommended naming pattern:
```text
hoodie_black_jbib.ydd
hoodie_black_torso.ydd
```

This makes:

* Pack maintenance easier
* Shop logic cleaner
* Player choice clearer

---

## Weight Painting Rules (Layered Clothing)

### Jackets / Hoodies

* Weighted to spine & clavicles
* Minimal arm weighting (if any)
* No elbow or wrist weights

### Torsos

* Fully weighted arms
* Match vanilla deformation closely
* Copy weights from GTA base torsos when possible

---

## Undershirts (When & Why)

Undershirts:

* Sit beneath jackets
* Are visible at collar, waist, sleeves
* Prevent skin clipping

### Best Practice

* Design undershirts with jackets in mind
* Avoid oversized collars
* Keep geometry simple

---

## Common Layering Failures

| Issue            | Cause                |
| ---------------- | -------------------- |
| Missing arms     | No torso equipped    |
| Arms clip jacket | Sleeve mismatch      |
| Jacket stretches | Weighted to arms     |
| Hands float      | Broken torso weights |
| Skin showing     | Missing undershirt   |

---

## Testing Layered Clothing

Always test:

* Standing idle
* Walking & running
* Entering vehicles
* Weapon holding
* Steering wheel animations

Test **male and female freemode** separately.

---

## Performance & Optimization

* Remove hidden interior faces
* Avoid duplicate geometry
* Share textures where possible
* Keep each layer efficient

Layered clothing multiplies draw calls — optimize aggressively.

---

## Advanced Tip: Modular Layer Sets

Professional packs often ship:

* Jacket + 3 torsos
* One undershirt
* Multiple colour variants

This gives players freedom without breaking visuals.

---

## Release Checklist (Layered Clothing)

* Jacket has no arms
* Matching torso exists
* Undershirt optional but tested
* Weights validated
* No clipping in motion
* Correct slot assignments