# 12. Equations, Algebraic Manipulation & Factoring

> **Unit:** Algebra Toolkit (Unit 12 of 14) · **13 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Word problems and puzzles almost always hide an **equation**. If you can name a variable, write the condition as an equation, and factor cleverly, hard-looking problems become short.

---

## Lesson Overview
What this note covers:

1. Setting Up & Solving Equations
2. Simultaneous Equations — *Sec 1*
3. Factoring — *Sec 1*
4. Algebraic Manipulation — *Sec, advanced*

---

## 1. Setting Up & Solving Equations

- **Equation:** a math sentence with an **equals sign** and an unknown letter. Example: 2x + 3 = 11 → x = 4.
- **The 4 steps (always follow in order):**
  1. **What to find?** — decide the exact thing the question asks.
  2. **Choose a variable** — call that unknown *x* (or *a*, *n*, …).
  3. **Condition = equation** — turn the words of the problem into an equation.
  4. **Solve** — do the same thing to both sides until the letter is alone.
- **Example:** "23 coins are worth 320 cents." Let *x* = number of one kind of coin, write the money total as an equation, then solve. (→ Mock Q2-18 below.)

> 💡 **Competition point:** The hard part is usually **step 3**, not the algebra. Read the sentence slowly and write "left side = right side" exactly as the words say.

---

## 2. Simultaneous Equations — *Sec 1*

- **Simultaneous equations:** **two (or more) equations** that must be true at the **same time**, with two (or more) unknowns.
- **Elimination:** add or subtract the equations so **one variable cancels**.
  - Example: from x + y = 10 and x − y = 4, add them → 2x = 14 → x = 7, then y = 3.
- **Substitution:** solve one equation for a letter, then **put that into the other** equation.
  - Example: y = 10 − x, then use it in the second equation to get one unknown.
- **Three variables (Sec 1):** if you have 3 equations, **subtract one equation from another** to get rid of a variable. Keep reducing until one letter is left.

> 💡 **Competition point:** When two equations look almost the same, **subtract them** — the messy parts often cancel and leave a simple answer (→ RI 2024 Q03: x + y/z = 15 and y + x/z = 20).

---

## 3. Factoring — *Sec 1*

- **Factoring:** writing an expression as a **product** (things multiplied). It is the reverse of expanding.
- **Common factor:** pull out what every term shares. **ax + ay = a(x + y)**.
  - Example: 6n + 9 = 3(2n + 3).
- **Perfect square:** **(a ± b)² = a² ± 2ab + b²**.
  - Example: x² + 6x + 9 = (x + 3)².
- **Difference of squares (⭐ most useful):** **a² − b² = (a + b)(a − b)**.
  - Example: 41² − 39² = (41 + 39)(41 − 39) = 80 × 2 = 160 (no long multiplying!).
- **Sum/Difference of cubes (advanced):** **a³ ± b³ = (a ± b)(a² ∓ ab + b²)**.

> 💡 **Competition point:** When you see **a big subtraction of two squares**, don't calculate each square. Use a² − b² = (a+b)(a−b) — it turns huge numbers into an easy product (→ RMO 2025 Q11).

---

## 4. Algebraic Manipulation — *Sec, advanced*

- **Linear combination:** build the thing you want by **adding multiples** of the equations you have (like aX + bY). You don't always need each letter's value — just the right mix.
  - Example: combine two people's price equations to find a total (→ AP 2025 Q18).
- **Symmetric expressions (advanced):** if you know **x + y** and **xy**, then x and y are the **roots of** t² − (x + y)t + xy = 0. Symmetric sums (x + y, xy) often solve the whole problem without finding x and y separately.
- **Optimization with AM–GM (advanced):** for positive a and b, **a + b ≥ 2√(ab)**, and they are **equal when a = b**. This is the quick way to find a **maximum or minimum** (→ Mock Q1-34: split time to maximise a product).

> 💡 **Competition point:** If a problem asks for the **biggest product with a fixed sum**, the answer is usually when the two parts are **equal**. That is AM–GM in disguise.

---

## 📚 From the Books (extra tricks)

- **Consecutive-integer sums:** N can be written as a sum of 2 or more consecutive positive integers **unless N is a power of 2**. Count the **odd factors of N** (including 1) — call that k — and there are exactly **k − 1** ways.
  - Example: 1995 = 3 × 5 × 7 × 19 has 2⁴ = 16 odd factors → **15 ways** to write 1995 as a sum of consecutive positive integers.
- **Middle-term trick:** for consecutive integers, the sum = (**middle term**) × (**count of terms**) when the count is **odd**. When the count is **even**, use the **average of the two middle terms** instead.
  - Example: 6 consecutive integers add to 2019 → average = 2019 ÷ 6 = 336.5 → the terms sit around 336.5, so they run 334…339 (largest = **339**).

> 💡 **Competition point (SFFT — very famous, very useful):** an expression like **xy + ax + by** can be forced into a product by adding **ab** to both sides: **(x + b)(y + a) = (constant) + ab**. This turns a 2-variable equation into a **factor-pair search**.
> - Example: xy + 3x + 2y = 16 → add 6 to both sides → xy + 3x + 2y + 6 = 22 → **(x + 2)(y + 3) = 22**. List the factor pairs of 22 to find every integer (x, y).

