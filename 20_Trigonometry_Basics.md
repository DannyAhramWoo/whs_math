# 20. Trigonometry Basics

> **Unit:** Trigonometry (Unit 20 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 3, advanced**
> **Why it matters:** Most primary problems avoid full trigonometry, but the Law of Sines/Cosines occasionally solve "awkward angle" triangle problems faster than angle-chasing. Treat this unit as *optional/advanced* — read [[02_Angles_Similarity_Circles]] first.

---

## Lesson Overview
What this note covers:

1. sin, cos, tan Basics — *Sec 3, advanced*
2. Special Angle Values
3. Area, Law of Sines & Law of Cosines — *Sec 3, advanced*

---

## 1. sin, cos, tan Basics — *Sec 3, advanced*

> 📖 *Source: AOPS Introduction to Geometry Ch.18 "Introduction to Trigonometry" — §18.1 (right-triangle ratios), §18.2 (beyond right triangles).*

For a right triangle with a chosen acute angle A:

- **sin A** = opposite side / hypotenuse
- **cos A** = adjacent side / hypotenuse
- **tan A** = opposite / adjacent = sin A / cos A
- **Remember it as SOH-CAH-TOA:** **S**in = **O**pp/**H**yp, **C**os = **A**dj/**H**yp, **T**an = **O**pp/**A**dj.
- **Reciprocals** (less common): cosec A = 1/sin A, sec A = 1/cos A, cot A = 1/tan A.

- **Core identity: sin²A + cos²A = 1.** *Why:* opp² + adj² = hyp² (Pythagoras); divide both sides by hyp² and each term becomes sin²A + cos²A = 1.
- **Cofunction identity:** sin A = cos(90° − A). The sine of an angle equals the cosine of its complement (opposite and adjacent swap when you look from the other acute angle).
- **Bounds (for an acute angle):** 0 < sin A < 1 and 0 < cos A < 1, while tan A > 0 with **no upper limit** (it shoots to infinity as A → 90°).

---

## 2. Special Angle Values

> 📖 *Source: AOPS Introduction to Geometry §18.1 & §18.4; the 30/45/60 values come from the special right triangles in Ch.6 §6.2 (also [[02_Angles_Similarity_Circles]]).*

These come straight from the 45-45-90 and 30-60-90 triangles:

| Angle | sin | cos | tan |
|-------|-----|-----|-----|
| 0° | 0 | 1 | 0 |
| 30° | 1/2 | √3/2 | 1/√3 |
| 45° | √2/2 | √2/2 | 1 |
| 60° | √3/2 | 1/2 | √3 |
| 90° | 1 | 0 | undefined |

- **Memory pattern for sine:** 0°, 30°, 45°, 60°, 90° give sin = √0/2, √1/2, √2/2, √3/2, √4/2 — i.e. **√0, √1, √2, √3, √4 all over 2**. Cosine is the same list **reversed**.
- Example: a right triangle with a 30° angle and short leg 5 → other leg = 5√3, hypotenuse = 10 (matches the 1:√3:2 ratio).

---

## 3. Area, Law of Sines & Law of Cosines — *Sec 3, advanced*

> 📖 *Source: AOPS Introduction to Geometry §18.2 (area formula) & §18.3 (Law of Sines, Law of Cosines).*

- **Area of any triangle: [ABC] = ½·ab·sin C** — half the product of two sides times the sine of the angle **between** them. (No height needed — great for "ugly angle" area problems.)
  - Example: sides 6 and 8 with a 30° angle between → area = ½·6·8·sin30° = 24·½ = **12**.
- **Law of Sines:** a/sin A = b/sin B = c/sin C. Use this when you know two angles and one side (or two sides and a non-included angle). *(The extended form a/sin A = 2R, R = circumradius, is a harder challenge-level result, not the basic law.)*
- **Law of Cosines:** c² = a² + b² − 2ab·cos(C). Use this when you know two sides and the INCLUDED angle, or all three sides (to find an angle). It's a generalization of Pythagoras — when C=90°, cos(90°)=0 and it collapses to the normal c²=a²+b².
  - Example: sides a=3, b=4, included angle C=30° → c² = 9+16−2(3)(4)cos30° = 25−12√3.

> ⚠️ **Warning (the ambiguous SSA case):** with two sides and a **non-included** angle, the Law of Sines can give **two** possible triangles (an angle and its supplement both have the same sine). Always check whether both fit — this is exactly why "SSA" is not a valid congruence rule.

> 💡 **Competition point:** If a triangle problem gives you an "ugly" non-90° angle and asks for a side or area, the Law of Cosines (for a side) or ½ab·sin C (for the area) usually solves it in one line — faster than angle-chasing.

---

## Cheat Sheet

| Idea | Formula |
|------|---------|
| sin A | opposite / hypotenuse (SOH) |
| cos A | adjacent / hypotenuse (CAH) |
| tan A | opposite / adjacent (TOA) |
| sin²+cos² | = 1 always |
| Cofunction | sin A = cos(90°−A) |
| sin pattern (0/30/45/60/90) | √0/2, √1/2, √2/2, √3/2, √4/2 |
| Triangle area | ½·ab·sin C |
| Law of Sines | a/sinA = b/sinB = c/sinC |
| Law of Cosines | c² = a²+b²−2ab·cosC |
| SSA | ambiguous — may give two triangles |

---

## Quick Check

1. In a right triangle, one leg is 5 and the angle opposite it is 30°. Find the hypotenuse.
2. What is sin 60°?
3. A triangle has sides 5, 7, and an included angle of 60°. Use the Law of Cosines to find the third side squared.
4. Find the area of a triangle with sides 10 and 6 and a 30° angle between them.
5. Using the cofunction identity, what is sin 70° equal to in terms of cosine?

<details>
<summary>Answers</summary>

1. sin30° = 5/hyp = 1/2 → hyp = **10**.
2. sin60° = **√3/2**.
3. c² = 25+49−2(5)(7)cos60° = 74−70(1/2) = 74−35 = **39**.
4. ½·10·6·sin30° = 30·½ = **15**.
5. sin 70° = cos(90° − 70°) = **cos 20°**.

</details>

---
*This is a new, optional/advanced unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds on the special right triangles in [[02_Angles_Similarity_Circles]]. Most primary problems don't need this — only use it if a problem gives an "ugly" angle that resists angle-chasing.*
