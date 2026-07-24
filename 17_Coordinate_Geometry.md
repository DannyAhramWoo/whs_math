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
6. Where a Line Meets a Circle (algebra)

---

## 1. Distance and Midpoint Formulas

> 📖 *Source: AOPS Introduction to Algebra §8.1 (Cartesian plane, distance formula) & §8.3 (midpoint). The distance formula is just the Pythagorean theorem on the coordinate grid.*

- **Distance formula** (from Pythagoras): distance between (x₁,y₁) and (x₂,y₂) = √[(x₂−x₁)² + (y₂−y₁)²].
  - Example: distance from (1,1) to (4,5) = √[3² + 4²] = √25 = 5.
- **Midpoint formula:** midpoint of (x₁,y₁) and (x₂,y₂) = ((x₁+x₂)/2, (y₁+y₂)/2) — just the **average** of the x's and of the y's.
  - Example: midpoint of (2,4) and (8,10) = (5,7).
- **Section (ratio) formula:** to find the point that divides the segment from P to Q in the ratio **m : n** (m parts from P), step that fraction of the way in each coordinate: the point is **(P + (m/(m+n))·(Q − P))** coordinate by coordinate.
  - Example: the point 1/3 of the way from (0,0) to (9,6) is (3, 2).

---

## 2. Slope

> 📖 *Source: AOPS Introduction to Algebra §8.2 "Slope" & §8.6 "Comparing Lines".*

- **Slope** m = (y₂−y₁)/(x₂−x₁) — measures steepness (rise over run). Positive slope rises left-to-right, negative falls, zero slope is horizontal (y=k), and a vertical line (x=h) has undefined slope.
  - Example: through (2,3) and (6,11): slope = (11−3)/(6−2) = 8/4 = 2.
- **Steepness by size:** a big slope (like 5) is nearly vertical; a small one (like 1/5) is nearly flat. |slope| > 1 rises faster than 45°, |slope| < 1 slower.
- **Collinearity test:** three points lie on **one line** exactly when the slope between each pair is the **same** (e.g. slope(A,B) = slope(B,C)).

> 💡 **Competition point:** Never swap the order of subtraction between numerator and denominator — always use the SAME point order in both.

---

## 3. Equations of a Line

> 📖 *Source: AOPS Introduction to Algebra §8.4 (point-slope & standard form) & §8.5 (slope-intercept, intercepts); horizontal/vertical lines in §8.7 Summary.*

- **Slope-intercept form:** y = mx + b — you can **read the slope (m) and y-intercept (b) straight off** the equation.
- **Point-slope form:** y − y₁ = m(x − x₁), built directly from the slope formula using one known point.
- **Standard form:** Ax + By = C (written with A > 0, integer coefficients, no common factor). Its **slope is −A/B** and its y-intercept is C/B — no rearranging needed.
- **Horizontal & vertical lines:** a horizontal line is **y = k** (slope 0); a vertical line is **x = h** (undefined slope). These don't fit y = mx + b, so know them separately.
- **x-intercept / y-intercept:** set y=0 to find the x-intercept, set x=0 to find the y-intercept. Quick way to graph a line — just plot both intercepts and connect them.
  - Example: for 2x + 3y = 12, x-intercept = (6,0), y-intercept = (0,4).

---

## 4. Parallel & Perpendicular Lines

> 📖 *Source: AOPS Introduction to Algebra §8.6 "Comparing Lines".*

- **Parallel lines** have EQUAL slopes.
- **Perpendicular lines** have slopes that are **negative reciprocals** of each other (their product = −1).
  - Example: a line perpendicular to slope 2/3 has slope −3/2.
- **Two lines = two equations:** solving them together gives **one** point (different slopes), **no** point (parallel — same slope, different intercept), or **infinitely many** (the same line). Comparing slopes tells you which before you solve.

---

## 5. Equation of a Circle

> 📖 *Source: standard analytic geometry (a direct application of the distance formula from §1). The circle equation isn't in our AOPS book excerpts, but it follows immediately: a point (x,y) is on the circle exactly when its distance to the centre equals r.*

- A circle with center (h,k) and radius r has equation (x−h)² + (y−k)² = r². (This just says "distance from (x,y) to (h,k) = r", squared.)
- If given a messy expanded equation, **complete the square** (for x and for y separately) to find the center and radius.
  - Example: x² − 4x + y² + 8y = 2 → (x−2)² + (y+4)² = 22, so center (2,−4), radius √22.

---

## 6. Where a Line Meets a Circle (algebra)

> 📖 *Source: standard analytic geometry. (Note: this algebraic substitution method is different from the synthetic **Power of a Point** theorem PA·PB = PC·PD in [[02_Angles_Similarity_Circles]] — that one relates segment lengths; this one finds the actual crossing points.)*

To find where a line crosses a circle: **substitute the line's equation into the circle's equation**, giving a quadratic in one variable — its roots are the crossing points.

> 💡 **Competition point:** Combining a line equation and a circle equation always reduces to solving ONE quadratic. The **discriminant** (see [[12_Equations_Algebra_Factoring]]) tells you how they meet: **positive** → two crossing points, **zero** → tangent (touches at one point), **negative** → the line misses the circle.

---

## Cheat Sheet

| Idea | Formula |
|------|---------|
| Distance | √[(x₂−x₁)² + (y₂−y₁)²] |
| Midpoint | ((x₁+x₂)/2, (y₁+y₂)/2) |
| Slope | (y₂−y₁)/(x₂−x₁) |
| 3 points collinear | equal slopes between pairs |
| Point-slope form | y−y₁ = m(x−x₁) |
| Standard form Ax+By=C | slope = −A/B |
| Horizontal / vertical line | y = k / x = h |
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
5. What is the slope of the line 3x + 4y = 12?
6. What is the equation of the horizontal line through (7, −2)?

<details>
<summary>Answers</summary>

1. √(9+16) = √25 = **5**.
2. ((−2+4)/2, (6−2)/2) = **(1, 2)**.
3. (10−2)/(5−1) = 8/4 = **2**.
4. (x−3)² + (y+1)² = **25**.
5. slope = −A/B = −3/4 → **−3/4**.
6. horizontal → y = k through y = −2 → **y = −2**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds on the coordinate basics in [[03_Special_Theorems_Coordinates_Solids]] and connects to circle theorems in [[02_Angles_Similarity_Circles]].*
