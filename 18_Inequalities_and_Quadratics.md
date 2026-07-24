# 18. Inequalities & Quadratic Graphs

> **Unit:** Inequalities & Quadratic Graphs (Unit 18 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** Inequalities appear whenever a problem says "at most," "at least," or "find the range of possible values." Quadratic graphs (parabolas) give a visual way to see the max/min facts already used in [[12_Equations_Algebra_Factoring]].

---

## Lesson Overview
What this note covers:

1. Inequality Manipulation Rules
2. Absolute Value Inequalities
3. Quadratic & Rational Inequalities (Sign Analysis)
4. The Trivial Inequality and AM-GM
5. Parabolas and the Vertex

---

## 1. Inequality Manipulation Rules

> 📖 *Source: AOPS Introduction to Algebra Ch.9 "Introduction to Inequalities" — §9.1 (the basics), §9.3 (linear inequalities & interval notation), §9.6 Summary.*

- Adding/subtracting the same number from both sides keeps the direction the same.
- Multiplying/dividing by a **positive** number keeps the direction the same.
- Multiplying/dividing by a **negative** number **FLIPS** the inequality sign — the single most commonly missed step.
  - Example: −2x < 6 → dividing by −2 flips the sign: x > −3.
- **Transitivity:** if a > b and b > c, then a > c.
- **Adding two inequalities:** if a > b and c > d, then **a + c > b + d** (add same-direction inequalities freely).
- **Multiplying two inequalities — only when all parts are positive:** if a > b > 0 and c > d > 0, then ac > bd. (Don't multiply inequalities that involve negatives — the sign can go wrong.)
- **Compound inequalities** like a < x < b: apply the same operation to all three parts at once.
- **Interval / number-line notation:** write the solution as an interval — `2 < x < 5` is **(2, 5)**; `x ≤ −1 or x ≥ 3` is **(−∞, −1] ∪ [3, ∞)**. A round bracket excludes the endpoint (strict <), a square bracket includes it (≤).

---

## 2. Absolute Value Inequalities

> 📖 *Source: AOPS Introduction to Algebra §20.2 covers **absolute value as distance** and abs-value *equations* (|2x−9| = 5) by casework; the |x| < k / |x| > k **inequality** split below is the standard extension of that distance idea.*

- **|x| means distance from 0.** So |x| = 3 means x is 3 away from 0 → x = 3 or −3. Inequalities follow from this "distance" picture:
- Isolate the absolute value first.
- |expr| **>** k (k>0) means "**farther than k from 0**" → splits into TWO separate ranges: "expr > k OR expr < −k".
- |expr| **<** k means "**within k of 0**" → ONE combined range: "−k < expr < k" (not "or").
  - Example: 4|x+3|+3 > 9 → |x+3| > 3/2 → x > −3/2 OR x < −9/2.

---

## 3. Quadratic & Rational Inequalities (Sign Analysis)

> 📖 *Source: AOPS Introduction to Algebra Ch.15 "More Inequalities" — §15.1 (quadratic inequalities), §15.2 (rational & higher-degree).*

To solve something like (x−2)(x−5) < 0:

1. Find the roots (where each factor = 0) — these are the boundary points.
2. Test each interval between the roots to see if the product is positive or negative there.
3. For strict inequalities (<, >), exclude the boundary points; for ≤/≥, include them.

- Example: (x−2)(x−5) < 0 is true only BETWEEN the roots: 2 < x < 5 (since one factor is positive and one is negative in that range, making the product negative).
- **More than two factors:** the same interval-testing works for (x−1)(x−2)(x−3) etc. — mark all the roots on a number line, then check the sign in each piece.
- **Rational inequalities (a fraction):** treat the numerator's and denominator's roots as boundary points. ⚠️ **The denominator's roots are never allowed** (they make it undefined), so those points are always **excluded**, even for ≤/≥.
- **Link to the discriminant:** if a quadratic has **no real roots** (discriminant < 0), it never crosses the x-axis, so it keeps **one sign everywhere** — always positive (if it opens up) or always negative (opens down).

> 💡 **Competition point:** If the quadratic isn't factored, use the quadratic formula (see [[12_Equations_Algebra_Factoring]]) to find the roots first, THEN do the sign analysis.

---

## 4. The Trivial Inequality and AM-GM

> 📖 *Source: AOPS Introduction to Algebra §15.3 "The Trivial Inequality" — x² ≥ 0 and the (a²+b²)/2 ≥ ab form. The named "AM–GM / √(ab)" statement is the standard competition version (the book proves the equivalent square form rather than naming it).*

- **Trivial Inequality:** for any real number x, x² ≥ 0 always (equality only when x=0). This "obvious" fact is the starting point for proving many other inequalities — rearrange an expression until it becomes a **sum of squares**.
- **The book's key consequence:** since (a − b)² ≥ 0, expanding gives **(a² + b²)/2 ≥ ab**. Another famous one: for any positive x, **x + 1/x ≥ 2** (from (√x − 1/√x)² ≥ 0).
- **Proof technique — work backwards, then write it forwards:** to *prove* an inequality, work back from it to something obviously true (a square ≥ 0), then reverse the steps to present it. (You can't just manipulate the thing you're trying to prove as if it's already true.)
- **AM-GM Inequality (the named √ version):** for positive numbers, their **arithmetic mean ≥ geometric mean**; for two numbers **(a + b)/2 ≥ √(ab)**, with equality only when a = b.
  - Example: for two positive numbers with a fixed sum a+b, their product ab is LARGEST when a=b.

> 💡 **Competition point:** "Find the maximum/minimum" word problems with a fixed sum or fixed product are usually AM-GM in disguise — check when equality can happen (both a bound AND an attainability check are needed).

---

## 5. Parabolas and the Vertex

> 📖 *Source: AOPS Introduction to Algebra Ch.14 "Graphing Quadratics" (parabola shape, vertex, axis of symmetry) & §15.4 "Quadratic Optimization" (max/min via completing the square).*

- The graph of y = ax² + bx + c is a U-shaped curve called a **parabola**. It opens upward if a > 0 (has a **minimum**) and downward if a < 0 (has a **maximum**). The turning point is the **vertex**.
- **|a| controls the width:** the bigger |a| is, the **narrower** the parabola; small |a| makes it wide.
- **Axis of symmetry:** the vertical line **x = −b/(2a)** through the vertex — the parabola is a mirror image across it.
- **Vertex x-coordinate:** x = −b/(2a) — this is also the **average of the two roots** (they sit symmetrically either side).
- **Intercepts:** the y-intercept is (0, c); the x-intercepts (if any) are the roots. No real roots (discriminant < 0) → the parabola never touches the x-axis.
- **Vertex form:** y = a(x−h)² + k, where (h,k) is the vertex — get there by completing the square (see [[12_Equations_Algebra_Factoring]]). Reading it as a **shift**: start from y = x², move **h** right and **k** up.
  - Example: y = x² − 4x + 3 = (x−2)² − 1, so the vertex is (2,−1), minimum value −1.
- **Why the vertex is the max/min (the optimization argument):** in vertex form a(x−h)² + k, the square (x−h)² ≥ 0 (Trivial Inequality), so if a > 0 the smallest y is k (at x = h); if a < 0 the largest y is k. That's why completing the square finds the extreme value.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Multiply/divide by negative | flips the inequality sign |
| Add two inequalities | same direction: a>b, c>d ⟹ a+c>b+d |
| Multiply two inequalities | only if all parts positive |
| Interval notation | (2,5) excludes ends; [2,5] includes them |
| \|expr\| > k | expr > k OR expr < −k (far from 0) |
| \|expr\| < k | −k < expr < k (near 0) |
| Quadratic inequality | find roots, test each interval's sign |
| Rational inequality | denominator's roots always excluded |
| Trivial Inequality | x² ≥ 0 always → (a²+b²)/2 ≥ ab, x+1/x ≥ 2 |
| AM-GM (2 numbers) | (a+b)/2 ≥ √(ab), equal only when a=b |
| Parabola width | bigger \|a\| → narrower |
| Axis of symmetry | x = −b/(2a) |
| Vertex x-coordinate | −b/(2a) = average of the roots |
| Vertex form | y = a(x−h)²+k; min/max = k (Trivial Ineq) |

---

## Quick Check

1. Solve: 3 − 2x > 7.
2. Solve: |x − 4| < 3.
3. Solve: (x+1)(x−3) ≥ 0.
4. Find the vertex of y = x² − 6x + 5.
5. Write the solution of question 3 in interval notation.
6. What is the minimum value of y = 2(x − 4)² + 7, and where does it occur?

<details>
<summary>Answers</summary>

1. −2x > 4 → dividing by −2 flips → x < **−2**.
2. −3 < x−4 < 3 → **1 < x < 7**.
3. Roots at x=−1, x=3. Product ≥0 outside or on the roots → **x ≤ −1 or x ≥ 3**.
4. x = −(−6)/(2×1) = 3 → y = 9−18+5 = −4 → vertex **(3, −4)**.
5. **(−∞, −1] ∪ [3, ∞)** (square brackets since ≥ includes the roots).
6. The square is ≥ 0, so the minimum is **7**, at **x = 4**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds directly on the quadratic formula/discriminant in [[12_Equations_Algebra_Factoring]].*
