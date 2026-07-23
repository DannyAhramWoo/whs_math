# 15. Statistics

> **Unit:** Statistics (Unit 15 · extra unit from book scans, no linked quiz-app problems yet)
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Mean, median, mode, and range show up in word problems and data-table questions. None of the other 13 units cover this — it's a completely separate skill.

---

## Lesson Overview
What this note covers:

1. Mean, Median, Mode, Range
2. Using a "Guessed Mean" Shortcut
3. Harmonic Mean and Geometric Mean
4. Mean/Median/Mode Together (harder problems)
5. Reading Data Displays

---

## 1. Mean, Median, Mode, Range

> 📖 *Source: AOPS Prealgebra §13.1 "Basic Statistics" (Ch.13 "Data and Statistics") — mean/median/mode/range and the "balance" view of the average.*

- **Mean (average):** sum of all values ÷ how many values there are.
  - Example: 3, 5, 6, 10 → mean = (3+5+6+10)/4 = 6.
- **Median:** the middle value once the list is sorted. If there's an even number of values, average the two middle ones.
  - Example: 4, 5, 7, 8, 11 → median = 7 (the middle one).
  - Example (even count): 4, 5, 7, 8 → median = (5+7)/2 = 6.
- **Mode:** the value(s) that appear most often. A list can have no mode, one mode, or several (if tied). (The mode is often the *least* useful summary — one common value can be misleading.)
- **Range:** biggest value − smallest value.

> ⚠️ **Warning:** mean, median, and mode are all sometimes called "averages", but in everyday use **"the average" means the mean**. Say which one you mean.

**The average is a "balance point".** The total amount that values sit **above** the mean exactly equals the total amount they sit **below** it. Two useful consequences:

- **Raise-the-average (working backward):** to hit a target average, first find the **total you'd need** (target × count), then subtract what you already have. E.g. you scored 82, 88, 91 on three tests; to average 88 over four tests you need a total 88 × 4 = 352, so the 4th test must be 352 − 261 = **91**.
- **Add a constant to every value → the mean shifts by that constant** (add 5 to every score → the average goes up by exactly 5). Likewise multiplying every value by k multiplies the mean by k.

> 💡 **Competition point:** An **outlier** (one value far from the rest) swings the **mean** a lot but barely moves the **median** — so when one value is extreme, the median is the more "honest" summary. Statistics can mislead: an average alone tells you nothing about the **spread** or the **totals** behind it.

---

## 2. Using a "Guessed Mean" Shortcut

Instead of adding up a long list of numbers, guess a nearby round number as your "trial mean," then sum the **deviations** (how far each number is above/below the guess) and adjust.

- Example: for 97, 102, 99, 105, 101, guess mean = 100. Deviations: −3, +2, −1, +5, +1 → sum = +4. True mean = 100 + 4/5 = 100.8.

> 💡 **Competition point:** This trick turns big-number addition into small-number addition — very useful when values are clustered close together.

---

## 3. Harmonic Mean and Geometric Mean

> 📖 *Source: these two "other means" are beyond the Prealgebra statistics chapter. The **geometric mean** appears in AOPS Intro to Algebra §21.3 (as the middle term of a geometric sequence); the **harmonic mean** appears in AOPS Prealgebra §7.5 as a Sidenote on round-trip average speed. Both are standard competition tools.*

- **Geometric mean** of n numbers = the nth root of their product. For two numbers a and b: geometric mean = √(ab).
  - Example: geometric mean of 4 and 9 = √36 = 6.
- **Harmonic mean** of n numbers = n ÷ (sum of the reciprocals of the numbers).
  - Example: harmonic mean of 1, 2, 4 = 3 ÷ (1/1 + 1/2 + 1/4) = 3 ÷ (7/4) = 12/7.

> 💡 **Competition point:** The classic "average speed for a round trip" problem (same distance there and back, different speeds) is really a **harmonic mean** in disguise — see [[10_Distance_Speed_Time]] for the speed version of this formula.

