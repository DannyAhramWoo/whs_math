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

> 📖 *Source: AOPS Introduction to Counting & Probability Ch.7 "Introduction to Probability" — §7.2 (basic probability), §7.3 (equally likely outcomes), §7.4 (counting techniques), §7.5 Summary.*

- **What probability means:** if you repeated the experiment **very many times**, the event would happen about this fraction of the time. P = 1/6 means "roughly 1 in 6 rolls".
- **Probability formula:** P(event) = (number of ways it happens) ÷ (number of ways total) — **only valid when every outcome is equally likely.**
  - Example: rolling a fair die, P(even number) = 3/6 = 1/2.
- Probability is always between 0 (never happens) and 1 (always happens). **If you ever get a number below 0 or above 1, you made a mistake** — a quick sanity check.
- **Most probability problems are just two counting problems:** count the favourable outcomes, count the total outcomes, divide. Everything from [[08_Permutations_Combinations_Counting]] applies.

> 💡 **Competition point:** The #1 mistake is treating outcomes as equally likely when they're not (e.g. treating "sum of two dice" as 11 equally likely values 2–12 — it's not! You must count the 36 equally likely dice-pairs instead, since sum=7 has 6 ways but sum=2 has only 1).

- **Consistency rule:** when counting the successful outcomes AND the total outcomes, use the SAME method for both (both ordered, or both unordered). Mixing the two gives a wrong answer.

---

## 2. Complement and "At Least One"

> 📖 *Source: AOPS Introduction to Counting & Probability §8.3 "Complementary Probabilities".*

- **Complement rule:** P(event happens) = 1 − P(event does NOT happen). Very useful when "at least one" is hard to count directly but "none" is easy — the complement turns an ugly casework problem into one subtraction.
  - Example: rolling a die 4 times, P(at least one 6) = 1 − P(no 6 in 4 rolls) = 1 − (5/6)⁴.

---

## 3. Independent vs Dependent Events

> 📖 *Source: AOPS Introduction to Counting & Probability §8.4 "Probability and Multiplication" (independent) & §8.5 "Probability with Dependent Events".*

- **Independent events** (neither affects the other): P(A and B) = P(A) × P(B).
  - Example: two coin flips, P(both heads) = 1/2 × 1/2 = 1/4.
- **Dependent events** (one changes the pool for the next, like drawing without replacement): multiply the changing probabilities step by step.
  - Example: drawing 2 red socks in a row (no replacement) from a drawer of 5 red, 3 blue: P = 5/8 × 4/7 = 20/56 = 5/14.

