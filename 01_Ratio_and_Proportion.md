# 01. Ratio and Proportion

> **Unit:** Ratio / Proportion (Unit 01 of 14) · **19 linked problems**
> **For:** primary competition students (SMO · NMOS · IMSO) — concepts go up to **Secondary 2** level
> **Why it matters:** This is the single biggest weak spot. Most of the linked problems are "side ratio → area ratio" geometry problems. Once the three area tricks and the proportion setup below are automatic, a whole page of these problems becomes routine.

---

## Lesson Overview
What this note covers:

1. What a Ratio Really Means
2. Simplifying Ratios (whole numbers, fractions, decimals)
3. Multi-way Ratios (a : b : c)
4. Part-of-the-Whole Thinking
5. Proportions and Cross-Multiplication
6. Side Ratio → Area Ratio (the big weapon)
7. Share One Vertex → Multiply Ratios — *Sec 1*
8. Similarity: Ratio Squared, Ratio Cubed — *Sec 2*
9. Move an Amount, Then Ratio (invariants)
10. Combined Ratio (Chaining)
11. Rates, Conversions, Direct/Inverse/Joint Proportion

---

## 1. What a Ratio Really Means

> 📖 *Source: AOPS Prealgebra §7.1 "What is a Ratio?"*

- A **ratio** compares the *relative* sizes of two (or more) quantities. If a class has 10 girls and 7 boys, the ratio of girls to boys is **10 to 7**, written three ways:
  - `10 to 7`, `10 : 7`, or `10/7`. The middle form `10 : 7` is the most common; it is spoken "10 to 7."
- **A ratio tells you nothing about the actual totals.** If girls : boys = 2 : 3, there could be 2 & 3, or 10 & 15, or 200 & 300. All you know is: if there are `2n` girls, there are `3n` boys — but you don't know `n`.

> **Concept:** A ratio is a *relative* comparison. By itself it never tells you the total amount — you always need one more piece of information (a total, a difference, or one actual value) to pin down the real numbers.

- **Ratios behave like fractions.** The ratio `12 : 6` is the same comparison as the fraction `12/6`, and both simplify to `2 : 1`. Anything you can do to a fraction (scale up, reduce, cross-multiply), you can do to a ratio.

---

## 2. Simplifying Ratios

> 📖 *Source: AOPS Prealgebra §7.1, Problem 7.1 (a)–(e)*

**To simplify a ratio** means to write it using integers whose greatest common factor is 1.

**(a) Whole-number ratios — divide out the GCF.**
- `2 : 10` → divide both by 2 → **`1 : 5`**.
- `9 : 6` → divide both by 3 → **`3 : 2`**.

**(b) Fraction ratios — multiply by the LCM of the denominators.**
- `½ : ⅓` → the denominators are 2 and 3, LCM = 6. Multiply both parts by 6:
  - `(½·6) : (⅓·6) = 3 : 2`.