---

## 4. Mean/Median/Mode Together (harder problems)

> 📖 *Source: AOPS Prealgebra §13.1 (Problem 13.7, the classic AMC-8 "mean 15, median 18, biggest possible largest value" — with its Bogus Solution) and §13.2 "Limits of Basic Statistics".*

Some problems fix the mean, median, AND range (or mode) all at once, and ask you to find missing numbers. The method:

1. Use the **median** to pin down the middle value(s) — this bounds what the sorted list can look like.
2. Use the **mean** to find the total sum of all numbers, then subtract the known values to find what's left.
3. **Case-check**: try the different orderings/digit choices that fit the constraints, and eliminate any that break a rule (like all numbers needing to be distinct, or a specific mode).

> 💡 **Competition point:** These problems reward careful bounding before guessing — figure out the tightest range for each unknown first, then check a short list of candidates rather than guessing randomly.

---

## 5. Reading Data Displays

> 📖 *Source: AOPS Prealgebra §13.3 "Tables, Graphs, and Charts".*

Exams often give the data as a **picture** instead of a list. Know how to read each one, then apply §1.

- **Bar chart / histogram:** bar heights give counts. A **histogram** groups values into ranges (bins), so you can find the mean/median *approximately* but not the exact values (grouping hides them).
- **Stem-and-leaf plot:** the "stem" is the leading digit(s), each "leaf" a last digit. `4 | 2 5 7` means 42, 45, 47. It keeps every exact value, so you can read off mean, median, and mode directly.
- **Line graph:** shows how a value changes over time. Good for trends.
- **Pie chart:** each slice is a **percent of the whole** (all slices add to 100%). Multiply a slice's percent by the total to get its amount.

> ⚠️ **Warning:** graphs can be made **misleading by the choice of scale** — a bar chart that doesn't start at 0, or a stretched axis, exaggerates differences. Always read the axis numbers, not just the picture.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Mean | sum ÷ count |
| Median | middle value after sorting (average of 2 middles if even count) |
| Mode | most frequent value(s) |
| Range | max − min |
| Outlier | swings mean a lot, median barely moves |
| Raise the average | need total = target × count, minus what you have |
| Add c to every value | mean goes up by c |
| Guessed mean | sum deviations from a round number, then adjust |
| Stem-and-leaf | stem = leading digits, leaf = last digit (exact values) |
| Pie chart | each slice = percent of the whole |
| Misleading graph | check the axis scale (may not start at 0) |
| Geometric mean (2 numbers) | √(a×b) |
| Harmonic mean (2 numbers) | 2ab/(a+b) — same idea as round-trip average speed |
| Mean+median+range problems | bound with median first, then use mean for the total, then case-check |

---

## Quick Check

1. Find the mean, median, and mode of: 2, 4, 4, 5, 6, 10, 4.
2. A list has mean 6 and 5 numbers. What is their total sum?
3. Find the geometric mean of 8 and 18.
4. Find the harmonic mean of 6 and 12.
5. Your first three test scores are 78, 85, 89. What must you score on the 4th test to average 85?
6. A pie chart shows 40% of 350 students chose maths. How many is that?

<details>
<summary>Answers</summary>

1. Mean = (2+4+4+5+6+10+4)/7 = 35/7 = **5**. Sorted: 2,4,4,4,5,6,10 → median = **4**. Mode = **4** (appears 3 times).
2. Sum = mean × count = 6 × 5 = **30**.
3. √(8×18) = √144 = **12**.
4. 2×6×12/(6+12) = 144/18 = **8**.
5. Need total 85 × 4 = 340; you have 78+85+89 = 252; so the 4th = 340 − 252 = **88**.
6. 40% × 350 = **140 students**.

</details>

---
*This is a new unit added from book scans (2026-07-22) — no quiz-app problems are linked to it yet. See [[08_Permutations_Combinations_Counting]] for the closely related unit on probability, and [[10_Distance_Speed_Time]] for the harmonic-mean speed formula.*
