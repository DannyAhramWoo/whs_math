# 14. Sequences & Recurrence

> **Unit:** Patterns & Sequences (Unit 14 of 14) · **5 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Many hard competition problems hide a **pattern**. If you can spot the rule of a sequence, or write a **recurrence** (each term from the ones before), a scary-looking problem turns into a short, safe calculation.

---

## Lesson Overview
What this note covers:

1. Arithmetic Sequences and their Sum
2. Geometric Sequences and their Sum — *Sec 1*
3. Special Number Patterns (triangular, square sums)
4. Recurrence and General Term
5. Fibonacci, Stairs & Tiling

---

## 1. Arithmetic Sequences and their Sum

- **Arithmetic sequence:** a list where you **add the same number each time**. That fixed jump is the **common difference (d)**.
  - Example: 3, 7, 11, 15, ... → d = 4
- **nth term:** the number in position n is **a + (n−1)d** (start value a, then take (n−1) jumps).
  - Example: 3, 7, 11, ... → 10th term = 3 + 9×4 = 39
- **Sum of an arithmetic sequence:** **S_n = n(a + l)/2** (n terms, first a, last l). Same as **S_n = n(2a + (n−1)d)/2**.
  - Trick to remember: pair the first and last, second and second-last... each pair has the same total. There are n/2 pairs, each equal to (a + l).
  - Example: 1 + 2 + ... + 100 = 100×(1+100)/2 = **5050**

> 💡 **Competition point:** Odd numbers 1, 3, 5, ... are an arithmetic sequence with d = 2. Their running sums are **perfect squares**: 1 = 1², 1+3 = 2², 1+3+5 = 3². The sum of the first n odd numbers = **n²**.

---

## 2. Geometric Sequences and their Sum — *Sec 1*

- **Geometric sequence:** a list where you **multiply by the same number each time**. That fixed multiplier is the **common ratio (r)**.
  - Example: 2, 6, 18, 54, ... → r = 3
- **nth term:** **a × r^(n−1)** (start value a, then multiply by r a total of (n−1) times).
- **Sum of a geometric sequence:** **S_n = a(1 − rⁿ)/(1 − r)** (when r ≠ 1).
  - Example: 1 + 2 + 4 + 8 + 16 = 1×(1 − 2⁵)/(1 − 2) = (1 − 32)/(−1) = **31**
- **Infinite geometric sum (advanced):** if the ratio is a fraction between −1 and 1, the whole never-ending sum settles on **S = a/(1 − r)**.
  - Example: 1/2 + 1/4 + 1/8 + ... = (1/2)/(1 − 1/2) = **1**

> 💡 **Competition point:** For a "sum that goes on forever" problem, check the ratio first. If it is a small fraction, use **S = a/(1 − r)** — you do not need to add infinitely many terms.

---

## 3. Special Number Patterns (triangular, square sums)

- **Triangular numbers:** dots that build a triangle: 1, 3, 6, 10, 15, ... The nth one is **T_n = n(n+1)/2**.
  - This is just the arithmetic sum 1 + 2 + ... + n.
- **Sum of squares:** **1² + 2² + ... + n² = n(n+1)(2n+1)/6**.
  - Example: 1² + 2² + 3² + 4² = 4×5×9/6 = **30**
- **Odd-number groups:** a common competition setup groups odd numbers like (1) (3 5) (7 9 11) (13 15 17 19)... Row n has **n numbers**, so after n rows you have used **1 + 2 + ... + n = T_n** odd numbers in total.

> 💡 **Competition point:** To find *which group* a number lands in, count **how many numbers came before**. Use triangular numbers T_n = n(n+1)/2 to jump ahead instead of listing every term (→ Mock Q1-22, AP 2025 Q23 below).

---

## 4. Recurrence and General Term

- **Recurrence:** a rule that builds **each term from the earlier terms**. Example: "double the last term, then add 1."
- **General term:** a single formula that gives term n **directly**, without walking through all the earlier ones.
- **How to attack a mystery sequence:**
  1. Write out the **first 5 terms** by hand.
  2. Look at the **differences** (or the **ratios**) between neighbours.
  3. Guess the rule, then **test it** on the next known term.
  - Example: 4, 9, 24, 69, 204, ... Check: 9 = 4×3 − 3, 24 = 9×3 − 3, 69 = 24×3 − 3 → rule is **×3 − 3**. Next: 204×3 − 3 = 609. ✓

> 💡 **Competition point:** If plain differences do not form a pattern, try **"multiply by something, then add/subtract something"** (the ×k + c type). Testing on 2–3 known terms confirms it fast (→ RI 2024 Q02 below).

---

## 5. Fibonacci, Stairs & Tiling

- **Fibonacci sequence:** each term is the **sum of the two before it**: **f(n) = f(n−1) + f(n−2)**.
  - Start 1, 1 → 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
- **Stairs / tiling follow Fibonacci:** many "how many ways" counting problems land on the exact same rule.
  - **Climbing stairs** (1 or 2 steps at a time) to reach step n = f(n).
  - **Tiling a 2×n board** with 2×1 dominoes: the last column is either one **vertical** tile (leaving 2×(n−1)) or two **horizontal** tiles (leaving 2×(n−2)). So **ways(n) = ways(n−1) + ways(n−2)** — Fibonacci again!
  - Ways for 2×n: n=1 → 1, 2 → 2, 3 → 3, 4 → 5, 5 → 8, 6 → 13, 7 → 21, 8 → **34**.

