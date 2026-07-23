# 07. Inclusion-Exclusion Principle

> **Unit:** Counting (Unit 07 of 14) · **9 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** When you count things that **overlap** — people in two clubs, numbers that are multiples of both 2 and 3 — simple adding gives the wrong answer. Inclusion-Exclusion is the tool that fixes double-counting. It shows up in almost every counting problem.

---

## Lesson Overview
What this note covers:

1. Two Sets — the basic overlap rule
2. Three Sets — add, subtract, add back
3. The Complement Trick ("none of these")
4. A Worked Venn Example — *Sec 1*
5. Min / Max Overlap (pigeon-style bounds) — *Sec, advanced*
6. The Probability Version (mutually exclusive events) — *Sec 1*

---

## 1. Two Sets — the basic overlap rule

> 📖 *Source: AOPS Introduction to Counting & Probability §1.3 "Counting with Addition and Subtraction" (pp.6–12).*

- **Set:** just a group of things. **|A|** means "how many things are in group A".
- **Union (A or B):** everything that is in A **or** B **or both**. Written **|A ∪ B|**.
- **Intersection (A and B):** the things that are in **both** A and B. Written **|A ∩ B|**.
- **The two-set formula:**
  - **|A ∪ B| = |A| + |B| − |A ∩ B|**
  - Why the minus? If you just add |A| + |B|, the **overlap gets counted twice** (once in A, once in B). Subtract it **once** to fix that.
  - Example: 20 like juice, 15 like milk, 8 like **both**. How many like at least one? → 20 + 15 − 8 = **27**.

> 💡 **Competition point:** The same rule works for **overlapping shapes**. Area(square1) + Area(square2) − Area(overlap) = Area covered (→ NM 2008 Q03 below).

---

## 2. Three Sets — add, subtract, add back

> 📖 *Source: standard inclusion–exclusion. AOPS Introduction to Counting & Probability develops the two-circle case in §1.3; the three-circle Venn extension follows the same "fill each region" logic.*

- **The three-set formula:**
  - **|A ∪ B ∪ C| = |A| + |B| + |C| − |A∩B| − |A∩C| − |B∩C| + |A∩B∩C|**
  - In words: **add the singles**, **subtract the pairs**, **add back the triple**.
- **Why add the triple back?** An item in **all three** gets added 3 times, then subtracted 3 times (once in each pair) → it disappears completely. So you must **add it back once** to count it.
- **The alternating-sign pattern:** singles **+**, pairs **−**, triples **+**, and (if you ever have 4 sets) fours **−**. The sign flips each level. That flipping is the whole idea of "inclusion–exclusion".

> 💡 **Competition point:** Count multiples of 2, of 3, and of 7 the three-set way, then use the complement (Section 3) to get "divisible by none" (→ Mock Q5-22 below).

---

## 3. The Complement Trick ("none of these")

> 📖 *Source: AOPS Introduction to Counting & Probability §2.3 "Complementary Counting" (p.35) — count the opposite, then subtract from the total.*

- **Complement:** the **opposite** group — everything that is **not** in your set. If there are **N** things in total, then
  - **(not in A ∪ B ∪ C) = N − |A ∪ B ∪ C|**
- **How to use it:** many problems ask "how many are divisible by **none** of these" or "wear **neither** X nor Y". Steps:
  1. Count the union |A ∪ B ∪ C| with the formula above.
  2. Subtract from the **total N**.
- **For counting multiples up to N:** the number of multiples of *d* from 1 to N is **⌊N ÷ d⌋** (whole-number part of the division).
  - Example: multiples of 7 up to 500 → ⌊500 ÷ 7⌋ = **71**. For "both 2 and 3", count multiples of **LCM(2,3)=6**.

> 💡 **Competition point:** "Not divisible by 2, 3 or 7" from 1 to 500 = 500 − |mult of 2 or 3 or 7| (→ Mock Q5-22 below). Always turn "none" into total minus union.

---

## 4. A Worked Venn Example — *Sec 1*

> 📖 *Source: AOPS Introduction to Counting & Probability §1.3 — the Venn-diagram method and the "let a region be a variable" technique (cats/kittens example, pp.9–11). A **Venn diagram** is named after John Venn (1834–1923), who first published it in 1881.*

