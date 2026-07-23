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

In these puzzles some people **always tell the truth** and some **always lie**. You must figure out who is who, or what the real number is.

- **Assume & check:** suppose one person is telling the truth (or lying). Follow the statements. If you reach an **impossible situation (contradiction)**, your guess was wrong — so the opposite is true.
  - Example: A says "I am a liar." A truth-teller would never say that, and a liar cannot truthfully call himself a liar either → the statement itself is impossible, so watch for these traps.
- **Case table:** if there are only a few people, **list every true/false combination** in a table and test each row. Only the row with no contradiction survives.
- **Meta-statements ("at least N of us…", "exactly N are true"):** turn the count into cases. Try N = 1, then N = 2, and so on, and see which count actually works.
  - Example: "Exactly 1 of these 4 statements is true." Test which single statement being true keeps all the others false at the same time.
- **Work backwards from the result:** sometimes the puzzle gives you the ending and asks for the start. Reverse every step (see section 2).

> 💡 **Competition point:** For "**exactly K of these statements are true**", pick which K statements are the true ones, assume the rest are false, and check for a clash. Only one choice fits (→ Mock Q5-34 below: 5 statements, exactly 3 true).

---

## 2. Working Backwards

- **Idea:** when a problem describes steps that **end** at a known number, start from the **end** and **undo** each step to reach the start.
- **Undo the operation:** every action has an opposite. If someone "**took half and then put 1 back**", you reverse it by "**subtract 1, then double**".
  - Example: 6 sweets remain. Reverse "take half, return 1": (6 − 1) × 2 = 10 before that person.
- **Go person by person:** repeat the reverse step once for each person, in **reverse order**, until you reach the starting amount.

> 💡 **Competition point:** Doing these forwards needs guessing. Doing them **backwards is exact** — no trial and error (→ Mock Q4-22 below).

---

## 3. Magic Squares

A **magic square** is a grid where **every row, every column, and both diagonals add up to the same total** (the "magic sum").

- **3×3 total trick:** the three rows together use **all 9 numbers**, so the whole grid sum = 3 × (magic sum). Therefore **magic sum = total of all numbers ÷ 3**.
- **Centre trick:** in a 3×3 square, **centre = total of all numbers ÷ 9**. (For 1–9 the total is 45, so centre = 5, magic sum = 15.)
- **Why the centre is special:** the centre cell lies on the **middle row, the middle column, and both diagonals** — it is used in **4 different lines**. That makes it the strongest clue.
- **Partly filled squares:** let each empty cell be a **letter (variable)**. Write **one equation per line** that is complete, then solve.
  - Example: if a row is `a + 5 + 8` and you know the magic sum is 15, then a = 2 straight away.

> 💡 **Competition point:** Always find the **magic sum first** (from a full row/column), then fill cells one line at a time (→ Mock Q1-29 and Mock Q2-20 below).

---

## 4. Sudoku-style Grid Logic — *Sec 1*

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
| "Exactly K true" | choose which K, make rest false, test |
| Impossible statement | "I am a liar" can never be said truthfully |
| Working backwards | undo each step from the end, in reverse order |
| Undo "take half, put 1 back" | subtract 1, then double |
| 3×3 magic sum | total of all numbers ÷ 3 |
| 3×3 centre | total of all numbers ÷ 9 (centre used in 4 lines) |
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
5. Of 3 statements, exactly 1 is true: (S1) "S2 is true", (S2) "S1 is false", (S3) "S1 is true". Which one is the true statement?

<details>
<summary>Answers</summary>

1. If A tells the truth, then B is a liar — but B claims both are truth-tellers, which is false, so B is indeed lying. No contradiction. **B is the liar.**
2. Total 1+…+9 = 45 → magic sum = 45 ÷ 3 = **15**, centre = 45 ÷ 9 = **5**
3. 9 + □ + 4 = 21 → □ = **8**
4. Reverse "take half, put 1 back": (7 − 1) × 2 = **12**
5. Test S2 true: then S1 is false, so "S2 is true" is false — contradiction. Test S1 true: then S2 true too (2 true, not allowed). Test S3 true: S1 is true → but only 1 may be true, clash. So the working case is **S2** (S1 false, S3 false: S3 says "S1 is true" which is false ✓, S1 says "S2 is true" which is true — recount). Careful recount: exactly S2 true forces S1 false and S3 false → **S2 is the true one**.

</details>

---
*Source map: `약점진단/13_논리_마방진.md` · Puzzle-style reasoning continues in [[14_Sequences_and_Recurrence]]*
