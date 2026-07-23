# 18. Inequalities & Quadratic Graphs

> **Unit:** Inequalities & Quadratic Graphs (Unit 18 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** Inequalities appear whenever a problem says "at most," "at least," or "find the range of possible values." Quadratic graphs (parabolas) give a visual way to see the max/min facts already used in [[12_Equations_Algebra_Factoring]].

---

## Lesson Overview
What this note covers:

1. Inequality Manipulation Rules
2. Absolute Value Inequalities
3. Quadratic Inequalities (Sign Analysis)
4. The Trivial Inequality and AM-GM
5. Parabolas and the Vertex

---

## 1. Inequality Manipulation Rules

- Adding/subtracting the same number from both sides keeps the direction the same.
- Multiplying/dividing by a **positive** number keeps the direction the same.
- Multiplying/dividing by a **negative** number **FLIPS** the inequality sign — the single most commonly missed step.
  - Example: −2x < 6 → dividing by −2 flips the sign: x > −3.
- **Compound inequalities** like a < x < b: apply the same operation to all three parts at once.

---

## 2. Absolute Value Inequalities

- Isolate the absolute value first.
- |expr| **>** k (k>0) splits into TWO separate ranges: "expr > k OR expr < −k".
- |expr| **<** k becomes ONE combined range: "−k < expr < k" (not "or").
  - Example: 4|x+3|+3 > 9 → |x+3| > 3/2 → x > −3/2 OR x < −9/2.

---

## 3. Quadratic Inequalities (Sign Analysis)

To solve something like (x−2)(x−5) < 0:

1. Find the roots (where each factor = 0) — these are the boundary points.
2. Test each interval between the roots to see if the product is positive or negative there.
3. For strict inequalities (<, >), exclude the boundary points; for ≤/≥, include them.

- Example: (x−2)(x−5) < 0 is true only BETWEEN the roots: 2 < x < 5 (since one factor is positive and one is negative in that range, making the product negative).

> 💡 **Competition point:** If the quadratic isn't factored, use the quadratic formula (see [[12_Equations_Algebra_Factoring]]) to find the roots first, THEN do the sign analysis.

---

## 4. The Trivial Inequality and AM-GM

- **Trivial Inequality:** for any real number x, x² ≥ 0 always (equality only when x=0). This "obvious" fact is the starting point for proving many other inequalities — rearrange an expression until it becomes a sum of squares.
- **AM-GM Inequality (core idea):** for positive numbers, their average (arithmetic mean) is always ≥ the geometric mean (nth root of the product); equality happens only when all the numbers are equal.
  - Example: for two positive numbers with a fixed sum a+b, their product ab is LARGEST when a=b.

> 💡 **Competition point:** "Find the maximum/minimum" word problems with a fixed sum or fixed product are usually AM-GM in disguise — check when equality can happen (both a bound AND an attainability check are needed).

---

## 5. Parabolas and the Vertex

- The graph of y = ax² + bx + c is a U-shaped curve called a **parabola**. It opens upward if a > 0 (has a minimum) and downward if a < 0 (has a maximum). The turning point is the **vertex**.
- **Vertex x-coordinate:** x = −b/(2a) — this is also the average of the two roots.
- **Vertex form:** y = a(x−h)² + k, where (h,k) is the vertex — get there by completing the square (see [[12_Equations_Algebra_Factoring]]).
  - Example: y = x² − 4x + 3 = (x−2)² − 1, so the vertex is (2,−1), minimum value −1.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Multiply/divide by negative | flips the inequality sign |
| \|expr\| > k | expr > k OR expr < −k |
| \|expr\| < k | −k < expr < k |
| Quadratic inequality | find roots, test each interval's sign |
| Trivial Inequality | x² ≥ 0 always |
| AM-GM (2 numbers) | (a+b)/2 ≥ √(ab), equal only when a=b |
| Vertex x-coordinate | −b/(2a) = average of the roots |
| Vertex form | y = a(x−h)²+k |

---

## Quick Check

1. Solve: 3 − 2x > 7.
2. Solve: |x − 4| < 3.
3. Solve: (x+1)(x−3) ≥ 0.
4. Find the vertex of y = x² − 6x + 5.

<details>
<summary>Answers</summary>

1. −2x > 4 → dividing by −2 flips → x < **−2**.
2. −3 < x−4 < 3 → **1 < x < 7**.
3. Roots at x=−1, x=3. Product ≥0 outside or on the roots → **x ≤ −1 or x ≥ 3**.
4. x = −(−6)/(2×1) = 3 → y = 9−18+5 = −4 → vertex **(3, −4)**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds directly on the quadratic formula/discriminant in [[12_Equations_Algebra_Factoring]].*