- **Mixed numbers first become improper fractions.** `2⅓ : 1⁴⁄₉`:
  - `2⅓ = 7/3`, `1⁴⁄₉ = 13/9`, so the ratio is `7/3 : 13/9`. Denominators 3 and 9 → LCM 9. Multiply by 9: `21 : 13`. (GCF of 21 and 13 is 1, so it's done.)

**(c) Decimal ratios — multiply by a power of 10, then reduce.**
- `1.4 : 2.4` → ×10 → `14 : 24` → ÷2 → **`7 : 12`**.

**(d) Two tricky cases worth knowing (from the exercises):**
- **Powers — factor first.** `6³ : 8³`. Write `6³ = (2·3)³ = 2³·3³` and `8³ = (2·4)³ = 2³·4³`; the common factor is `2³`, so `6³ : 8³ = 3³ : 4³ = 27 : 64`.
- **A zero part.** `672 : 0` → divide both by 672 → **`1 : 0`**. A ratio can legitimately have a 0 part; it just means "none of the second thing."

> 💡 **Competition point:** A ratio is *not* in simplest form if the parts share a common factor (`6 : 4 : 8` still divides by 2) **or** if any part is not an integer (`½ : ⅓ : ⅔` — clear the fractions first). Check both conditions before you call it "done."

---

## 3. Multi-way Ratios (a : b : c)

> 📖 *Source: AOPS Prealgebra §7.2 "Multi-way Ratios"*

- The same rules extend to three or more quantities. If a pet store has 4 dogs, 5 cats, and 11 goldfish, that's `4 : 5 : 11` (already simplest — no common factor).
- `9 : 12 : 21` → all divisible by 3 → `3 : 4 : 7`.
- A multi-way ratio still only gives relative sizes: `1 : 2 : 5` could be 1, 2, 5 or 6, 12, 30 — for any `n`, it's `n : 2n : 5n`.

**Removing a term.** You can drop parts of a multi-way ratio to compare just two of the quantities. From butter : flour : sugar : milk = `1 : 6 : 2 : 1`, the butter-to-sugar ratio alone is just `1 : 2`.

> **Concept:** You can pull any two terms out of a multi-way ratio to get a simpler two-part ratio between just those quantities.

---

## 4. Part-of-the-Whole Thinking

> 📖 *Source: AOPS Prealgebra §7.2, Problems 7.7–7.9 (prize money, cake, paint)*

This is the most powerful single idea for ratio word problems where you're given a **total**.

- If quantities are in ratio `a : b : c`, then the total is split into `a + b + c` equal parts. Each quantity is its share of the whole:
  - first quantity = `a/(a+b+c)` × total, and so on.

**Worked example (prize money).** A bowling tournament pays the top 3 in ratio `5 : 2 : 1`, total \$1000.
- Total parts = 5 + 2 + 1 = 8. One part = \$1000 / 8 = \$125.
- First place = 5 parts = **\$625**.

**Worked example (paint).** A mix is 2 parts blue, 3 parts white, 1 part red, total 3 gallons.
- Red is `1/(2+3+1) = 1/6` of the whole → `1/6 × 3 = ½` gallon of red.

**Worked example (rope).** A 10-ft rope is cut in ratio 1 : 4. The longer piece is `4/(1+4) = 4/5` of the whole → `4/5 × 10 = 8 ft`.

**Worked example — three methods for one problem (worth studying).** A cake needs butter : flour : sugar : milk = `1 : 6 : 2 : 1`, and you have ½ cup of sugar. How much of each other ingredient?
- **Method A — rescale so the known part matches.** Sugar is the "2" slot but you have ½, so divide every term by 4: `1 : 6 : 2 : 1 = ¼ : 3/2 : ½ : ¼`. Read off: butter ¼, flour 3/2, milk ¼ cup.
- **Method B — split into two-part ratios.** Butter : sugar = `1 : 2`, so butter = ½ × ½ = ¼. Flour : sugar = `6 : 2 = 3 : 1`, so flour = 3 × ½ = 3/2. Milk : sugar = `1 : 2`, so milk = ¼.
- **Method C — parts of the whole.** Sugar is `2/(1+6+2+1) = 2/10 = 1/5` of the whole. Since ½ cup = 1/5 of the total, total = ½ ÷ 1/5 = 5/2 cups. Then butter = 1/10 × 5/2 = ¼, flour = 6/10 × 5/2 = 3/2, milk = ¼.

> **Concept:** No ratio method is "the right one." Ratios reward flexible thinking — pick whichever of "rescale / split / parts-of-whole" makes the given numbers easiest.

---

## 5. Proportions and Cross-Multiplication

> 📖 *Source: AOPS Prealgebra §7.3 "Proportions" (Mario chocolate-milk intro), Problems 7.13–7.15 (shadow, map scale, blueprint)*

- A **proportion** is a statement that two ratios are equal: `2 : 3 = 8 : 12`.
- **What a proportion is really for:** it describes two changing quantities whose **ratio stays constant** as they grow or shrink together.
  - *Mario's chocolate milk:* the recipe uses 8 oz milk to 2 oz syrup — a ratio of `8 : 2 = 4 : 1`. To make enough for 6 people he needs `6 × 8 = 48` oz milk and `6 × 2 = 12` oz syrup, and `48 : 12` is **still** `4 : 1`. No matter the batch size the ratio is always 4 : 1 — we say milk and syrup are **proportional** (or *in proportion*).
- **Cross-multiply rule:** in `a : b = c : d`, the product of the means equals the product of the extremes → **`b × c = a × d`**.
  - `2 : 3 = 8 : x` → `3 × 8 = 2 × x` → `x = 12`.

**Where proportions hide (all the same idea):**
- **Shadows / heights.** At a fixed time, an object's length is proportional to its shadow. Sadie is 3 ft tall with an 8 ft shadow (ratio 3 : 8). Nick is 5 ft tall — his shadow `x` satisfies `5 : x = 3 : 8`, so `40 = 3x`, `x = 13⅓ ft`.
- **Map scale.** A scale `¼ inch = 5 miles` is the ratio `¼ : 5 = 1 : 20`. So 13 inches on the map means `13 × 20 = 260` miles.
- **Blueprints.** Building : window = 30 ft : 8 ft = 15 : 4. On the blueprint the building is 8 in, so window height `x` solves `15 : 4 = 8 : x` → `15x = 32` → `x = 2²⁄₁₅` inches.

> 💡 **Competition point:** Almost every ratio word problem becomes a proportion `a : b = c : d`. Write it, cross-multiply, solve for the one unknown. The hard part is usually *setting it up correctly*, not the algebra.

---

## 6. Side Ratio → Area Ratio (the big weapon)

> 📖 *Source: competition weakness analysis (`약점진단/01`); "fixed shape from area" example from AOPS Prealgebra §7.3, Problem 7.16 (enlarging a photo)*

This is the real weakness — **9 of the 19 linked problems live here.** Three tools handle almost all of them.

**Tool 1 — Same height → area ratio = base ratio.**
If two triangles sit on **one straight line** and share the **same apex (top vertex)**, they have the same height. So their area ratio equals their base ratio.
- Point D on BC with BD : DC = 2 : 3 → triangle ABD : triangle ACD = **2 : 3**.
- Why: area = ½ × base × height; the height is shared, so only the base matters.

> 💡 **Competition point:** Hunt for a point that splits one side. The two triangles it creates always inherit the split ratio as their area ratio (→ RI 2023 Q18 uses BD = DE = EC to chop a triangle into equal-area thirds).

**Tool 2 — Width×height for rectangles / area = (linear)² for growth** (see §8).

**Tool 3 — The "fixed shape, given area" proportion (from the photo problem).**
A wallet photo is 3 cm × 5 cm, so width : height = `3 : 5` always. To enlarge it to area 135 cm², let width = 3x, height = 5x:
- area = `(3x)(5x) = 15x² = 135` → `x² = 9` → `x = 3`. New photo is `3x = 9` cm wide, `5x = 15` cm tall.

This is the algebra engine behind every "the shape stays similar, find the new size from the area" problem — including the geometry ones below.

---

## 7. Share One Vertex → Multiply Ratios — *Sec 1*

> 📖 *Source: competition technique (`약점진단/01`); related to the area-ratio lemma in AOPS Introduction to Geometry (similar triangles chapter)*

- In triangle ABC, put D on AB and E on AC. Then the corner triangle ADE compares to ABC by **multiplying the two side fractions**:
  - **triangle ADE : triangle ABC = (AD × AE) : (AB × AC)**.
- If AD : DB = m : 1 and AE : EC = n : 1, then AD : AB = m : (m+1), AE : AC = n : (n+1), so
  - triangle ADE : triangle ABC = **(m·n) : ((m+1)(n+1))**.
- Numbers: AD : DB = 2 : 1, AE : EC = 3 : 1 → ratio = (2·3) : (3·4) = 6 : 12 = **1 : 2**.

> 💡 **Competition point:** When a small triangle sits in a corner sharing one vertex, multiply the two side fractions to get its share of the big triangle (→ Mock Q2-26, Mock Q1-26).

---

## 8. Similarity: Ratio Squared, Ratio Cubed — *Sec 2*

> 📖 *Source: AOPS Introduction to Geometry (similarity chapter — "ratio of areas = square of ratio"); volume version from AOPS Prealgebra Ch.11 (solids)*

- **Similar shapes** have the same shape but different size; every matching length is in the same ratio (the *similarity ratio*).
- **Area scales as the ratio squared.** Side ratio `2 : 3` → area ratio `2² : 3² = 4 : 9`.
  - Doubling every side (ratio `1 : 2`) makes area **4×** bigger — never "2× bigger."
- **Volume scales as the ratio cubed.** Side ratio `2 : 3` → volume ratio `2³ : 3³ = 8 : 27`.

> 💡 **Competition point:** "All sides doubled" means **area × 4** and **volume × 8** (→ Mock Q4-21, hexagon with every side doubled). Whenever a problem enlarges a whole figure, square the ratio for area, cube it for volume.

---

## 9. Move an Amount, Then Ratio (invariants)

> 📖 *Source: competition technique (`약점진단/01`); "add to reach a target ratio" mirrors AOPS Prealgebra §7.1, Problem 7.5 (candy jar)*

These problems shift something around and ask for the new ratio (5 of the linked problems). The trick is always the same:

- **Find the invariant — ask "what does NOT change?"**
  - If you only **move** things around → the **total** stays fixed.
  - If you only **add or remove one kind** → the **other kind** stays fixed.
- **Let the fixed part be your anchor.** Give the ratio parts a single variable (like 4x and 1x), write the after-change amounts, match the new given ratio, cross-multiply.

**Worked example.** A box has red : white = 4 : 1. After adding 30 red balls it's 7 : 1. How many white?
- White is untouched → white = w, red starts at 4w. After: (4w + 30) : w = 7 : 1 → 4w + 30 = 7w → 3w = 30 → **w = 10**.

**Worked example (candy — add to hit a target ratio).** A jar has butterscotch : jelly beans = 5 : 2, total 56. You add only jelly beans until the ratio is 2 : 1. How many to add?
- Butterscotch is untouched. 5 + 2 = 7 parts share 56 → 1 part = 8. So butterscotch = 40, jelly = 16.
- Want butterscotch : jelly = 2 : 1, butterscotch fixed at 40 → jelly must become 20. Add **20 − 16 = 4**.

> 💡 **Competition point:** Lock the invariant first, then use one variable for the changing side (→ Mock Q2-25 oil poured P→Q→P; RI 2024 Q14 with two ratio conditions).

---

## 10. Combined Ratio (Chaining)

> 📖 *Source: AOPS Prealgebra §7.2, Problem 7.10 (blots : bleets : blits)*

- **Match the common middle term.** Join A : B = 2 : 3 and B : C = 4 : 5 by making **B equal** in both. LCM(3, 4) = 12 → A : B = 8 : 12 and B : C = 12 : 15 → **A : B : C = 8 : 12 : 15**.

**Worked example (chart method).** blots : bleets = 3 : 4 and bleets : blits = 5 : 6. Find blots : blits.
- Make bleets equal: multiply the first by 5, the second by 4:
  - blots : bleets = 15 : 20, bleets : blits = 20 : 24 → **blots : blits = 15 : 24 = 5 : 8**.

- **Adding property.** If a : b = c : d then also `(a + c) : (b + d) = a : b`.
  - `2 : 3 = 4 : 6` → `(2+4) : (3+6) = 6 : 9 = 2 : 3` ✓.

> 💡 **Competition point:** Chain three or four ratios by lining up shared terms, then read off the whole ratio in one line (→ AP 2025 Q10, four parts summing to 2158).

---

## 11. Rates, Conversions, Direct/Inverse/Joint Proportion

> 📖 *Source: AOPS Prealgebra §7.4 (Conversions), §7.5 (Speed), §7.6 (Other Rates), plus AOPS Volume 1 (proportion / variation section)*

- **Direct proportion (y ∝ x):** the **quotient** is constant, `y/x = k`. Double x → double y.
- **Inverse proportion (y ∝ 1/x):** the **product** is constant, `xy = k`. Double x → halve y.
  - 8 workers finish in 6 days → workers × days = constant → `8 × 6 = 12 × d` → `d = 4` days for 12 workers.
- **Joint proportion:** one quantity depends on two or more at once, e.g. `x ∝ yz` or `x ∝ y/w`. Find `k` from one full data point, then reuse it.
- **Chain rule for equal ratios:** if `a₁/b₁ = a₂/b₂ = a₃/b₃`, each fraction also equals `(a₁+a₂+a₃)/(b₁+b₂+b₃)`.
  - `x/4 = y/6 = z/9` with `x+y+z = 38` → each ratio = `38/(4+6+9) = 2`, so x=8, y=12, z=18.
**Unit conversion — the "conversion factor" idea.** A conversion is just a special ratio. Since 12 inches and 1 foot are the *same length*, we can write `12 inches = 1 foot`, which turns into a fraction equal to 1:

- `(12 inches)/(1 foot) = 1`, and its reciprocal `(1 foot)/(12 inches) = 1` is also valid.

> **Concept:** Think of every conversion factor as a **fraction that equals 1**. Multiplying by 1 never changes the true amount — it only rewrites it in new units.

> **Concept:** **Multiply conversion factors to cancel units.** Arrange each factor so the unit you want to get rid of appears once on top and once on the bottom, then it cancels like a common factor.

- Chaining example: how many inches in a yard? `(12 inches / 1 foot) × (3 feet / 1 yard) = 36 inches / 1 yard` — the "feet" cancel, leaving 36 inches per yard.
- Bigger chain: `1 gallon → tablespoons` (1 gal = 16 cups, 1 cup = 8 oz, 1 tbsp = ½ oz): `1 × (16 cups/1 gal) × (8 oz/1 cup) × (1 tbsp / ½ oz) = 256 tbsp`. Chain as many factors as needed, as long as each equals 1 and units cancel.
- Bigger chain: `45 mi/hr → ft/s`: `45 × (5280 ft / 1 mi) × (1 hr / 3600 s) = 66 ft/s`.
- **Currency is a conversion factor too.** If \$1 = ¥90, then `¥90/\$1 = 1`. Will takes \$1000 to Japan → `\$1000 × (¥90/\$1) = ¥90,000`; converting leftover yen back uses the reciprocal `\$1/¥90`.

**Speed and other rates (a rate is a ratio between two units).**

- **Speed is the ratio of distance to time:** `speed = distance / time`, which rearranges to `distance = speed × time` and `time = distance / speed`. The word **"per"** ("miles *per* hour") literally means "divided by."
  - A car going 110 miles in 2 hours travels `110/2 = 55 mph`; at 70 mph for 2 hours it covers `70 × 2 = 140 miles`.
- **Speed acts like a conversion factor** between time and distance: `2 hours × (70 miles / 1 hour) = 140 miles`.
- **Any "per" quantity is a rate:** typing 40 words/minute, a hose filling 0.5 gallons/second, water's density 8.3 pounds/gallon. Treat them exactly like conversion factors — write the units in and let them cancel.

> ⚠️ **Warning — you cannot just average two speeds.** For a round trip of 50 miles at 75 mph then 50 miles at 50 mph, the average is **NOT** (75+50)/2 = 62.5. You must find the *times*: `50/75 = ⅔ hr` and `50/50 = 1 hr`, total 100 miles in `1⅔ hr` → `100 / (5/3) = 60 mph`. (For equal distances the true average is the **harmonic mean** `2/(1/a + 1/b)`, not the ordinary mean.)

> 💡 **Competition point:** For any "workers/days" or "speed/time" problem, first decide whether the **product** stays constant (inverse) or the **quotient** stays constant (direct) — choosing wrong flips the whole equation. Write the units into your fractions and let them cancel; if the leftover units aren't the ones you want, a factor is upside-down. (Full speed/distance/time problems live in [[10_Distance_Speed_Time]]; work-rate problems in [[11_Work_Percent_Concentration_Profit]].)

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Simplify whole-number ratio | divide by the GCF |
| Simplify fraction ratio | ×LCM of denominators, then reduce |
| Simplify decimal ratio | ×10ⁿ, then reduce |
| Given the total | each part = (its parts)/(total parts) × total |
| Ratio word problem | write a proportion, cross-multiply |
| Same height triangles | area ratio = base ratio |
| Corner triangle, shared vertex | multiply the two side fractions |
| Similar shapes, side ratio 2 : 3 | area 4 : 9, volume 8 : 27 |
| Sides doubled | area × 4, volume × 8 |
| Moving things around | the **total** stays fixed |
| Adding one kind only | the **other kind** stays fixed |
| Chaining ratios | match the common middle term (LCM) |
| Direct proportion | quotient y/x constant |
| Inverse proportion | product xy constant |
| Unit conversion | multiply by fractions equal to 1 |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Side ratio → Area ratio**
- [Mock Q2-4](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_4.png) — rectangle split into 4 parts (areas 65, 35, 49 m²); find the last one
- [Mock Q2-26](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_26.png) — inner triangle DEF = 7; find the area of triangle ABC
- [Mock Q1-26](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_26.png) — interior points give triangle EFG; find its area
- [Mock Q4-15](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_15.png) — trapezium ABCD; find the shaded area
- [Mock Q4-21](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_21.png) — hexagon with every side doubled; find the big hexagon
- [NM 2010 Q25](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/25.png) — triangle BEF area → area of quadrilateral AEFC
- [RI 2023 Q18](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/18.png) — mass points; BD = DE = EC, CF : AC = 1 : 3
- [RI 2024 Q11](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/11.png) — BD = 3/7 of BC, AF = FD; find the shaded area
- [RMO 2025 Q03](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/03.png) — rhombus inside a square; find the area ratio

**② Move/change an amount, then ratio**
- [Mock Q2-25](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_25.png) — oil poured P → Q → P; final ratio 11 : 7
- [Mock Q4-6](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_6.png) — red and white balls; the extra difference is 64
- [Mock Q4-28](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_28.png) — price change gives a new mass ratio m : n
- [RI 2023 Q12](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/12.png) — people move from B to A; the male ratio changes
- [RI 2024 Q14](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/14.png) — marbles moved; two ratio conditions given

**③ Combined ratio (chaining)**
- [RI 2023 Q07](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/07.png) — income 4 : 3, spending 11 : 7, savings equal; find the monthly income
- [AP 2025 Q10](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/10.png) — parts S1 : S2 : S3 : S4 combined; total is 2158

---

## Quick Check

1. In triangle ABC, D is on BC with BD : DC = 3 : 5. What is triangle ABD : triangle ACD?
2. Two similar squares have sides in ratio 3 : 4. What is the ratio of their areas?
3. In triangle ABC, AD : AB = 1 : 3 and AE : AC = 1 : 2. What fraction of triangle ABC is triangle ADE?
4. A : B = 2 : 5 and B : C = 3 : 4. Write A : B : C.
5. A box has red : white = 4 : 1. After adding 30 red balls the ratio is 7 : 1. How many white balls are there?
6. Simplify the ratio `1½ : 2¼`.
7. Prize money \$2400 is split 5 : 4 : 3. How much does the biggest share get?
8. A photo is 4 cm × 6 cm. Enlarged to keep its shape, its area becomes 216 cm². How wide is it now?
9. A car travels 150 miles in 2.5 hours. What is its speed? At that speed, how far in 4 hours?
10. If \$1 = ¥90, how many yen is \$40? (Use a conversion factor.)
11. You drive 60 miles at 30 mph, then the same 60 miles back at 60 mph. What is your average speed for the whole trip? (Careful!)

<details>
<summary>Answers</summary>

1. Same height, so area ratio = base ratio = **3 : 5**
2. Square the side ratio → 3² : 4² = **9 : 16**
3. Share vertex A → multiply: (1/3) × (1/2) = **1/6**
4. Make B the same (LCM of 5 and 3 = 15): A : B = 6 : 15, B : C = 15 : 20 → **6 : 15 : 20**
5. White stays fixed = w, red starts 4w. 4w + 30 = 7w → 3w = 30 → w = **10**
6. `1½ : 2¼ = 3/2 : 9/4` → ×4 → `6 : 9` → **2 : 3**
7. Parts = 5+4+3 = 12; one part = 2400/12 = 200; biggest = 5×200 = **\$1000**
8. width : height = 4 : 6 = 2 : 3. Let width 2x, height 3x → area 6x² = 216 → x² = 36 → x = 6 → width = 2x = **12 cm**
9. speed = 150/2.5 = **60 mph**; distance = 60 × 4 = **240 miles**
10. \$40 × (¥90/\$1) = **¥3600**
11. NOT 45. Time out = 60/30 = 2 hr, time back = 60/60 = 1 hr → 120 miles in 3 hr → average = 120/3 = **40 mph**

</details>

---
*Source map: `약점진단/01_비율활용_세부분석.md`; concepts expanded from AOPS Prealgebra Ch.7 (Ratios, Conversions, Rates). Geometry continues in [[02_Angles_Similarity_Circles]]; the "similar shapes, area from ratio" idea reappears in [[03_Special_Theorems_Coordinates_Solids]]. For the general area-ratio formula on a triangle, look up **Routh's theorem**.*
