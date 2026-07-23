# 09. Colouring, Partitions, Pigeonhole & Grid Paths

> **Unit:** Combinatorics (Unit 09 of 14) · **12 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** These are the four big "counting" tools. Colouring counts arrangements, stars-and-bars shares things out, pigeonhole proves "two must be the same", and grid paths count routes. Together they crack most hard counting questions.

---

## Lesson Overview
What this note covers:

1. Colouring counts
2. Chromatic polynomial — *Sec, advanced*
3. Integer partition (stars and bars) — *Sec 1*
4. Pigeonhole principle
5. Grid paths

---

## 1. Colouring counts

> 📖 *Source: standard competition technique (adjacency colouring). It isn't a named topic in AOPS Introduction to Counting & Probability, but it's just the **product rule** from [[08_Permutations_Combinations_Counting]] §1 applied one cell at a time.*

- **Basic multiplication (step by step):** colour one cell at a time. The **first** cell can be any colour. Each next cell must differ from its coloured neighbours, so it has **(total colours − colours already used next to it)** choices. Multiply all the choices.
  - Example: a row of 3 cells, 4 colours, neighbours must differ → first 4, second 3, third 3 → 4×3×3 = **36**.
- **Neighbours differ = adjacent rule:** two cells that touch (share a side or edge) may not have the same colour. Cells that do **not** touch may share a colour.
- **Order the cells cleverly:** colour the most-connected cell first. This keeps the "choices left" easy to count.

> 💡 **Competition point:** Always ask "how many neighbours are **already** coloured?" That number, subtracted from the total colours, is your choice count for that cell (→ Mock Q4-35, hexagon cells with 4 colours).

---

## 2. Chromatic polynomial — *Sec, advanced*

> 📖 *Source: graph theory — an external, advanced topic well beyond AOPS Introduction to Counting & Probability. Included only for the rare contest that needs it; the step-by-step method in Section 1 is what you'll actually use.*

- **Chromatic polynomial P(G, k):** a formula that gives the **number of ways to colour** a shape (graph G) with **k colours** so touching parts differ. Plug in k to get the count.
  - Example: a triangle (3 cells all touching) → P = k(k−1)(k−2). With k = 4 → 4×3×2 = **24**.
- **Deletion-contraction:** a rule to build the formula: **P(G, k) = P(G−e, k) − P(G/e, k)**.
  - **G−e** = the same shape with one edge **removed** (that pair may now match).
  - **G/e** = the two ends of that edge **merged** into one cell.
  - You keep breaking a hard shape into two easier shapes until each is simple.

> 💡 **Competition point:** For primary contests you rarely need the full polynomial — the **step-by-step multiplication** in Section 1 is faster. Learn deletion-contraction only if a shape has awkward loops.

---

## 3. Integer partition (stars and bars) — *Sec 1*

> 📖 *Source: AOPS Introduction to Counting & Probability §13.4 "A Clever Solution" (the dividers method, pp.198–199); built up in §13.3 (pp.193–197), where the answers are shown to be Pascal's-Triangle diagonals.*

