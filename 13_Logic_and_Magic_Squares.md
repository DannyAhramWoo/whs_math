# 13. Logic, Magic Squares & Truth Puzzles

> **Unit:** Logic & Puzzles (Unit 13 of 14) · **7 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** These problems have no formula. You win by **careful reasoning**: assume, check, and cross out. Learn the tricks here and "hard-looking" puzzle questions become quick and safe marks.

---

## Lesson Overview
What this note covers:

1. Truth-telling Puzzles (Knights & Knaves)
2. Working Backwards
3. Magic Squares
4. Sudoku-style Grid Logic

---

## 1. Truth-telling Puzzles (Knights & Knaves)

> 📖 *Source: AMC 8 Preparation Vol.1 Ch.3 "Logical Reasoning" — statements & negation, contradictory/agreeing statements, and the "exactly K statements are true" method.*

In these puzzles some people **always tell the truth** and some **always lie**. You must figure out who is who, or what the real number is.

- **A statement is either true or false** (never both). Commands, questions, and opinions aren't statements. To **negate** "all are red" you say "at least one is not red" (not "none are red").
- **Assume & check:** suppose one person is telling the truth (or lying). Follow the statements. If you reach an **impossible situation (contradiction)**, your guess was wrong — so the opposite is true.
  - Example: A says "I am a liar." A truth-teller would never say that, and a liar cannot truthfully call himself a liar either → the statement itself is impossible, so watch for these traps.
- **Shortcut — find two statements that contradict each other.** If statement P and statement Q **can't both be true and can't both be false**, then **exactly one of them is the true one**. In a "only one is true" puzzle, every *other* statement is then automatically false — no need to test all cases.
- **Shortcut — statements that agree.** If two statements are true together or false together, and only one may be true, then **neither** can be the single true one — cross both out.
- **Contrapositive (equivalent restatement):** "if P then Q" is exactly equivalent to "if **not Q** then **not P**". (Its *converse* "if Q then P" is **not** equivalent — a classic trap.)
- **Case table:** if there are only a few people, **list every true/false combination** in a table and test each row. Only the row with no contradiction survives.
- **Meta-statements ("at least N of us…", "exactly N are true"):** turn the count into cases. Try N = 1, then N = 2, and so on, and see which count actually works.

> 💡 **Competition point:** For "**exactly K of these statements are true**", first hunt for a **contradicting pair** (that pins one true statement fast); otherwise pick which K statements are the true ones, assume the rest are false, and check for a clash (→ Mock Q5-34 below: 5 statements, exactly 3 true).

---

## 2. Working Backwards

> 📖 *Source: AOPS Prealgebra §15.4 "Work Backwards" (one of the four problem-solving strategies: Find a Pattern, Make a List, Draw a Picture, Work Backwards).*

- **Idea:** when a problem describes steps that **end** at a known number, start from the **end** and **undo** each step to reach the start.
- **Undo the operation:** every action has an opposite. If someone "**took half and then put 1 back**", you reverse it by "**subtract 1, then double**".
  - Example: 6 sweets remain. Reverse "take half, return 1": (6 − 1) × 2 = 10 before that person.
- **The "undo table" method:** write two columns — each **action** and its **undoing action** (+3 ↔ −3, ×2 ↔ ÷2). Then apply the undo actions from the **last step to the first**. Keeping the table straight stops sign slips.
- **Go person by person:** repeat the reverse step once for each person, in **reverse order**, until you reach the starting amount.

> 💡 **Competition point:** Working backwards is exact (no guessing) when you **know the ending and must find the start**. But it isn't always best — sometimes **setting up an equation** (let x = the start, write the forward process, solve) is cleaner. Try both if one gets messy (→ Mock Q4-22 below).

---

## 3. Magic Squares

> 📖 *Source: standard competition topic (not in the AOPS/AMC reference books). The magic-sum arithmetic below is self-contained.*

A **magic square** is a grid where **every row, every column, and both diagonals add up to the same total** (the "magic sum").

- **3×3 total trick:** the three rows together use **all 9 numbers**, so the whole grid sum = 3 × (magic sum). Therefore **magic sum = total of all numbers ÷ 3**.
- **Centre trick:** in a 3×3 square, **centre = total of all numbers ÷ 9**. (For 1–9 the total is 45, so centre = 5, magic sum = 15.)
- **Why the centre is special:** the centre cell lies on the **middle row, the middle column, and both diagonals** — it is used in **4 different lines**. That makes it the strongest clue.
- **Partly filled squares:** let each empty cell be a **letter (variable)**. Write **one equation per line** that is complete, then solve.
  - Example: if a row is `a + 5 + 8` and you know the magic sum is 15, then a = 2 straight away.