> 💡 **Competition point:** When a counting problem says "in one step you can do this **or** that," split by the **last move**. The two cases almost always add up to a **Fibonacci-style recurrence** (→ Mock Q1-25 below).

---

## 📚 From the Books (extra tricks)

- **Difference tables:** if the first differences are not constant, take the differences **of the differences** (second differences), and repeat. The number of rounds needed to get a constant row tells you the sequence follows a polynomial of that degree.
  - Example: 5, 11, 19, 29, ... → 1st differences 6, 8, 10 (not constant) → 2nd differences 2, 2, 2 (constant!) → this is a **"degree 2"** pattern, so you can build a formula for the nth term.
- **Repeating-cycle position:** for a periodic pattern (repeating decimal digits, a repeating letter/colour sequence), find the kth term using **k mod (period length)** — but a remainder of 0 usually means "the **last** term of the cycle," not term 0.
  - Example: 100th digit of 1/7 = 0.142857142857... (period 6): 100 = 16×6 + 4 → matches the 4th digit of "142857," which is **8**.
- **Middle-term trick (odd count):** for an arithmetic series with an **odd** number of terms, sum = (number of terms) × (the middle term). Often faster than the full sum formula, especially when the problem gives scattered terms.
  - Example: a₄ + a₇ + a₁₀ = 17, and a₇ is the middle of that trio → 3×a₇ = 17 directly, no need to find the first term and common difference.
- **Geometric mean between neighbours:** in a geometric sequence, any term equals **√(product of its two neighbours)** — the geometric-sequence version of "a term = average of its two neighbours" in arithmetic sequences.
  - Example: 3, 3√3, 9, 9√3, 27 → middle term 9 = √(3×27).
- **Index-sum shortcut:** if m + n = p + q, then **aₘ + aₙ = aₚ + aq** (arithmetic) or **aₘ × aₙ = aₚ × aq** (geometric). If m + n = 2t, then aₘ + aₙ = 2aₜ. This skips solving for a and d entirely.
  - Example: a₁ + a₉ = 10 → since 1+9 = 2×5, a₁+a₉ = 2a₅ → a₅ = **5** directly.
- **Common terms of two arithmetic sequences:** if two arithmetic sequences share infinitely many terms, those shared terms form a **new arithmetic sequence**, with common difference = **LCM** of the two original common differences.

> 💡 **Competition point:** Before grinding through a sum or an unknown term, check if the index numbers add up nicely (m+n = p+q) or if the count of terms is odd — these shortcuts skip solving for a and d altogether.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Arithmetic nth term | a + (n−1)d |
| Arithmetic sum | n(a + l)/2 |
| Sum of first n odd numbers | n² (a perfect square) |
| Geometric nth term | a × r^(n−1) |
| Geometric sum | a(1 − rⁿ)/(1 − r) |
| Infinite geometric sum | a/(1 − r), needs \|r\| < 1 |
| Triangular number | T_n = n(n+1)/2 |
| Sum of squares | n(n+1)(2n+1)/6 |
| Fibonacci | f(n) = f(n−1) + f(n−2) |
| Stairs / 2×n tiling | Fibonacci pattern |
| Mystery sequence | list 5 terms, check differences/ratios, test the rule |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Sequence rules (arithmetic / geometric / triangular)**
- [Mock Q1-22](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_22.png) — odd numbers in growing groups; find the size of the group holding 2023 → *use triangular numbers*
- [AP 2025 Q23](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/23.png) — odd-number table with growing rows; the number sitting just below 2025

**② Recurrence / general term**
- [Mock Q1-25](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_25.png) — cover a 2×8 board with 2×1 tiles; count the number of ways → *Fibonacci*
- [RI 2024 Q02](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/02.png) — 4, 9, 24, 69, 204, 609, ...; find the sum of the next two terms
- [RI 2022 Q05](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/05.png) — value of the infinite sum of Fibonacci ÷ 5ⁿ

---

## Quick Check

1. What is 5 + 8 + 11 + ... + 50? (arithmetic, d = 3)
2. What is the sum 1 + 3 + 5 + ... + 39?
3. Find the 6th triangular number.
4. A sequence goes 2, 5, 14, 41, ... Each term is "×3 − 1" of the one before. What is the 5th term?
5. In how many ways can you climb a staircase of 6 steps, taking 1 or 2 steps at a time?

<details>
<summary>Answers</summary>

1. Terms: 5, 8, ..., 50 → count n = (50−5)/3 + 1 = 16. Sum = 16×(5+50)/2 = **440**
2. These are the first 20 odd numbers (39 is the 20th) → 20² = **400**
3. T₆ = 6×7/2 = **21**
4. 41×3 − 1 = **122**
5. Fibonacci: f(6) with f(1)=1, f(2)=2 → 1, 2, 3, 5, 8, **13**

</details>

---
*Source map: `약점진단/14_수열_점화식.md` · Patterns connect back to scaling ideas in [[01_Ratio_and_Proportion]]*
