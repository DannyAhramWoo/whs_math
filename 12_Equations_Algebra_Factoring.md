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

> 📖 *Source: AOPS Introduction to Algebra Ch.3 "Linear Equations" — §3.1–3.2 (solving), §3.3 (word problems). The book's method adds a 5th step: check.*

- **Equation:** a math sentence with an **equals sign** and an unknown letter. Example: 2x + 3 = 11 → x = 4.
- **The 5 steps (always follow in order):**
  1. **What to find?** — decide the exact thing the question asks.
  2. **Choose a variable** — call that unknown *x* (or *a*, *n*, …).
  3. **Condition = equation** — turn the words of the problem into an equation.
  4. **Solve** — do the same thing to both sides until the letter is alone.
  5. **Check** — put your answer back into the original words to be sure it fits (the book always does this).
- **Example:** "23 coins are worth 320 cents." Let *x* = number of one kind of coin, write the money total as an equation, then solve. (→ Mock Q2-18 below.)
- **How many solutions?** A linear equation can have **one** solution (the usual case), **no** solution (it reduces to something false like 0 = 5), or **infinitely many** (it reduces to something always true like 0 = 0). If your variable cancels out, check which of these happened.

> 💡 **Competition point:** The hard part is usually **step 3**, not the algebra. Read the sentence slowly and write "left side = right side" exactly as the words say.

---

## 2. Simultaneous Equations — *Sec 1*

> 📖 *Source: AOPS Introduction to Algebra Ch.5 "Systems of Linear Equations" — §5.2 (substitution), §5.3 (elimination), §5.6 (more variables), §5.7 Summary.*

- **Simultaneous equations:** **two (or more) equations** that must be true at the **same time**, with two (or more) unknowns.
- **Elimination:** add or subtract the equations so **one variable cancels**. Often you must **scale one equation first** so a variable's coefficients match.
  - Example: from x + y = 10 and x − y = 4, add them → 2x = 14 → x = 7, then y = 3.
  - Scaling example: 2x + 3y = 13 and x + y = 5 → double the second (2x + 2y = 10) → subtract → y = 3.
- **Substitution:** solve one equation for a letter, then **put that into the other** equation.
  - Example: y = 10 − x, then use it in the second equation to get one unknown.
- **Three variables (Sec 1):** if you have 3 equations, **subtract one equation from another** to get rid of a variable. Keep reducing until one letter is left.
- **Two lines, three outcomes:** two linear equations cross at **one** point (usual), never meet (**parallel** — no solution), or are the **same line** (infinitely many solutions). If elimination kills *both* variables, you've hit one of the last two cases.

> 💡 **Competition point:** When two equations look almost the same, **subtract them** — the messy parts often cancel and leave a simple answer (→ RI 2024 Q03: x + y/z = 15 and y + x/z = 20).

---

## 3. Factoring — *Sec 1*

> 📖 *Source: AOPS Introduction to Algebra Ch.11 "Special Factorizations" — §11.1 (squares of binomials), §11.2 (difference of squares), §11.3 (cubes); factoring quadratics is Ch.10 §10.2–10.3.*

- **Factoring:** writing an expression as a **product** (things multiplied). It is the reverse of expanding.
- **Common factor:** pull out what every term shares. **ax + ay = a(x + y)**.
  - Example: 6n + 9 = 3(2n + 3).
- **Factoring a quadratic x² + bx + c:** find two numbers that **multiply to c and add to b**; then x² + bx + c = (x + p)(x + q). When the leading coefficient isn't 1 (like 6x² + 11x + 3), look for factors of (first × last) that add to the middle, or split the middle term.
- **Zero-product property (why factoring solves equations):** if a **product is 0**, then one of the factors is 0. So (x − 2)(x + 5) = 0 means x = 2 **or** x = −5. This is the whole reason we factor to solve.
- **Perfect square:** **(a ± b)² = a² ± 2ab + b²**.
  - Example: x² + 6x + 9 = (x + 3)². (Handy for mental math: 31² = (30+1)² = 900 + 60 + 1 = 961.)
- **Difference of squares (⭐ most useful):** **a² − b² = (a + b)(a − b)**.
  - Example: 41² − 39² = (41 + 39)(41 − 39) = 80 × 2 = 160 (no long multiplying!).
- **Sum/Difference of cubes (advanced):** **a³ ± b³ = (a ± b)(a² ∓ ab + b²)**.

> 💡 **Competition point:** When you see **a big subtraction of two squares**, don't calculate each square. Use a² − b² = (a+b)(a−b) — it turns huge numbers into an easy product (→ RMO 2025 Q11).

---

## 4. Algebraic Manipulation — *Sec, advanced*

> 📖 *Source: AOPS Introduction to Algebra — linear combinations & symmetric systems Ch.22 §22.3; AM–GM as the "Trivial Inequality" Ch.15 §15.3; quadratic optimization §15.4.*

- **Linear combination:** build the thing you want by **adding multiples** of the equations you have (like aX + bY). You don't always need each letter's value — just the right mix.
  - Example: combine two people's price equations to find a total (→ AP 2025 Q18).