- **Completing the square:** to turn x² + bx into a perfect square, add **(b/2)²**. This solves *any* quadratic, even ones that don't factor nicely.
  - Example: x² + 8x = 14 → add 16 to both sides → (x + 4)² = 30 → x = −4 ± √30.
- **The Quadratic Formula:** completing the square on ax² + bx + c = 0 in general gives **x = (−b ± √(b² − 4ac)) / (2a)**.
- **The Discriminant (b² − 4ac):** tells you the *type* of roots without solving — **positive** → 2 different real roots, **zero** → 1 repeated root, **negative** → no real roots.
- **Vieta's Formulas (full version):** for ax² + bx + c = 0 with roots r and s: **r + s = −b/a** and **r × s = c/a**. Read the sum/product straight off the coefficients — no need to solve at all.
- **Coefficient-matching:** if Ax + B and Cx + D are equal for **every** value of x (not just one), then **A = C and B = D**. Fast way to find them: plug in an easy value like **x = 0** to isolate one equation instantly.
- **Rationalizing with a conjugate:** for a denominator like c + √d, multiply top and bottom by its conjugate **c − √d**, since (c + √d)(c − √d) = **c² − d** removes the square root.
- **Nested radicals:** for something like √(6+√11) + √(6−√11), let x = the whole expression and **square it** — the cross term collapses because √((6+√11)(6−√11)) = √(36−11) = √25 = 5.

> 💡 **Competition point (Telescoping — another very high-value trick):** rewrite each term of a sum or product as a **difference of two simpler pieces**, so that writing out all the terms, the **middle ones cancel** and only the first and last survive.
> - Sum example: 1/(1×2) + 1/(2×3) + … + 1/(99×100) = (1 − 1/2) + (1/2 − 1/3) + … + (1/99 − 1/100) = 1 − 1/100 = **99/100**.
> - Product example: (3/1) × (4/2) × (5/3) × … × (40/38) — each term shares a factor with its neighbour, so it collapses to (39 × 40)/(1 × 2) = **780**.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Word problem | 4 steps: find → variable → equation → solve |
| Two unknowns | elimination (cancel) or substitution |
| Three unknowns | subtract equations to reduce |
| Common factor | ax + ay = a(x + y) |
| Perfect square | (a ± b)² = a² ± 2ab + b² |
| Difference of squares ⭐ | a² − b² = (a + b)(a − b) |
| Cubes (advanced) | a³ ± b³ = (a ± b)(a² ∓ ab + b²) |
| Know x+y and xy | roots of t² − (x+y)t + xy = 0 |
| Max product, fixed sum | equal parts (AM–GM) |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Equations (linear & simultaneous)**
- [NM 2008 Q16](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/16.png) — chess wins/losses and chocolate exchange; find the total number of games
- [Mock Q2-18](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_18.png) — 5-, 10-, 25-cent coins: 23 coins worth 320 cents; difference of 25c and 5c coins
- [Mock Q4-25](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_25.png) — 100 problems with a scoring rule; most correct answers that still score 50
- [Mock Q4-3](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_3.png) — three numbers sum to 2015 with three given pair-sums; find m
- [RI 2024 Q03](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/03.png) — x + y/z = 15 and y + x/z = 20; find (x + y)/z → *subtract the equations*
- [AP 2025 Q07](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/07.png) — xy = 10(x + y) = 15(x − y); find x + y
- [AP 2025 Q24](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/24.png) — equal area when length −14 and width +8; find the perimeter

**② Factoring**
- [RMO 2025 Q09](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/09.png) — a difference in AB − CD form; regroup the terms to factor
- [RMO 2025 Q11](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/11.png) — (odd squares − even squares) ÷ (odd sum − even sum) → *difference of squares*
- [AP 2021 Q04](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/04.png) — a table total that equals (row sum) × (column sum)

**③ Algebraic manipulation**
- [RI 2023 Q03](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/03.png) — the difference of the products of two big fraction sums
- [AP 2025 Q18](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/18.png) — combine Wang's and Li's equations to get prices 56, 108, 52 → *linear combination*
- [Mock Q1-34](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_34.png) — split 10 hours of exercise and reading to maximise mood × stamina → *AM–GM*

---

## Quick Check

1. Solve the pair: x + y = 20 and x − y = 6. Find x and y.
2. Use a shortcut to compute 53² − 47².
3. Factor fully: 8m + 12.
4. Three numbers add to 30. The pair-sums of two pairs are 19 and 21. Find the third number's partner sums — actually, find all three numbers.
5. You will split 12 into two positive parts to make their **product** as big as possible. What are the two parts?

<details>
<summary>Answers</summary>

1. Add: 2x = 26 → x = 13; then y = 20 − 13 = **7** (so x = 13, y = 7)
2. 53² − 47² = (53 + 47)(53 − 47) = 100 × 6 = **600**
3. 8m + 12 = **4(2m + 3)**
4. Let the numbers be a, b, c with a+b+c = 30. If a+b = 19 then c = 11; if a+c = 21 then b = 9; so a = 30 − 9 − 11 = 10 → **10, 9, 11**
5. Equal parts give the biggest product: 6 and 6 → **6 and 6** (product 36)

</details>

---
*Source map: `약점진단/12_방정식_식조작_인수분해.md` · Puzzle-style reasoning continues in [[13_Logic_and_Magic_Squares]]*
