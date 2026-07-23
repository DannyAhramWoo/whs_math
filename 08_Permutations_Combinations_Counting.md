# 08. Permutations, Combinations & Counting

> **Unit:** Counting & Combinatorics (Unit 08 of 14) · **12 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Counting problems are everywhere. If you know when order matters (permutation) and when it does not (combination), you can turn a scary "how many ways" question into one clean multiplication.

---

## Lesson Overview
What this note covers:

1. Permutations (order matters)
2. Combinations (order does not matter) — *Sec 1*
3. Geometric Counting (points, lines, triangles)
4. Burnside's Lemma (counting with symmetry) — *Sec, advanced*

---

## 1. Permutations — order matters

- **Permutation:** an **ordered** arrangement. "ABC" and "CBA" count as **different**.
- **P(n, r) formula:** the number of ways to line up **r** items chosen from **n**.
  - **P(n, r) = n! / (n−r)! = n(n−1)(n−2)…** (r factors, counting down).
  - Example: seat 3 of 5 people in a row → P(5,3) = 5×4×3 = **60**.
- **With repeats (repeated letters):** if some items are the same, divide by the factorial of each repeat.
  - **Arrangements = n! / (a! b! c! …)**
  - Example: the word "hello" has 5 letters with **two l's** → 5! / 2! = 120 / 2 = **60**.
- **Circular arrangement:** n people around a **circle** = **(n − 1)!**. Fix one person; only the others' order matters (rotations are the same).
  - Example: 5 people at a round table → (5−1)! = 4! = **24**.
- **"Must be together" (glue rule):** treat the group as **one block**, arrange, then multiply by the ways **inside** the block.
- **"Not together":** first arrange the others, then **place the special ones in the gaps** between them.

> 💡 **Competition point:** A **derangement (mis-arrangement)** is an arrangement where **nothing** sits in its own place. Small ones are worth memorising: 3 items → 2, 4 items → 9, 5 items → 44 (→ Mock Q4-27, AP 2021 Q23 below).

---

## 2. Combinations — order does not matter — *Sec 1*

- **Combination:** a **choice** where order does **not** matter. Picking {A, B, C} is the same as {C, B, A}.
- **C(n, r) formula:** the number of ways to **choose r** from **n**.
  - **C(n, r) = n! / (r! (n−r)!)**
  - Example: choose 2 from 5 → C(5,2) = 10.
- **Symmetry:** C(n, r) = C(n, n−r). Choosing what to keep = choosing what to leave out.
- **Pascal's identity:** **C(n, r) = C(n−1, r−1) + C(n−1, r)**. Each entry in Pascal's triangle is the sum of the two above it.
- **Subtract-the-bad:** count **everything**, then take away the cases that break the rule.
  - Example: triangles from points = C(all, 3) − (sets of 3 that lie **on one line**).
- **Conditional ("A and B both hold"):** count only the arrangements that satisfy **every** condition at once, often by combining a choice with a rule.

> 💡 **Competition point:** "Strictly decreasing digits" like 6 > 4 > 1 means **once you choose the digits, only one order works** — so it becomes a pure **combination**, not a permutation (→ RI 2021 Q09 below).

---

## 3. Geometric Counting — points, lines, triangles

- **Triangles from N points:** choose any 3 points → C(N, 3). But 3 points **on a straight line** make **no** triangle.
  - **Number of triangles = C(N, 3) − (number of collinear 3-point sets).**
- **Finding collinear sets on a grid/array:** scan every **row**, **column**, and **diagonal**; for a line with k points count C(k, 3) bad sets.
- **Segments/lines through points:** count carefully by direction so you do **not** count the same line twice.

> 💡 **Competition point:** In a triangular or grid array, the sneaky part is the **diagonals** — students remember rows and columns but forget the slanted lines (→ RI 2024 Q13 below).

---

## 4. Burnside's Lemma — counting with symmetry — *Sec, advanced*

- **The problem it solves:** when rotations or flips make some arrangements **look the same**, plain counting **over-counts**.
- **Burnside's lemma:** number of **truly different** arrangements = the **average number of arrangements that stay unchanged** across all the symmetries.
  - **Distinct = (1 / |G|) × (sum of fixed arrangements for each symmetry)**, where **|G|** is how many symmetries there are.
  - Example: 4 beads in a circle with only rotations → **|G| = 4** (turn by 0, 1, 2, 3 places); average the beads that "come back to themselves" for each turn.

> 💡 **Competition point:** For a rectangle card the symmetry group is small (identity, half-turn, two flips). List each symmetry, count what it fixes, then average (→ AP 2025 Q26 below).

---

## 📚 From the Books (extra tricks)

- **Sum Rule vs Product Rule:** if a job can be done through separate alternatives joined by **"OR"**, **add** the ways. If a job needs several steps joined by **"AND"**, **multiply** the ways.
  - Example: 1 book from 5 paperbacks OR 3 hardcovers → 5+3 = **8** (sum rule). An outfit from 5 shirts AND 4 skirts AND 3 shoes → 5×4×3 = **60** (product rule).
- **Multinomial coefficient:** splitting **n distinct** objects into groups of sizes n₁, n₂, … nᵣ, where the groups are **distinguishable** (e.g. named people) = **n! / (n₁! n₂! … nᵣ!)**.
  - Example: give 6 different books to Alex, Bob, Catherine, 2 each → 6!/(2!2!2!) = **90**.
