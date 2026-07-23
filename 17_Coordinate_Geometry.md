# 17. Coordinate Geometry

> **Unit:** Coordinate Geometry (Unit 17 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** Distance/midpoint/slope formulas let you solve geometry problems with pure algebra instead of drawing — a fast backup method when angle-chasing gets stuck. Builds on the coordinate basics already in [[03_Special_Theorems_Coordinates_Solids]].

---

## Lesson Overview
What this note covers:

1. Distance and Midpoint Formulas
2. Slope
3. Equations of a Line
4. Parallel & Perpendicular Lines
5. Equation of a Circle
6. Power of a Point (algebraic view)

---

## 1. Distance and Midpoint Formulas

- **Distance formula** (from Pythagoras): distance between (x₁,y₁) and (x₂,y₂) = √[(x₂−x₁)² + (y₂−y₁)²].
  - Example: distance from (1,1) to (4,5) = √[3² + 4²] = √25 = 5.
- **Midpoint formula:** midpoint of (x₁,y₁) and (x₂,y₂) = ((x₁+x₂)/2, (y₁+y₂)/2).
  - Example: midpoint of (2,4) and (8,10) = (5,7).

---

## 2. Slope

- **Slope** m = (y₂−y₁)/(x₂−x₁) — measures steepness. Positive slope rises left-to-right, negative falls, zero slope is horizontal (y=k), and a vertical line (x=h) has undefined slope.
  - Example: through (2,3) and (6,11): slope = (11−3)/(6−2) = 8/4 = 2.

> 💡 **Competition point:** Never swap the order of subtraction between numerator and denominator — always use the SAME point order in both.

---

## 3. Equations of a Line

- **Slope-intercept form:** y = mx + b (m = slope, b = y-intercept).
- **Point-slope form:** y − y₁ = m(x − x₁), built directly from the slope formula using one known point.
- **Standard form:** Ax + By = C.
- **x-intercept / y-intercept:** set y=0 to find the x-intercept, set x=0 to find the y-intercept. Quick way to graph a line — just plot both intercepts and connect them.
  - Example: for 2x + 3y = 12, x-intercept = (6,0), y-intercept = (0,4).

---

## 4. Parallel & Perpendicular Lines

- **Parallel lines** have EQUAL slopes.
- **Perpendicular lines** have slopes that are **negative reciprocals** of each other (their product = −1).
  - Example: a line perpendicular to slope 2/3 has slope −3/2.

---

## 5. Equation of a Circle

- A circle with center (h,k) and radius r has equation (x−h)² + (y−k)² = r².
- If given a messy expanded equation, **complete the square** (for x and for y separately) to find the center and radius.
  - Example: x² − 4x + y² + 8y = 2 → (x−2)² + (y+4)² = 22, so center (2,−4), radius √22.

---

## 6. Power of a Point (algebraic view)

This is the same theorem already in [[02_Angles_Similarity_Circles]], but here's how to find where a line crosses a circle using algebra: substitute the line's equation into the circle's equation, giving a quadratic — its two roots are the two crossing points' coordinates.

> 💡 **Competition point:** Combining a line equation and a circle equation always reduces to solving ONE quadratic. If the discriminant (see [[12_Equations_Algebra_Factoring]]) is zero, the line is tangent to the circle (touches at exactly one point).

---

## Cheat Sheet

| Idea | Formula |
|------|---------|
| Distance | √[(x₂−x₁)² + (y₂−y₁)²] |
| Midpoint | ((x₁+x₂)/2, (y₁+y₂)/2) |
| Slope | (y₂−y₁)/(x₂−x₁) |
| Point-slope form | y−y₁ = m(x−x₁) |
| Parallel lines | same slope |
| Perpendicular lines | slopes multiply to −1 |
| Circle equation | (x−h)²+(y−k)² = r² |
| Line meets circle | substitute → quadratic; discriminant=0 means tangent |

---

## Quick Check

1. Find the distance between (0,0) and (3,4).
2. Find the midpoint of (−2,6) and (4,−2).
3. Find the slope of the line through (1,2) and (5,10).
4. Find the equation of a circle with center (3,−1) and radius 5.

<details>
<summary>Answers</summary>

1. √(9+16) = √25 = **5**.
2. ((−2+4)/2, (6−2)/2) = **(1, 2)**.
3. (10−2)/(5−1) = 8/4 = **2**.
4. (x−3)² + (y+1)² = **25**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds on the coordinate basics in [[03_Special_Theorems_Coordinates_Solids]] and connects to circle theorems in [[02_Angles_Similarity_Circles]].*