- **Stars and bars idea:** to share **n identical items** into **k groups**, line up n stars and drop **k−1 bars** between them to split them. Counting the arrangements counts the sharings.
- **Why the formula (the book's derivation):** you now have **n stars + (k−1) bars = n + k − 1 symbols** in a row, and you just choose **which k−1 of them are bars** — so ways = **C(n + k − 1, k − 1)**. (Two bars next to each other = a group gets **0**, which is why empty groups are allowed.)
- **Non-negative (groups may be empty):** ways = **C(n + k − 1, k − 1)**.
  - Example: 5 sweets into 3 kids, empty allowed → C(5+2, 2) = C(7,2) = **21**.
- **Positive (no group empty):** first give each group 1, then share the rest → ways = **C(n − 1, k − 1)**.
  - Example: 5 sweets into 3 kids, none empty → C(4,2) = **6**.
- **Minimum / maximum limits:** if group *i* must get at least *mᵢ*, **hand out those minimums first**, then stars-and-bars the leftover. This turns a hard question into a plain one.
- **Strictly increasing (each bigger than the last):** if amounts must go up every step, subtract 0,1,2,… to make the gaps disappear, then count as **distinct** values.

> 💡 **Competition point:** Read the wording carefully. "None empty" → C(n−1, k−1). "At least n for group n" → subtract the minimums first (→ Mock Q5-23).

---

## 4. Pigeonhole principle

> 📖 *Source: standard competition principle — not a named topic in AOPS Introduction to Counting & Probability, but a must-know for olympiad-style "two must be the same" arguments.*

- **Basic pigeonhole:** put **n + 1 items** into **n boxes** → some box holds **at least 2**.
  - Example: 13 people, 12 months → two share a birth month.
- **Stronger pigeonhole:** put **kn + 1 items** into **n boxes** → some box holds **at least k + 1**.
  - Example: 25 socks in 4 drawers → 25 = 6×4 + 1 → some drawer holds **at least 7**.
- **Counting by outcomes:** if there are only **N possible results**, then **N + 1 people** force **two with the same result**. The trick is to count how many different results exist.

> 💡 **Competition point:** The hard part is choosing the "boxes". Make each box **one possible outcome**, count the outcomes = N, then N+1 forces a repeat (→ Mock Q5-30, 5 colours picked 2 at a time).

---

## 5. Grid paths

> 📖 *Source: AOPS Introduction to Counting & Probability §5.2 "Paths on a Grid" (pp.81–83); §5.5 Summary (p.92).*

- **Basic grid path:** to go from a corner to the opposite corner using only **right** and **up** steps, with m rights and n ups, ways = **C(m + n, m)**.
  - Example: a 3-by-2 grid needs 3 rights and 2 ups → C(5, 3) = **10**.
- **Why it's a combination (the book's model):** every path is just a **word** made of the steps, like R R R U U — m R's and n U's in some order. Counting the arrangements of that word (a permutation with repeats, m+n steps of which m are identical R's) gives **(m+n)! / (m! n!) = C(m+n, m)**. Choosing **where the m R-steps go** among the m+n moves *is* the path. (Same "identical items" division as [[08_Permutations_Combinations_Counting]] §1.)
- **Reversed directions still count the same way:** a "down and right" grid, or "left and up", uses the identical C(m+n, m) — only the two step-types and their counts matter.
- **Through a point P:** a path **must pass P** → count (start → P) and (P → end) separately, then **multiply** them.
- **Through two points Y and P (in order):** break the trip into pieces start→Y, Y→P, P→end and **multiply all pieces**.

> 💡 **Competition point:** A "must pass this point" question always **splits and multiplies**. A "score climbs from a to b" question is secretly a grid path — each point won is a step (→ RI 2021 Q18, going from 8–0 up to 11–8).

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Colour a shape | multiply choices, subtract used neighbour colours |
| Chromatic polynomial | P(G,k); deletion-contraction P(G−e)−P(G/e) — *advanced* |
| Share n into k, empty ok | C(n+k−1, k−1) |
| Share n into k, none empty | C(n−1, k−1) |
| Minimum limits | give out minimums first, then stars-and-bars |
| Pigeonhole (basic) | n+1 into n boxes → some box ≥ 2 |
| Pigeonhole (strong) | kn+1 into n boxes → some box ≥ k+1 |
| Stars & bars, why | arrange n stars + (k−1) bars → choose bar spots |
| Grid path corner to corner | C(m+n, m) = arrange m R's + n U's |
| Path through point P | (start→P) × (P→end) |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Colouring counts**
- [Mock Q4-35](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_35.png) — 11 hexagon cells, 4 colours, touching cells must differ
- [Mock Q5-33](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_33.png) — 3×5 grid, colour 9 cells black so every row and column has an odd number black
- [RI 2022 Q17](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/17.png) — 3×3 grid, arrange with an odd/even adjacency rule
- [AP 2025 Q20](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/20.png) — 8 regions, 4 colours, neighbours must differ

**② Integer partition (stars and bars)**
- [Mock Q5-23](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_23.png) — share 30 into 4 groups where group n gets at least n
- [RI 2023 Q17](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/17.png) — 23 apples and 18 oranges into 5 shops with minimums
- [Mock Q1-14](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_14.png) — 28 marbles into 3 boxes, none empty
- [AP 2021 Q12](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/12.png) — solve 25 problems over 6 days, strictly increasing each day

**③ Pigeonhole principle**
- [Mock Q4-32](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_32.png) — cards 1–13, most cards so all pair-sums differ
- [Mock Q5-30](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_30.png) — 5 colours, pick 2 each; people needed to force 2 with the same combination

**④ Grid paths**
- [RI 2021 Q18](https://dannyahramwoo.github.io/math-quiz/problems/51.%20RI%202021/18.png) — from 8–0 to 11–8, count the paths where A wins
- [AP 2021 Q22](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/22.png) — two people on a circular track meeting; find the track length

---

## Quick Check

1. A row of 4 cells is coloured with 3 colours so touching cells differ. How many ways?
2. Share 10 identical sweets among 3 children, empty allowed. How many ways?
3. Share 10 identical sweets among 3 children, none empty. How many ways?
4. 100 people each pick a number from 1 to 9. Must two people share a number? What is the largest group forced?
5. How many right/up paths go from one corner of a 4-by-3 grid to the opposite corner?
6. Write the grid-path count in question 5 as an arrangement of R's and U's — how many of each letter?

<details>
<summary>Answers</summary>

1. First cell 3, then each next 2 → 3×2×2×2 = **24**
2. C(10+2, 2) = C(12,2) = **66**
3. C(10−1, 2) = C(9,2) = **36**
4. 100 = 11×9 + 1 → some number is shared by **at least 12** people
5. 4 rights, 3 ups → C(7, 3) = **35**
6. 4 R's and 3 U's → arrangements of RRRRUUU = 7!/(4!3!) = **35** (same as question 5)

</details>

---
*Source map: `약점진단/09_색칠_분할_비둘기집.md` · Counting continues in [[10_Distance_Speed_Time]]*