- **Stars and Bars:** placing **n identical** objects into **k distinguishable** bins = **C(n+k−1, k−1)**. If every bin needs **at least one**: **C(n−1, k−1)**.
  - Example: 3 friends share 6 identical pencils, everyone gets ≥1 → C(5,2) = **10**. If 0 is allowed → C(8,2) = **28**.
- **Digit-pattern shortcuts:** n-digit numbers with strictly **increasing** digits = **C(9, n)**. Strictly **decreasing** digits (a leading digit can pair with a trailing 0) = **C(10, n)**. n-digit **palindromes** = **9 × 10^(⌈n/2⌉ − 1)**.
- **Grid path counting:** moving only right/up on a grid, the paths from corner to corner = **C(m+n, n)**, where m and n are the steps in each direction. Counting **rectangles** in a grid of m vertical and n horizontal lines = **C(m,2) × C(n,2)**.
- **Basic probability:** **P(event) = (ways it happens) ÷ (ways total)**, when every outcome is equally likely. Don't mix ordered and unordered counting — count both the successes **and** the total the **same way**, never one ordered and the other not.
- **Handshake / counting-pairs formula:** pairs among n items (handshakes, matches, diagonals) = **n(n−1)/2** — count the ordered pairs n(n−1), then halve since each pair got counted twice.
- **Pascal's Triangle ↔ combinations:** building the triangle (each entry = sum of the two above) gives exactly **C(n, r)** at row n, position r. This can be proven with a "committee" argument: an r-person team either includes one fixed person or it doesn't.
- **Hockey Stick Identity:** C(r,r) + C(r+1,r) + … + C(n,r) = **C(n+1, r+1)** — on Pascal's Triangle these terms trace an L-shape, hence the name.
- **Binomial Theorem:** (x+y)ⁿ = C(n,0)xⁿ + C(n,1)xⁿ⁻¹y + … + C(n,n)yⁿ — each coefficient is a combination number straight from row n of Pascal's Triangle.
  - Example: (x+y)³ = x³ + 3x²y + 3xy² + y³ (coefficients 1, 3, 3, 1).

> 💡 **Competition point:** Stars and Bars and the Hockey Stick Identity look unrelated to permutations at first, but both come from the same C(n, r) toolbox — spotting "identical objects, distinguishable bins" or a Pascal's-Triangle L-shape is often the fastest way in.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Order matters | use permutation P(n, r) |
| Order does not | use combination C(n, r) |
| P(n, r) | n! / (n−r)! |
| C(n, r) | n! / (r!(n−r)!) |
| Repeated items | divide by a! b! c! |
| Circle of n | (n−1)! |
| Must be together | glue into one block |
| Not together | place in the gaps |
| Derangements | 3→2, 4→9, 5→44 |
| Pascal's identity | C(n,r) = C(n−1,r−1) + C(n−1,r) |
| Triangles from points | C(N,3) − collinear 3-sets |
| Symmetry over-counts | Burnside: average the fixed cases |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Permutation**
- [NM 2008 Q09](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/09.png) — enter and leave a room through 8 doors; count the ordered ways
- [Mock Q4-27](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_27.png) — mis-arrangements (derangements) of the word "hello"
- [Mock Q5-16](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_16.png) — 6 people in a row with Jack, Tony, Andy all next to each other → *glue rule*
- [AP 2021 Q06](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/06.png) — place 5 stones on a board, one per row and one per column
- [AP 2021 Q23](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/23.png) — derangements of the digits 2, 3, 4, 5

**② Combination**
- [RI 2021 Q09](https://dannyahramwoo.github.io/math-quiz/problems/51.%20RI%202021/09.png) — 3-digit even numbers with strictly decreasing digits
- [RI 2024 Q06](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/06.png) — 12 equally spaced points on a circle; triangles up to rotation and reflection
- [RI 2023 Q16](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/16.png) — scores you **cannot** make from 3-, 4- and 6-point problems
- [AP 2025 Q22](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/22.png) — integer pairs meeting the ≥25% and 25–28 conditions at once
- [AP 2025 Q25](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/25.png) — 4-digit numbers with exactly one repeated digit

**③ Geometric counting (3 points / collinear)**
- [RI 2024 Q13](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/13.png) — triangular array of points; count the segments passing through 3 points

**④ Burnside's lemma**
- [AP 2025 Q26](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/26.png) — 2×3 black/white cards; count the symmetry classes → *Sec, advanced*

---

## Quick Check

1. In how many ways can 4 different books be lined up on a shelf?
2. How many different arrangements are there of the letters in "BANANA"?
3. From 7 students, how many ways to choose a team of 3?
4. 6 friends sit around a round table. How many seatings are different?
5. There are 10 points and no 3 are on one line. How many triangles can be drawn?

<details>
<summary>Answers</summary>

1. 4! = **24**
2. "BANANA" has 3 A's and 2 N's → 6! / (3!·2!) = 720 / 12 = **60**
3. C(7,3) = 7!/(3!·4!) = **35**
4. (6−1)! = 5! = **120**
5. C(10,3) = **120** (no collinear sets to subtract)

</details>

---
*Source map: `약점진단/08_순열_조합_세기.md` · Counting continues in [[09_Colouring_Partitions_Pigeonhole]]*
