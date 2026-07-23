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

---

## 1. Two Sets — the basic overlap rule

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

- **The three-set formula:**
  - **|A ∪ B ∪ C| = |A| + |B| + |C| − |A∩B| − |A∩C| − |B∩C| + |A∩B∩C|**
  - In words: **add the singles**, **subtract the pairs**, **add back the triple**.
- **Why add the triple back?** An item in **all three** gets added 3 times, then subtracted 3 times (once in each pair) → it disappears completely. So you must **add it back once** to count it.
- **The alternating-sign pattern:** singles **+**, pairs **−**, triples **+**, and (if you ever have 4 sets) fours **−**. The sign flips each level. That flipping is the whole idea of "inclusion–exclusion".

> 💡 **Competition point:** Count multiples of 2, of 3, and of 7 the three-set way, then use the complement (Section 3) to get "divisible by none" (→ Mock Q5-22 below).

---

## 3. The Complement Trick ("none of these")

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

A **Venn diagram** is the fastest way to see the overlaps. Fill the **innermost region first**, then work outward.

- **Problem:** 30 students. 18 play violin, 15 play e-piano, 7 play **both**. How many play **neither**?
  - Both (centre) = **7**
  - Violin only = 18 − 7 = **11**
  - E-piano only = 15 − 7 = **8**
  - At least one = 11 + 8 + 7 = **26** (this is the union)
  - Neither = 30 − 26 = **4**
- **Rule of thumb:** the number written in a circle (like "18 play violin") is the **total** for that circle, so subtract the overlap to get the "only" part.

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

<details>
<summary>Answers</summary>

1. 14 + 11 − 5 = **20**
2. At least one = 20 + 12 − 6 = 26 → neither = 30 − 26 = **4**
3. mult of 2 = 50, mult of 5 = 20, mult of 10 (both) = 10 → 50 + 20 − 10 = **60**
4. mult of 2 = 30, mult of 3 = 20, mult of 6 = 10 → union = 40 → none = 60 − 40 = **20**
5. min both = 30 + 25 − 40 = **15**

</details>

---
*Source map: `약점진단/07_포함배제_원리.md` · Counting continues in [[08_Permutations_Combinations_Counting]]*
