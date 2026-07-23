# 16. Probability & Expected Value

> **Unit:** Probability (Unit 16 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** Probability questions ("what is the chance that...") are common in exams and connect directly to the counting tools in [[08_Permutations_Combinations_Counting]]. This unit turns those counting skills into probability answers.

---

## Lesson Overview
What this note covers:

1. Basic Probability
2. Complement and "At Least One"
3. Independent vs Dependent Events
4. Addition Rule (Overlapping Events)
5. Geometric Probability
6. Expected Value

---

## 1. Basic Probability

- **Probability formula:** P(event) = (number of ways it happens) ÷ (number of ways total) — **only valid when every outcome is equally likely.**
  - Example: rolling a fair die, P(even number) = 3/6 = 1/2.
- Probability is always between 0 (never happens) and 1 (always happens).

> 💡 **Competition point:** The #1 mistake is treating outcomes as equally likely when they're not (e.g. treating "sum of two dice" as 11 equally likely values 2–12 — it's not! You must count the 36 equally likely dice-pairs instead, since sum=7 has 6 ways but sum=2 has only 1).

- **Consistency rule:** when counting the successful outcomes AND the total outcomes, use the SAME method for both (both ordered, or both unordered). Mixing the two gives a wrong answer.

---

## 2. Complement and "At Least One"

- **Complement rule:** P(event happens) = 1 − P(event does NOT happen). Very useful when "at least one" is hard to count directly but "none" is easy.
  - Example: rolling a die 4 times, P(at least one 6) = 1 − P(no 6 in 4 rolls) = 1 − (5/6)⁴.

---

## 3. Independent vs Dependent Events

- **Independent events** (neither affects the other): P(A and B) = P(A) × P(B).
  - Example: two coin flips, P(both heads) = 1/2 × 1/2 = 1/4.
- **Dependent events** (one changes the pool for the next, like drawing without replacement): multiply the changing probabilities step by step.
  - Example: drawing 2 red socks in a row (no replacement) from a drawer of 5 red, 3 blue: P = 5/8 × 4/7 = 20/56 = 5/14.

---

## 4. Addition Rule (Overlapping Events)

- P(A or B) = P(A) + P(B) − P(A and B) — same idea as [[07_Inclusion_Exclusion]], applied to probabilities instead of counts. For mutually exclusive events (can't both happen), just add: P(A or B) = P(A) + P(B).
  - Example: rolling a die, P(even or greater than 4) = 3/6 + 2/6 − 1/6 = 4/6 = 2/3 (subtract the overlap: rolling a 6 is counted in both groups).

---

## 5. Geometric Probability

When outcomes form a continuous range (a random point on a segment, a random arrival time) instead of a countable list, probability = (favorable length/area) ÷ (total length/area).

- Example: a point is picked at random on a 10-unit segment. P(point is within the last 3 units) = 3/10.
- **Classic "meeting problem":** two people each arrive at a random time in a 1-hour window and wait 15 minutes for each other. Plot both arrival times on a square (one axis per person); the region where they overlap is a diagonal band. P(they meet) = (area of the band) ÷ (area of the whole square) — found by subtracting the two unmet corner triangles from the full square, same "whole minus holes" idea from [[02_Angles_Similarity_Circles]].

---

## 6. Expected Value

- **Expected value (E):** the probability-weighted average of all possible outcomes: E = p₁x₁ + p₂x₂ + ... + pₙxₙ, where each xᵢ is an outcome's value and pᵢ its probability.
  - Example: a standard die roll has E = (1+2+3+4+5+6)/6 = 3.5 (note: the expected value doesn't have to be an outcome you can actually roll!).
- **Fair price of a game:** the amount that makes the game break even in the long run = its expected winnings. Charging more than that gives the house an expected profit.
  - Example: a weighted coin (heads 3/4 of the time, wins $2; tails 1/4, loses $1): E = (3/4)(2) + (1/4)(−1) = $1.25. That's the "fair" price to play.

> 💡 **Competition point:** For "find the unknown given the expected value" problems, set up E as an algebraic expression with the unknown, set it equal to the given value, and solve like a normal equation.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Basic probability | favorable ÷ total, only if equally likely |
| Complement | P(not A) = 1 − P(A) |
| Independent events | multiply P(A) × P(B) |
| Dependent events | multiply changing probabilities step by step |
| A or B (overlap) | P(A) + P(B) − P(A and B) |
| Geometric probability | favorable length/area ÷ total length/area |
| Expected value | Σ (outcome × its probability) |
| Fair price | equals the expected value |

---

## Quick Check

1. A bag has 4 red and 6 blue marbles. What's the probability of drawing a red marble?
2. Two dice are rolled. What's the probability the sum is 7?
3. A box has 3 red and 2 blue balls. Two are drawn without replacement. What's the probability both are red?
4. A game gives $10 with probability 1/5 and $0 otherwise. What's the expected value?

<details>
<summary>Answers</summary>

1. 4/10 = **2/5**.
2. 6 ways out of 36 total (1-6,2-5,3-4,4-3,5-2,6-1) = **1/6**.
3. 3/5 × 2/4 = 6/20 = **3/10**.
4. E = (1/5)(10) + (4/5)(0) = **$2**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds directly on [[08_Permutations_Combinations_Counting]] (counting tools) and [[07_Inclusion_Exclusion]] (the addition rule). See [[15_Statistics]] for the mean/median/mode unit.*