> ⚠️ **Warning (the book's Bogus Solution):** for **without-replacement** draws, don't reuse the first probability. Drawing two cards of the same suit is 13/52 × **12/51**, *not* 13/52 × 13/52 — after the first card, one suit-card and one card are gone, so the second fraction changes.

---

## 4. Addition Rule (Overlapping Events)

> 📖 *Source: AOPS Introduction to Counting & Probability §8.2 "Probability and Addition".*

- P(A or B) = P(A) + P(B) − P(A and B) — same idea as [[07_Inclusion_Exclusion]], applied to probabilities instead of counts. For **mutually exclusive** events (can't both happen), the overlap is 0, so just add: P(A or B) = P(A) + P(B). This extends to any number of pairwise-exclusive events: P(A₁ or … or Aₙ) = P(A₁) + … + P(Aₙ).
  - Example: rolling a die, P(even or greater than 4) = 3/6 + 2/6 − 1/6 = 4/6 = 2/3 (subtract the overlap: rolling a 6 is counted in both groups).

---

## 5. Geometric Probability

> 📖 *Source: AOPS Introduction to Counting & Probability Ch.10 "Geometric Probability" — §10.2 (lengths), §10.3 (areas), including the meeting problem.*

- **Discrete vs continuous:** when the outcomes are a **countable list** (die faces, cards) you count them; when they form a **continuous range** (any point on a line, any time in an hour) you can't count — you measure length or area instead.
- **First find the "successful region", then divide by the whole.** When outcomes form a continuous range, probability = (favorable length/area) ÷ (total length/area).

- Example: a point is picked at random on a 10-unit segment. P(point is within the last 3 units) = 3/10.
- **Classic "meeting problem":** two people each arrive at a random time in a 1-hour window and wait 15 minutes for each other. Plot both arrival times on a square (one axis per person); the region where they overlap is a diagonal band. P(they meet) = (area of the band) ÷ (area of the whole square) — found by subtracting the two unmet corner triangles from the full square, same "whole minus holes" idea from [[02_Angles_Similarity_Circles]].

---

## 6. Expected Value

> 📖 *Source: AOPS Introduction to Counting & Probability Ch.11 "Expected Value" — §11.2 (definition), §11.3 (problems), §11.5 Summary.*

- **Expected value (E, sometimes written μ):** the probability-weighted average of all possible outcomes: E = p₁x₁ + p₂x₂ + ... + pₙxₙ, where each xᵢ is an outcome's value and pᵢ its probability. (The weights must satisfy **p₁ + p₂ + … + pₙ = 1** — every outcome accounted for.)
  - Example: a standard die roll has E = (1+2+3+4+5+6)/6 = 3.5 (note: the expected value doesn't have to be an outcome you can actually roll!).
- **E generalises the plain average:** if **all outcomes are equally likely**, the expected value is just the ordinary mean. When they aren't, E weights each outcome by how likely it is.
- **Expected value of a sum (linearity):** the expected value of two things added is the **sum of their expected values** — E(X + Y) = E(X) + E(Y), *even if X and Y affect each other*. E.g. the expected total of two dice = 3.5 + 3.5 = **7**.
- **Fair price of a game:** the amount that makes the game break even in the long run = its expected winnings. Charging more than that gives the house an expected profit.
  - Example: a weighted coin (heads 3/4 of the time, wins $2; tails 1/4, loses $1): E = (3/4)(2) + (1/4)(−1) = $1.25. That's the "fair" price to play.

> 💡 **Competition point:** For "find the unknown given the expected value" problems, set up E as an algebraic expression with the unknown, set it equal to the given value, and solve like a normal equation.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Basic probability | favorable ÷ total, only if equally likely |
| Probability range | between 0 and 1 (else you erred) |
| Complement | P(not A) = 1 − P(A); use for "at least one" |
| Independent events | multiply P(A) × P(B) |
| Dependent events | multiply changing probabilities step by step |
| A or B (overlap) | P(A) + P(B) − P(A and B); exclusive → just add |
| Discrete vs continuous | count outcomes vs measure length/area |
| Geometric probability | favorable length/area ÷ total length/area |
| Expected value | Σ (outcome × its probability); weights sum to 1 |
| E of a sum | E(X + Y) = E(X) + E(Y) |
| Fair price | equals the expected value |

---

## Quick Check

1. A bag has 4 red and 6 blue marbles. What's the probability of drawing a red marble?
2. Two dice are rolled. What's the probability the sum is 7?
3. A box has 3 red and 2 blue balls. Two are drawn without replacement. What's the probability both are red?
4. A game gives $10 with probability 1/5 and $0 otherwise. What's the expected value?
5. A die is rolled 3 times. Using the complement, find P(at least one 6).
6. What is the expected total when you roll two fair dice? (Use linearity.)

<details>
<summary>Answers</summary>

1. 4/10 = **2/5**.
2. 6 ways out of 36 total (1-6,2-5,3-4,4-3,5-2,6-1) = **1/6**.
3. 3/5 × 2/4 = 6/20 = **3/10**.
4. E = (1/5)(10) + (4/5)(0) = **$2**.
5. 1 − P(no 6) = 1 − (5/6)³ = 1 − 125/216 = **91/216**.
6. Each die has E = 3.5, so E(sum) = 3.5 + 3.5 = **7**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. Builds directly on [[08_Permutations_Combinations_Counting]] (counting tools) and [[07_Inclusion_Exclusion]] (the addition rule). See [[15_Statistics]] for the mean/median/mode unit.*