A **Venn diagram** is the fastest way to see the overlaps. Fill the **innermost region first**, then work outward.

- **Problem:** 30 students. 18 play violin, 15 play e-piano, 7 play **both**. How many play **neither**?
  - Both (centre) = **7**
  - Violin only = 18 − 7 = **11**
  - E-piano only = 15 − 7 = **8**
  - At least one = 11 + 8 + 7 = **26** (this is the union)
  - Neither = 30 − 26 = **4**
- **Rule of thumb:** the number written in a circle (like "18 play violin") is the **total** for that circle, so subtract the overlap to get the "only" part.

**The "let a region be x" method** (when you *don't* know the overlap). Put a variable in the region you don't know, write every other region in terms of it, then use the grand total to solve.

- **Problem:** 27 cats; 14 are short-haired, 11 are kittens, 5 are neither. How many short-haired kittens?
  - Let the overlap (short-haired kittens) = **x**. Then short-haired-only = 14 − x, kittens-only = 11 − x, and outside = 5.
  - All regions sum to the total: `(14 − x) + x + (11 − x) + 5 = 27` → `30 − x = 27` → **x = 3**.
- **Concept (from the book):** when you set up a variable, **let it stand for the quantity the problem is asking for** — then you solve for the answer directly.

> 💡 **Competition point:** When a problem gives two categories with two options each (e.g. white/black top **and** black/blue bottom), draw a small table and use the union rule (→ Mock Q4-16 below).

---

## 5. Min / Max Overlap (pigeon-style bounds) — *Sec, advanced*

- **Maximum overlap** of two groups = the size of the **smaller** group (one can sit entirely inside the other).
- **Minimum overlap** of A and B inside a total N:
  - **min(A ∩ B) = |A| + |B| − N** (and if that is negative, the minimum is 0).
  - Why? To keep the overlap **small**, spread the two groups apart. But once |A| + |B| is bigger than N, they are **forced** to share |A| + |B| − N members.
- **Many sets, "who can do ALL of them":** to find the **smallest** number who satisfy every condition, add up the people **missing** each condition; the total who fail at least one is **at most** that sum, so
  - **(do all) ≥ N − (sum of the ones who miss each)**.

> 💡 **Competition point:** "At least how many people can do all 4 sports?" or "minimum in both sets" both use **|A|+|B|−N** style bounds (→ RI 2023 Q13, AP 2021 Q21 below).

---

## 6. The Probability Version (mutually exclusive events) — *Sec 1*

> 📖 *Source: AOPS Introduction to Counting & Probability §8.2 "Probability and Addition" (pp.123–126).*

The exact same add/subtract idea works for **probabilities**, not just counts.

- **Mutually exclusive events:** two events that **cannot both happen at once** (rolling a 1 vs rolling a 4 on one die). For these, **P(A or B) = P(A) + P(B)** — just add. This extends to any number: P(A₁ or A₂ or … or Aₙ) = P(A₁) + … + P(Aₙ) **when they are pairwise mutually exclusive**.
- **When events *can* overlap, subtract the overlap** — the probability inclusion-exclusion rule: **P(A or B) = P(A) + P(B) − P(A and B)**.
  - Example: draw one card from 52. P(Queen or ◊) = P(Queen) + P(◊) − P(Queen of ◊) = 4/52 + 13/52 − 1/52 = **16/52 = 4/13**. (The queen of diamonds was counted in both, so subtract it once.)

> ⚠️ **Warning:** "Add the probabilities" only works when the events are **mutually exclusive**. If they can happen together (like "Queen" and "diamond"), you must **subtract P(both)** — exactly the two-set rule from Section 1, in probability form.

---

## 📚 From the Books (extra tricks)

- **Set language:** **B ⊆ A** ("B is a subset of A") just means every member of B is also in A. The **universal set U** is "everything we're talking about" for that problem. **A∩B** = "in both" (intersection), **A∪B** = "in either" (union) — same symbols as Sections 1–2, just the formal names.
- **Counting subsets:** a set with **n** elements has **2ⁿ** subsets in total (this includes the empty set and the whole set itself), and **2ⁿ − 1 proper subsets** (all subsets except the whole set). Exactly **2ⁿ ⁄ 2** of the subsets have an **even** number of elements.
  - Example: a 5-element set → 2⁵ = **32** subsets total, **31** proper subsets, **16** with an even element-count.

> 💡 **Competition point:** If a problem says "how many subsets does {a,b,c,d,e} have", don't list them — just compute 2ⁿ.

- **The "tickets" method** for "at least how many people do **ALL** k activities": give each person one ticket per activity they like, and add up **all** tickets given out. Everyone then gives back tickets until they hold **at most (k−1)** each (people who like fewer activities just give back everything). Whatever tickets are **left over** can only belong to people who like **all k** activities.
  - Example: 4 activities liked by 78%, 80%, 84%, 88% of 100 students → 332 tickets handed out. At most 3×100 = 300 can be given back (everyone keeps ≤3). So at least 332 − 300 = **32** students like all 4.
  - This is another way to get the same kind of bound as Section 5's min-overlap formula, but works cleanly for **more than 2** groups.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Two sets | \|A∪B\| = \|A\|+\|B\|−\|A∩B\| |
| Three sets | singles − pairs + triple |
| Sign pattern | +, −, +, −, … (flips each level) |
| Unknown overlap | let it = x, write regions in x, sum = total |
| Mutually exclusive | P(A or B) = P(A) + P(B) |
| Overlapping events | P(A or B) = P(A) + P(B) − P(A and B) |
| "None of these" | total N − union |
| Multiples of d up to N | ⌊N ÷ d⌋ |
| "Both 2 and 3" | count multiples of LCM = 6 |
| Venn diagram | fill the centre first |
| Max overlap | size of the smaller group |
| Min overlap | \|A\|+\|B\|−N (or 0) |
| "Do all" minimum | N − (sum of those who miss each) |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Inclusion-Exclusion Principle**
- [NM 2008 Q03](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/03.png) — overlap area of two squares → area1 + area2 − union
- [NM 2008 Q08](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/08.png) — greatest number wearing **neither** a bow-tie nor glasses (max "neither")
- [NM 2010 Q14](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/14.png) — students comparing their Maths and English grades (two overlapping groups)
- [Mock Q2-8](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_8.png) — how many play violin **or** e-piano → union count
- [Mock Q4-16](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_16.png) — 60 people, white/black tops & black/blue bottoms; find black-top **and** black-bottom
- [Mock Q5-22](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_22.png) — from 1 to 500, how many are divisible by **none** of 2, 3, 7
- [RI 2023 Q13](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/13.png) — 46 people; the **minimum** who can do all 4 sports
- [AP 2021 Q19](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/19.png) — arrange 6 cards so neighbours differ in colour and number (careful counting)
- [AP 2021 Q21](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/21.png) — SMOPS and HCIC participant sets → union / overlap

---

## Quick Check

1. 25 pupils: 14 like apples, 11 like bananas, 5 like both. How many like at least one?
2. 30 people: 20 wear a hat, 12 wear a scarf, 6 wear both. How many wear **neither**?
3. From 1 to 100, how many numbers are multiples of 2 **or** 5?
4. From 1 to 60, how many are divisible by **none** of 2 and 3?
5. In a class of 40, 30 passed Maths and 25 passed Science. What is the **least** number who passed **both**?
6. A card is drawn from 52. Find P(King or ♥) — remember to subtract the overlap.
7. 25 cats: 16 are black, 12 have long tails, 4 are neither. Using "let x = both", how many are black **and** long-tailed?

<details>
<summary>Answers</summary>

1. 14 + 11 − 5 = **20**
2. At least one = 20 + 12 − 6 = 26 → neither = 30 − 26 = **4**
3. mult of 2 = 50, mult of 5 = 20, mult of 10 (both) = 10 → 50 + 20 − 10 = **60**
4. mult of 2 = 30, mult of 3 = 20, mult of 6 = 10 → union = 40 → none = 60 − 40 = **20**
5. min both = 30 + 25 − 40 = **15**
6. 4/52 + 13/52 − 1/52 = 16/52 = **4/13** (the King of hearts is the overlap)
7. black-only (16−x) + both (x) + long-only (12−x) + neither (4) = 25 → 32 − x = 25 → **x = 7**

</details>

---
*Source map: `약점진단/07_포함배제_원리.md` · Counting continues in [[08_Permutations_Combinations_Counting]]*