- **Building a 3×3 from scratch (the staircase / Siamese method for odd squares):** put **1** in the top-middle cell. Each next number goes **up one and right one**; if that lands off the grid, wrap around to the other side; if the cell is already filled, drop **down one** instead. This fills a 3×3 with 1–9 as a magic square automatically.

> 💡 **Competition point:** Always find the **magic sum first** (from a full row/column), then fill cells one line at a time (→ Mock Q1-29 and Mock Q2-20 below).

---

## 4. Sudoku-style Grid Logic — *Sec 1*

> 📖 *Source: standard competition topic (grid/constraint logic — not in the reference books).*

You must place numbers in a grid so that each row/column/region follows a rule. No arithmetic formula — only **logic**.

- **Elimination:** for each cell, **cross out** every value that is not allowed. Whatever is left must go there.
- **Uniqueness (last spot):** if a value X can only fit in **one place** in a row (all other cells are blocked), then X **must** go there.
- **Branch on cases:** if you are stuck, **assume** a cell has a value, follow the rules, and if you hit a contradiction, that value is wrong — try the next.

> 💡 **Competition point:** When regions must have **equal sums**, first find that shared sum (total of all numbers ÷ number of regions), then use it to pin down the "?" cell (→ RI 2024 Q01 below).

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Truth puzzle | assume → check → contradiction means flip it |
| Contradicting pair | exactly one of the two is true → others false |
| "Exactly K true" | find a contradicting pair first, else test cases |
| Contrapositive | "if P then Q" ≡ "if not Q then not P" (converse ≠) |
| Impossible statement | "I am a liar" can never be said truthfully |
| Working backwards | undo table; apply undos last-step-first |
| Undo "take half, put 1 back" | subtract 1, then double |
| 3×3 magic sum | total of all numbers ÷ 3 |
| 3×3 centre | total of all numbers ÷ 9 (centre used in 4 lines) |
| Build a 3×3 (odd) | staircase: 1 top-middle, up-right, wrap or drop down |
| Partly-filled square | one equation per complete line |
| Grid logic | eliminate, find the only spot, branch if stuck |
| Equal-region sum | total ÷ number of regions |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Truth-telling puzzles**
- [NM 2008 Q12](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/12.png) — Andy, Ben & Calvin in a queue; work out the total number of people
- [Mock Q5-21](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_21.png) — 4 statements, exactly 1 is true; find the number of pictures
- [Mock Q5-34](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_34.png) — 5 statements, exactly 3 are true; find the 3-digit number
- [Mock Q4-22](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_22.png) — 6 people each take half plus 1 back; work backwards on the sweets

**② Magic squares**
- [Mock Q1-29](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_29.png) — 3×3 magic square; find x
- [Mock Q2-20](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_20.png) — partly filled 3×3 square; find the common sum

**③ Sudoku-style grid logic**
- [RI 2024 Q01](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/01.png) — place 1–5 in a 5×5 grid with equal region sums; find the "?"

---

## Quick Check

1. A says "B is a liar." B says "A and I are both truth-tellers." One always lies, one always tells the truth. Who is the liar?
2. In a 3×3 magic square using 1–9, what is the magic sum and what number is in the centre?
3. A magic square has magic sum 21. One full row is `9 + □ + 4`. What is the missing number?
4. A jar loses "half of what is inside, then 1 more is put back" each round. After a round, 7 are inside. How many were there before?
5. Of 3 statements, exactly 1 is true: (S1) "all three are false", (S2) "exactly one is true", (S3) "S1 is true". Which statement is the true one?
6. "If it rains, the match is cancelled." Write the equivalent contrapositive.

<details>
<summary>Answers</summary>

1. If A tells the truth, then B is a liar — but B claims both are truth-tellers, which is false, so B is indeed lying. No contradiction. **B is the liar.**
2. Total 1+…+9 = 45 → magic sum = 45 ÷ 3 = **15**, centre = 45 ÷ 9 = **5**
3. 9 + □ + 4 = 21 → □ = **8**
4. Reverse "take half, put 1 back": (7 − 1) × 2 = **12**
5. If S1 ("all three are false") were true, it would call itself false — impossible, so **S1 is false**. Then S3 ("S1 is true") is also **false**. That leaves S2 ("exactly one is true"), and with S1 and S3 both false, S2 being the single true one is consistent → **S2 is the true statement**.
6. Contrapositive: **"If the match is not cancelled, then it did not rain."** (Equivalent to the original.)

</details>

---
*Source map: `약점진단/13_논리_마방진.md` · Puzzle-style reasoning continues in [[14_Sequences_and_Recurrence]]*
