# 19. Functions

> **Unit:** Functions (Unit 19 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** "Function" language (f(x), domain, floor/ceiling) shows up in harder word problems and custom-operator problems, which already appear in [[12_Equations_Algebra_Factoring]].

---

## Lesson Overview
What this note covers:

1. What is a Function
2. Domain and Range
3. Graph Transformations
4. Floor, Ceiling, and Absolute Value Functions

---

## 1. What is a Function

- A **function** is a rule that takes an input and gives exactly ONE output — like f(x) = 2x + 3.
- If a single input could give more than one output, it's NOT a function.
- This is the same idea as the **custom-defined operators** already in [[12_Equations_Algebra_Factoring]] (like a♦b = a²+ab−b²) — a function is just a formula you evaluate by substitution.

---

## 2. Domain and Range

- **Domain:** every input value that's allowed (doesn't break the rule — like dividing by zero, or taking the square root of a negative number).
- **Range:** every possible output value.
  - Example: f(x) = 1/(x−3) has domain "all reals except 3" (can't divide by 0) and range "all reals except 0" (the fraction can never equal exactly 0).

---

## 3. Graph Transformations

Four basic moves on a graph, given the original y = f(x):

| Change | Effect |
|--------|--------|
| f(x) + k | shifts UP by k |
| f(x − h) | shifts RIGHT by h (careful — the sign looks backwards!) |
| −f(x) | flips vertically (upside down) |
| a·f(x) | stretches vertically by factor a |

- Example: if f(x) = x², then f(x−3)+2 = (x−3)²+2 is the same parabola moved 3 right and 2 up.

> 💡 **Competition point:** f(x−h) shifts RIGHT, not left — a common mix-up. Test it with an easy point if unsure.

---

## 4. Floor, Ceiling, and Absolute Value Functions

- **Floor function ⌊x⌋:** the greatest integer ≤ x ("round down"). ⌊4.7⌋ = 4, but for negatives it's NOT the same as truncating: ⌊−5.3⌋ = **−6**, not −5.
- **Ceiling function ⌈x⌉:** the smallest integer ≥ x ("round up"). ⌈3.2⌉ = 4, ⌈−2.3⌉ = −2.
- **Fractional part:** {x} = x − ⌊x⌋, always between 0 (inclusive) and 1 (exclusive).
- **Absolute value |x|:** the distance from x to 0 — always non-negative. |x−a| means "distance from x to a."
  - Example: |x+3| + |x−2| = 7 — split into cases based on where each inside expression changes sign (x < −3, −3 ≤ x < 2, x ≥ 2), solve each case, then check the solution actually falls in that case's range.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Function | one input → exactly one output |
| Domain | allowed inputs |
| Range | possible outputs |
| f(x)+k | shift up |
| f(x−h) | shift right |
| −f(x) | flip vertically |
| ⌊x⌋ | round down (careful with negatives!) |
| ⌈x⌉ | round up |
| \|x−a\| | distance from x to a |

---

## Quick Check

1. What is ⌊7.9⌋? What is ⌈7.1⌉?
2. What is ⌊−3.2⌋?
3. If f(x) = x² − 1, what is the domain and range?
4. Sketch (in words) how y = f(x−2) − 1 relates to y = f(x).

<details>
<summary>Answers</summary>

1. ⌊7.9⌋ = **7**, ⌈7.1⌉ = **8**.
2. **−4** (round down, away from zero for negatives).
3. Domain = all reals. Range = **y ≥ −1** (since x² ≥ 0, so x²−1 ≥ −1).
4. Shift **right by 2, then down by 1**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Connects to custom operators in [[12_Equations_Algebra_Factoring]] and graphing in [[17_Coordinate_Geometry]].*
