# 20. Trigonometry Basics

> **Unit:** Trigonometry (Unit 20 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary competition students (SMO · NMOS · IMSO) — concepts go up to **Secondary 3, advanced**
> **Why it matters:** Most SMO/NMOS/IMSO problems avoid full trigonometry, but the Law of Sines/Cosines occasionally solve "awkward angle" triangle problems faster than angle-chasing. Treat this unit as *optional/advanced* — read [[02_Angles_Similarity_Circles]] first.

---

## Lesson Overview
What this note covers:

1. sin, cos, tan Basics — *Sec 3, advanced*
2. Special Angle Values
3. Law of Sines and Law of Cosines — *Sec 3, advanced*

---

## 1. sin, cos, tan Basics — *Sec 3, advanced*

For a right triangle with a chosen acute angle A:

- **sin A** = opposite side / hypotenuse
- **cos A** = adjacent side / hypotenuse
- **tan A** = opposite / adjacent = sin A / cos A

- Core identity: sin²A + cos²A = 1 (this is really just Pythagoras in disguise).

---

## 2. Special Angle Values

These come straight from the 45-45-90 and 30-60-90 triangles already in [[02_Angles_Similarity_Circles]]:

| Angle | sin | cos | tan |
|-------|-----|-----|-----|
| 30° | 1/2 | √3/2 | 1/√3 |
| 45° | √2/2 | √2/2 | 1 |
| 60° | √3/2 | 1/2 | √3 |

- Example: a right triangle with a 30° angle and short leg 5 → other leg = 5√3, hypotenuse = 10 (matches the 1:√3:2 ratio).

---

## 3. Law of Sines and Law of Cosines — *Sec 3, advanced*

- **Law of Sines:** a/sin A = b/sin B = c/sin C = 2R (R = circumradius). Use this when you know two angles and one side (or two sides and a non-included angle).
- **Law of Cosines:** c² = a² + b² − 2ab·cos(C). Use this when you know two sides and the INCLUDED angle, or all three sides (to find an angle). It's a generalization of Pythagoras — when C=90°, cos(90°)=0 and it collapses to the normal c²=a²+b².
  - Example: sides a=3, b=4, included angle C=30° → c² = 9+16−2(3)(4)cos30° = 25−12√3.

> 💡 **Competition point:** If a triangle problem gives you an "ugly" non-90° angle and asks for a side or area, the Law of Cosines usually solves it in one line — faster than trying to angle-chase a solution.

---

## Cheat Sheet

| Idea | Formula |
|------|---------|
| sin A | opposite / hypotenuse |
| cos A | adjacent / hypotenuse |
| tan A | opposite / adjacent |
| sin²+cos² | = 1 always |
| Law of Sines | a/sinA = b/sinB = c/sinC = 2R |
| Law of Cosines | c² = a²+b²−2ab·cosC |

---

## Quick Check

1. In a right triangle, one leg is 5 and the angle opposite it is 30°. Find the hypotenuse.
2. What is sin 60°?
3. A triangle has sides 5, 7, and an included angle of 60°. Use the Law of Cosines to find the third side squared.

<details>
<summary>Answers</summary>

1. sin30° = 5/hyp = 1/2 → hyp = **10**.
2. sin60° = **√3/2**.
3. c² = 25+49−2(5)(7)cos60° = 74−70(1/2) = 74−35 = **39**.

</details>

---
*This is a new, optional/advanced unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds on the special right triangles in [[02_Angles_Similarity_Circles]]. Most SMO/NMOS problems don't need this — only use it if a problem gives an "ugly" angle that resists angle-chasing.*
