# 19. Functions

> **Unit:** Functions (Unit 19 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** "Function" language (f(x), domain, floor/ceiling) shows up in harder word problems and custom-operator problems, which already appear in [[12_Equations_Algebra_Factoring]].

---

## Lesson Overview
What this note covers:

1. What is a Function
2. Composition and Inverses — *Sec 2*
3. Domain and Range
4. Graph Transformations
5. Floor, Ceiling, Piecewise & Absolute Value

---

## 1. What is a Function

> 📖 *Source: AOPS Introduction to Algebra Ch.16 "Functions" — §16.1 (the "machine" idea), §16.6 (custom operations).*

- A **function** is a rule (a "machine") that takes an input and gives exactly ONE output — like f(x) = 2x + 3.
- **Evaluate by substitution:** f(5) = 2·5 + 3 = 13. You can also feed in an **expression**: f(2k) = 2·(2k) + 3 = 4k + 3.
- If a single input could give more than one output, it's NOT a function.
- A function doesn't have to be a formula — it can be given by a **table** or a set of input→output pairs.
- This is the same idea as the **custom-defined operators** already in [[12_Equations_Algebra_Factoring]] (like a♦b = a²+ab−b²) — a function is just a rule you evaluate by substitution.

> ⚠️ **Warning:** f²(x) usually means **f(f(x))** (apply f twice), *not* f(x)·f(x). Read the problem's definition carefully.

---

## 2. Composition and Inverses — *Sec 2*

> 📖 *Source: AOPS Introduction to Algebra §16.2 (combining functions), §16.3 (composition), §16.4 (inverse functions).*

- **Combining functions:** you can add, subtract, multiply or divide two functions — (f + g)(x) = f(x) + g(x), and so on.
- **Composition f(g(x))** (also written (f∘g)(x)): put x into g **first**, then feed g's output into f.
  - Example: f(x) = x + 1, g(x) = 2x → f(g(x)) = f(2x) = 2x + 1. (Order matters: g(f(x)) = 2(x+1) = 2x + 2 is different.)
- **Inverse function f⁻¹:** the function that **undoes** f — if f sends 3 → 7, then f⁻¹ sends 7 → 3. Formally f(f⁻¹(x)) = x and f⁻¹(f(x)) = x.
  - To find it: write y = f(x), swap x and y, then solve for y. E.g. f(x) = 2x + 1 → x = 2y + 1 → **f⁻¹(x) = (x − 1)/2**.

---

## 3. Domain and Range

> 📖 *Source: AOPS Introduction to Algebra §16.1 (domain/range), §16.7 Summary (range-finding method).*

- **Domain:** every input value that's allowed (doesn't break the rule — like dividing by zero, or taking the square root of a negative number).
- **Range:** every possible output value.
  - Example: f(x) = 1/(x−3) has domain "all reals except 3" (can't divide by 0) and range "all reals except 0" (the fraction can never equal exactly 0).
- **Finding the range:** set y = f(x) and solve for x in terms of y; the y-values for which a valid x exists are the range.

---

## 4. Graph Transformations

> 📖 *Source: AOPS Introduction to Algebra Ch.17 "Graphing Functions" — §17.1 (graphs, vertical-line test), §17.2 (transformations).*

- **A function's graph is y = f(x).** Because each input has exactly one output, **any vertical line hits the graph at most once** (the "vertical-line test" — a quick way to check something is a function).

The basic moves on a graph, given the original y = f(x):

| Change | Effect |
|--------|--------|
| f(x) + k | shifts UP by k (down if k < 0) |
| f(x − h) | shifts RIGHT by h (careful — the sign looks backwards!) |
| −f(x) | reflects over the **x-axis** (upside down) |
| f(−x) | reflects over the **y-axis** (left-right mirror) |
| a·f(x) | vertical stretch by a (if a > 1); **squash** if 0 < a < 1 |
| f(a·x) | horizontal squash by a (if a > 1); stretch if 0 < a < 1 |

- **Why f(x − h) shifts *right*:** to get the same output the machine used to give at x, you now have to feed in a value that's h **bigger**, so every point slides right. Test with a point if unsure.
- Example: if f(x) = x², then f(x−3)+2 = (x−3)²+2 is the same parabola moved 3 right and 2 up.

> 💡 **Competition point:** f(x−h) shifts RIGHT, not left — a common mix-up. And changes **inside** f(...) affect the graph **horizontally** (backwards-looking); changes **outside** affect it **vertically** (the intuitive way).

---

## 5. Floor, Ceiling, Piecewise & Absolute Value

> 📖 *Source: AOPS Introduction to Algebra Ch.20 "Special Functions" — §20.2 (absolute value), §20.3 (floor & ceiling), §20.5 (piecewise).*

- **Floor function ⌊x⌋** (also called the **greatest integer function**, sometimes written [x]): the greatest integer ≤ x ("round down"). ⌊4.7⌋ = 4, but for negatives it's NOT the same as truncating: ⌊−5.3⌋ = **−6**, not −5.
- **Ceiling function ⌈x⌉:** the smallest integer ≥ x ("round up"). ⌈3.2⌉ = 4, ⌈−2.3⌉ = −2.
- **Floor/ceiling of a surd — bracket between squares:** to find ⌊√39⌋, note 6² = 36 ≤ 39 < 49 = 7², so 6 < √39 < 7 → ⌊√39⌋ = **6** (and ⌈√39⌉ = 7).
- **Fractional part:** {x} = x − ⌊x⌋, always between 0 (inclusive) and 1 (exclusive). So every number splits as **x = ⌊x⌋ + {x}** (integer part + fractional part).
- **Piecewise function:** a function defined by different rules on different pieces of the domain, e.g. f(x) = 2x if x < 0, and 3x if x ≥ 0. Evaluate by first checking **which piece** the input falls in.
- **Absolute value |x|:** the distance from x to 0 — always non-negative, and |x| = √(x²). Split by the sign: |x| = x if x ≥ 0, and −x if x < 0. |x−a| means "distance from x to a."
  - Example: |x+3| + |x−2| = 7 — split into cases based on where each inside expression changes sign (x < −3, −3 ≤ x < 2, x ≥ 2), solve each case, then check the solution actually falls in that case's range.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Function | one input → exactly one output |
| f²(x) | means f(f(x)), not f(x)² |
| Composition f(g(x)) | do g first, then f (order matters) |
| Inverse f⁻¹ | undoes f; swap x,y and solve |
| Vertical-line test | a function's graph: each vertical line hits once |
| Domain | allowed inputs |
| Range | possible outputs; set y=f(x), solve for x |
| f(x)+k | shift up |
| f(x−h) | shift right (inside = horizontal, backwards) |
| −f(x) / f(−x) | flip over x-axis / y-axis |
| a·f(x) | stretch (a>1) or squash (0<a<1) |
| ⌊x⌋ | round down (careful with negatives!) |
| ⌈x⌉ | round up |
| ⌊√n⌋ | bracket n between consecutive squares |
| Piecewise | different rule on each piece; check which |
| \|x−a\| | distance from x to a; \|x\|=√(x²) |

---

## Quick Check

1. What is ⌊7.9⌋? What is ⌈7.1⌉?
2. What is ⌊−3.2⌋?
3. If f(x) = x² − 1, what is the domain and range?
4. Sketch (in words) how y = f(x−2) − 1 relates to y = f(x).
5. If f(x) = x + 4 and g(x) = 3x, find f(g(2)) and g(f(2)).
6. Find the inverse of f(x) = 3x − 6.
7. What is ⌊√50⌋?

<details>
<summary>Answers</summary>

1. ⌊7.9⌋ = **7**, ⌈7.1⌉ = **8**.
2. **−4** (round down, away from zero for negatives).
3. Domain = all reals. Range = **y ≥ −1** (since x² ≥ 0, so x²−1 ≥ −1).
4. Shift **right by 2, then down by 1**.
5. f(g(2)) = f(6) = **10**; g(f(2)) = g(6) = **18** (order matters).
6. y = 3x − 6 → x = 3y − 6 → **f⁻¹(x) = (x + 6)/3**.
7. 7² = 49 ≤ 50 < 64 = 8² → **7**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Connects to custom operators in [[12_Equations_Algebra_Factoring]] and graphing in [[17_Coordinate_Geometry]].*