- **Symmetric systems (advanced):** if a system doesn't change when you swap the letters, **add all the equations** (and/or subtract them) to get simpler symmetric combinations like x + y and xy.
- **Symmetric expressions (advanced):** if you know **x + y** and **xy**, then x and y are the **roots of** t² − (x + y)t + xy = 0. Also **x² + y² = (x + y)² − 2xy** — a constant time-saver.
- **Optimization with AM–GM (advanced):** for positive a and b, **a + b ≥ 2√(ab)**, and they are **equal when a = b**. This is the quick way to find a **maximum or minimum** (→ Mock Q1-34: split time to maximise a product). It rests on the **Trivial Inequality** (any square is ≥ 0), since (√a − √b)² ≥ 0 rearranges to a + b ≥ 2√(ab).
- **Vertex/completing-the-square optimization:** a quadratic y = ax² + bx + c reaches its max or min at the **vertex**; complete the square to read it off. (This is the non-AM-GM way to do "biggest product" problems.)

> 💡 **Competition point:** If a problem asks for the **biggest product with a fixed sum**, the answer is usually when the two parts are **equal**. That is AM–GM in disguise.

---

## 📚 From the Books (extra tricks)

> 📖 *Source: AOPS Introduction to Algebra — SFFT Ch.11 §11.5; completing the square & quadratic formula Ch.13 §13.2–13.3; discriminant §13.5; Vieta's Ch.10 §10.4; rationalizing Ch.11 §11.4; nested radicals/self-similarity Ch.22 §22.2; telescoping Ch.21 §21.5. (Consecutive-integer sums is a number-theory topic, external to this book.)*

- **Consecutive-integer sums** *(number theory — see [[04_Divisors_Multiples_GCD_LCM]], not in Intro to Algebra)*: N can be written as a sum of 2 or more consecutive positive integers **unless N is a power of 2**. Count the **odd factors of N** (including 1) — call that k — and there are exactly **k − 1** ways.
  - Example: 1995 = 3 × 5 × 7 × 19 has 2⁴ = 16 odd factors → **15 ways** to write 1995 as a sum of consecutive positive integers.
- **Middle-term trick:** for consecutive integers, the sum = (**middle term**) × (**count of terms**) when the count is **odd**. When the count is **even**, use the **average of the two middle terms** instead.
  - Example: 6 consecutive integers add to 2019 → average = 2019 ÷ 6 = 336.5 → the terms sit around 336.5, so they run 334…339 (largest = **339**).

> 💡 **Competition point (SFFT — very famous, very useful):** an expression like **xy + ax + by** can be forced into a product by adding **ab** to both sides: **(x + b)(y + a) = (constant) + ab**. This turns a 2-variable equation into a **factor-pair search**.
> - Example: xy + 3x + 2y = 16 → add 6 to both sides → xy + 3x + 2y + 6 = 22 → **(x + 2)(y + 3) = 22**. List the factor pairs of 22 to find every integer (x, y).

- **Completing the square:** to turn x² + bx into a perfect square, add **(b/2)²**. This solves *any* quadratic, even ones that don't factor nicely.
  - Example: x² + 8x = 14 → add 16 to both sides → (x + 4)² = 30 → x = −4 ± √30.
- **The Quadratic Formula:** completing the square on ax² + bx + c = 0 in general gives **x = (−b ± √(b² − 4ac)) / (2a)**.
- **The Discriminant (b² − 4ac):** tells you the *type* of roots without solving — **positive** → 2 different real roots, **zero** → 1 repeated root, **negative** → no real roots (the two roots are a **complex-conjugate pair**, a ± b*i*).
- **Vieta's Formulas (full version):** for ax² + bx + c = 0 with roots r and s: **r + s = −b/a** and **r × s = c/a**. Read the sum/product straight off the coefficients — no need to solve at all.
  - **Combine with the identity** r² + s² = (r + s)² − 2rs to get the sum of squares of the roots straight from the coefficients — a very common contest step.
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
| Word problem | 5 steps: find → variable → equation → solve → check |
| Solution count | one / none (0=5) / infinite (0=0) |
| Two unknowns | elimination (cancel) or substitution |
| Three unknowns | subtract equations to reduce |
| Zero-product | product = 0 → a factor is 0 |
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
6. Solve (x − 3)(x + 7) = 0 using the zero-product property.
7. For x² − 5x + 6 = 0, use Vieta to find r + s and rs without solving.

<details>
<summary>Answers</summary>

1. Add: 2x = 26 → x = 13; then y = 20 − 13 = **7** (so x = 13, y = 7)
2. 53² − 47² = (53 + 47)(53 − 47) = 100 × 6 = **600**
3. 8m + 12 = **4(2m + 3)**
4. Let the numbers be a, b, c with a+b+c = 30. If a+b = 19 then c = 11; if a+c = 21 then b = 9; so a = 30 − 9 − 11 = 10 → **10, 9, 11**
5. Equal parts give the biggest product: 6 and 6 → **6 and 6** (product 36)
6. One factor must be 0 → x = **3 or −7**
7. r + s = −(−5)/1 = **5**, rs = 6/1 = **6** (indeed the roots are 2 and 3)

</details>

---
*Source map: `약점진단/12_방정식_식조작_인수분해.md` · Puzzle-style reasoning continues in [[13_Logic_and_Magic_Squares]]*
