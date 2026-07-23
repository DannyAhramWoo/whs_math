# 02. Angles, Similarity & Circles (Plane Geometry)

> **Unit:** Plane Geometry (Unit 02 of 14) · **21 linked problems**
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** Plane geometry is where the hardest "figure" questions live. If you can chase angles, spot similar triangles, and use the circle rules, you can crack most shape problems without guessing.

---

## Lesson Overview
What this note covers:

1. What an Angle Is, and Measuring It
2. Angle Chasing (straight, vertical, supplementary, complementary)
3. Parallel Lines Cut by a Transversal
4. Angles in a Triangle (the 180° rule)
5. Exterior Angles (and the 360° result)
6. Congruence, Similarity & Triangle/Quadrilateral Properties — *Sec 1*
7. Circle Properties — *Sec 2*
8. Pythagoras, Special Triangles & Area Cutting — *Sec 1*
9. More Tools (triangle centers, Ptolemy, special quads, sectors) — *advanced*

---

## 1. What an Angle Is, and Measuring It

> 📖 *Source: AOPS Introduction to Geometry §2.1 "What is an Angle?", §2.2 "Measuring Angles"*

- **Angle:** two rays sharing a common origin. The shared origin is the **vertex**; the two rays are the **sides**.
  - We write ∠XOY with the **vertex in the middle** (∠XOY or ∠YOX, but never ∠XYO). When only one angle can be meant, just ∠O.
  - When two lines cross at P, "∠P" is ambiguous — you must name three points (∠APC, ∠BPC, …) to say *which* angle.
- **Measuring — degrees.** A full circle is **360°**; a half-circle (**semicircle**) is 180°. A protractor is a semicircle split into 180 equal degrees.
- **The "fraction of a circle" view (very useful).** An angle's measure = the fraction of a full circle it cuts off, times 360°.
  - ¼ of a circle = 90°, ⅓ = 120°, 1/12 = 30°, 1/8 = 45°.

> 💡 **Competition point:** The "fraction of a circle" idea turns pie-chart / clock / pizza-slice problems into a one-line calculation: (fraction) × 360°. A clock's hour marks are `360°/12 = 30°` apart.

---

## 2. Angle Chasing (straight, vertical, supplementary, complementary)

> 📖 *Source: AOPS Introduction to Geometry §2.3 "Straight and Vertical Angles"*

- **Straight angle:** a straight line is an angle of **180°** (it cuts off exactly half a circle).
- **Supplementary angles:** two angles that add to **180°**. Any two adjacent angles on a straight line are supplementary.
  - Example: if two angles sit on a line and one is 55°, the other is `180° − 55° = 125°`.
- **Complementary angles:** two angles that add to **90°**.
- **Vertical (opposite) angles are equal.** When two lines cross, the angles directly across from each other are equal.
  - *Why (proof):* ∠MPN = 180° − ∠NPO (straight line), and ∠LPO = 180° − ∠NPO (straight line), so ∠MPN = ∠LPO. The proof never used the actual number — vertical angles are *always* equal.

> **Concept:** When you can't compute the target angle directly, **find whatever angles you can first** — a straight line or a crossing point almost always hands you one, and that unlocks the rest.

> ⚠️ **Warning:** An *example* is not a *proof*. Checking one case (e.g. "when it's 72° it works") does not prove a statement always holds.

---

## 3. Parallel Lines Cut by a Transversal

> 📖 *Source: AOPS Introduction to Geometry §2.4 "Parallel Lines"*

- **Parallel lines** never meet; we write AB ∥ CD. Little arrows on the lines mark them parallel.
- When a **transversal** (crossing line) cuts two parallel lines, all **8 angles fall into just two sizes**:
  - a group of **four equal angles**, and another group of **four equal angles**, and the two group-sizes are **supplementary** (add to 180°).
- So every pair is either **equal** or **supplementary** — that's all you really need. (The formal names — corresponding, alternate interior/exterior, co-interior — are nice to know but not worth memorising; just see which angles match and which sum to 180°.)

**Worked example.** m ∥ n, one angle marked 113°. Every angle equals **113°** or its supplement **67°** (`180° − 113°`). Pick each angle's size by whether it's in the same group as the 113° or the other group.

> 💡 **Competition point:** The instant you see parallel lines, copy the one known angle to **every** matching position in the figure (equal) and mark the supplements (180° − it). Angle problems collapse once every angle is labelled.

---

## 4. Angles in a Triangle (the 180° rule)

> 📖 *Source: AOPS Introduction to Geometry §2.5 "Angles in a Triangle"*

- **The three interior angles of any triangle add to 180°.** This is one of the most-used facts in all of geometry.
  - *Why (proof sketch):* through vertex A draw a line parallel to BC. The two "extra" angles it makes equal ∠B and ∠C (alternate angles), and together with ∠A they form a straight angle → ∠A + ∠B + ∠C = 180°.
- **Turning words into equations.** Most triangle word problems: name the unknown angles with a variable, write "they sum to 180°," solve.
  - Example: one angle is twice another, the third is 54°. Let the small one be x, the other 2x → `54° + x + 2x = 180°` → x = 42°. Angles are 42°, 54°, 84°; smallest = **42°**.

> **Concept:** Seeing "180°" should make you look for a **useful line** — often a parallel line, because parallel lines hand out equal angles. That's the trick behind the proof above.

> ⚠️ **Warning:** Your *last* step should always be to check you answered the actual question asked (here: the *smallest* angle, not just x).

---

## 5. Exterior Angles (and the 360° result)

> 📖 *Source: AOPS Introduction to Geometry §2.6 "Exterior Angles"*

- **Exterior angle** = the angle formed by extending one side of a triangle past a vertex.
- **Exterior Angle Theorem:** an exterior angle equals the **sum of the two non-adjacent (far) interior angles**.
  - *Why:* at vertex C, interior ∠ACB and exterior x sit on a straight line, so `∠ACB + x = 180°`; but also `∠A + ∠B + ∠ACB = 180°`, so `x = ∠A + ∠B`.
  - Example: interior angles 35° and 79° → the far exterior angle is `35° + 79° = 114°`.
- **Beautiful result — the three exterior angles of a triangle add to 360°.**
  - Each exterior angle = sum of its two far interior angles, so x + y + z = 2(∠A + ∠B + ∠C) = 2(180°) = **360°**. (This generalises: the exterior angles of *any* convex polygon sum to 360°.)

> 💡 **Competition point:** The exterior-angle theorem lets you skip a step — read the far angle directly as a sum instead of computing the interior angle first (→ RI 2024 Q20: sum the 5 tip angles of a star by chasing exterior angles).

- **Isosceles triangle:** if two sides are equal, the **two base angles are equal** (and vice versa) — a constant source of "hidden" equal angles.

---

## 6. Congruence, Similarity & Triangle/Quadrilateral Properties — *Sec 1*

> 📖 *Source: AOPS Introduction to Geometry Ch.3 (Congruent Triangles, §3.8 Summary) & Ch.5 (Similar Triangles); "same base / same altitude" area idea from Ch.4*

**Congruent = exactly the same.** Two figures are **congruent** if you can slide, spin, and/or flip one to land exactly on the other. For triangles, four tests prove congruence:

- **SSS** — three sides equal.
- **SAS** — two sides and the angle *between* them equal.
- **ASA** — two angles and the side *between* them equal.
- **AAS** — two angles and a *non-included* side equal.
- **CPCTC** — once triangles are congruent, **C**orresponding **P**arts of **C**ongruent **T**riangles are **C**ongruent: every matching side and angle is equal. This is how one congruence unlocks many equal lengths/angles.

> ⚠️ **Warning — the SSA trap:** SSA (two sides + a non-included angle) is **NOT** a valid congruence test. The same three measurements can give two different triangles (this is the "ambiguous case" — e.g. AB = 13, BC = 10, ∠A = 40° has *two* possible triangles).

**Isosceles & equilateral (a constant source of equal angles):**

- **Isosceles:** if two sides are equal, the two **base angles** are equal — and the converse: equal base angles force equal sides. (AB = AC ⟺ ∠B = ∠C.)
- **Equilateral:** all three sides equal ⟺ all three angles equal ⟺ every angle is **60°**.
- *Trick:* dropping a segment from the apex of an isosceles triangle to the midpoint of the base splits it into two congruent right triangles — instant symmetry.

**Similar = same shape, scaled size.** Matching angles are equal and matching sides share one ratio **k** (the scale factor). Three tests:

- **AA** — two angles equal (the one you'll use most; the third angle is then automatic).
- **SAS similarity** — two sides in the same ratio with the included angle equal.
- **SSS similarity** — all three sides in the same constant ratio.
  - Example: △ABC with sides 7, 4, 5 and △DEF with sides 14, 8, 10 → every side doubles, so AB/DE = AC/DF = BC/EF = 1/2 → △ABC ~ △DEF, and therefore ∠A=∠D, ∠B=∠E, ∠C=∠F.

- **Scale factor k → area k², volume k³.** Side ratio k means perimeters in ratio k, **areas in ratio k²**, volumes in ratio k³.
  - Sides ×2 → area ×4, volume ×8.

**Area shortcuts (very competition-relevant):**

- **Same height → area ratio = base ratio.** Two triangles with equal heights compare by their bases alone.
- **Same base and same height → equal area**, even if the shapes look different (a triangle "slides" its apex along a line parallel to the base without changing area).
- **Midpoint theorem:** the segment joining midpoints of two sides is **half the third side** and **parallel** to it.
- **Parallelogram:** opposite sides equal; diagonals **bisect each other**.
- **Trapezium area:** (top + bottom) × height ÷ 2.

> 💡 **Competition point:** To compare two areas, hunt for **similar triangles** (use the k² rule) or **shared height/base** — never measure. Proving a small congruence with SSS/SAS/ASA/AAS, then applying CPCTC, is the workhorse for "show these two lengths are equal" problems (→ RI 2022 Q02: from a parallelogram's area, find triangle ABC).

---

## 7. Circle Properties — *Sec 2*

> 📖 *Source: AOPS Introduction to Geometry §11.4 (Circle basics), Ch.12 §12.6 Summary (Circles and Angles) & Ch.13 §13.3 Summary (Power of a Point)*

**Vocabulary.** A **circle** is all points a fixed distance (the **radius** r) from a fixed **center**. A **chord** joins two points on the circle; a **diameter** is a chord through the center (length 2r). A **secant** is a line hitting the circle at two points; a **tangent** touches at exactly one point. An **arc** is a piece of the circle; a **central angle** (vertex at the center) equals the measure of the arc it cuts off.

**The angle rules (this is the whole chapter in one place).** Where an angle's vertex sits decides the rule:

- **Vertex ON the circle — inscribed angle = half its arc.** An angle formed by two chords from a point on the circle equals **half the arc it cuts off**: ∠PQR = (arc PR)/2.
  - **Consequence 1:** any angle inscribed in a **semicircle is 90°** (Thales — the arc is a full semicircle = 180°, half is 90°).
  - **Consequence 2:** two angles inscribed in (standing on) the **same arc are equal**.
  - **Consequence 3:** a **central angle is twice** any inscribed angle on the same arc.
- **Vertex INSIDE — average of the two arcs.** Two chords crossing inside the circle make an angle equal to **half the sum** of the two arcs they cut off: ∠ = (arc₁ + arc₂)/2.
- **Vertex OUTSIDE — half the difference.** Two secants (or a tangent + secant, or two tangents) meeting outside make an angle equal to **half the difference** of the far and near arcs: ∠ = (far arc − near arc)/2.
- **Tangent–chord angle:** an angle between a tangent and a chord at the point of tangency = **half the intercepted arc**.

**Tangent & radius facts:**

- A tangent is **perpendicular to the radius** drawn to the point of tangency (and the converse: a line through a circle point perpendicular to that radius must be tangent). "Draw the radius to a tangent point" is a reflex move.
- From an outside point you can draw **two tangent segments, and they're equal in length**.

**Cyclic quadrilateral:** if all 4 corners lie on a circle, **opposite angles add to 180°**.

**Power of a Point (Sec 2, advanced but very useful).** For any line through a point P meeting the circle at U and V, the product **(PU)(PV) is constant** — the "power" of P.

- **P inside** (two chords cross at X): (XA)(XB) = (XC)(XD).
- **P outside** (two secants): (PB)(PA) = (PD)(PC) — *the same outside point P must appear in every segment.*
- **Tangent from outside:** (tangent PT)² = (PB)(PA) for any secant through P.

> ⚠️ **Warning:** In the outside-point version, the shared point must be in *all four* segments. Writing (BC)(BA) = (DC)(DE) is wrong; the correct pairing keeps C common: (CD)(CE) = (CB)(CA).

> 💡 **Competition point:** When a circle appears, **draw radii to every key point** and hunt for a right angle (tangent) or a diameter (Thales) — those right angles unlock everything. If a segment **stops in the middle of a circle**, extend it to the circle and reach for Power of a Point (→ AP 2021 Q10: area of a circle around 7 unit squares; AP 2021 Q24: two perpendicular chords).

---

## 8. Pythagoras, Special Triangles & Area Cutting — *Sec 1*

> 📖 *Source: AOPS Introduction to Geometry §6.2 (Two Special Right Triangles), §6.3 (Pythagorean Triples), §6.5★ (Heron's Formula), §6.7 Summary, and Ch.10 §10.3 (Triangle Inequality)*

- **Pythagoras' theorem:** in a **right-angled triangle**, **a² + b² = c²**, where **c is the hypotenuse** (longest side, opposite the right angle).
- **Pythagorean triples (memorise!):** whole-number sides that fit a²+b²=c² — **3-4-5**, **5-12-13**, **8-15-17**, **7-24-25**. Any multiple works too (6-8-10, 9-12-15). Spotting one skips all calculation.
  - Legs 3 and 4 → hypotenuse **5**, no working. (Note {1,2,3} is *not* a triple — you can't make the third from the other two.)

**Two special right triangles (know the side ratios cold):**

- **45-45-90 (isosceles right):** the two legs are equal and the **hypotenuse = leg × √2**. (Proof: leg² + leg² = 2·leg² = hyp².)
  - Leg 5 → hypotenuse 5√2. Hypotenuse 6 → each leg 6/√2 = 3√2.
- **30-60-90:** sides are in ratio **1 : √3 : 2** (short leg : long leg : hypotenuse). The short leg faces the 30° angle, the long leg faces 60°, the hypotenuse faces 90°.
  - Hypotenuse 12 with a 30° angle → short leg 6, long leg 6√3.
  - *These come from cutting an equilateral triangle in half with an altitude* — which is also how you derive the **equilateral-triangle area = (√3/4)·s²**.

> 💡 **Competition point:** The instant you see a **30°, 60°, 120°, or 45°** angle in a figure, look for a hidden 30-60-90 or 45-45-90 triangle — you can then read off the sides with no trig.

**Heron's Formula (area from three sides, no height needed):**

- **[ABC] = √(s(s−a)(s−b)(s−c))**, where **s = (a+b+c)/2** is the semiperimeter.
  - Example: sides 13, 14, 15 → s = 21 → area = √(21·8·7·6) = √7056 = **84**.
- Derived by dropping an altitude and applying Pythagoras twice — the reason the area is fixed once you fix all three sides (SSS congruence).

**Triangle Inequality (when three lengths can even form a triangle):**

- Each side must be **less than the sum** of the other two: a+b>c, a+c>b, b+c>a. (Equivalently, each side is **greater than the difference** of the other two.)
  - Sides 7 and 13 → the third side x must satisfy **6 < x < 20**.

**Area cutting:** split a complex shape into simple **triangles and rectangles**, then add or subtract their areas.

> 💡 **Competition point:** For a shaded region, think "**whole minus holes**" — compute one big easy area, subtract the unwanted pieces. When paper is **folded**, the two layers are **congruent**, handing you hidden equal lengths — set up a Pythagoras equation on the crease (→ Mock Q1-27: fold so A lands on C).

---

## 9. More Tools (advanced / competition extras)

> 📖 *Source: AOPS Introduction to Geometry Ch.7 (Special Parts of a Triangle — centers), Ch.8 (Quadrilaterals), Ch.9 (Polygons), Ch.11 (sector area), plus standard competition results (Ptolemy). These go beyond the core chapters above.*

- **Right-triangle congruence shortcuts:** besides SSS/SAS/ASA/AAS, right triangles also have **HL** (hypotenuse + one leg) and **LL** (two legs).
- **Four triangle centers** (Ch.7):
  - **Centroid** — the three **medians** meet here, cutting each median **2:1** from the vertex; splits the triangle into **6 equal-area** pieces.
  - **Incenter** — the three **angle bisectors** meet here, equidistant from the 3 *sides* (center of the incircle, radius r). **Area = r × s** (s = semiperimeter).
  - **Circumcenter** — the three **perpendicular bisectors** meet here, equidistant from the 3 *vertices* (center of the circumcircle, radius R). For a **right triangle**, the circumcenter is the **midpoint of the hypotenuse**, so **R = ½ · hypotenuse**.
  - **Orthocenter** — where the three **altitudes** meet.
- **Angle Bisector Theorem:** if AD bisects ∠A (D on BC), then **AB/BD = AC/DC** — the bisector splits the opposite side in the ratio of the two adjacent sides.
- **Altitude-to-hypotenuse (right triangle):** the altitude from the right angle to the hypotenuse at D gives three "geometric mean" facts: **BD² = AD·DC**, **AB² = AD·AC**, **CB² = CD·CA**.
- **Ptolemy's Theorem** (cyclic quadrilateral ABCD): **AC · BD = AB·CD + AD·BC**.
- **Incircle/circumcircle radii:** **r = Area/s**; for a right triangle **r = (leg₁ + leg₂ − hypotenuse)/2**; and **R = abc/(4·Area)**.
- **Special quadrilaterals** (Ch.8):
  - **Rhombus:** area = (d₁ × d₂)/2, diagonals perpendicular.
  - **Isosceles trapezoid:** base angles equal in pairs, legs equal, diagonals equal (any one forces the others).
  - **Trapezoid median** (midpoints of the legs): parallel to both bases, **median = (base₁+base₂)/2**, **Area = height × median**.
  - **Kite:** two pairs of *consecutive* equal sides; diagonals perpendicular.
  > 💡 **Competition point:** for true/false "is every rhombus a rectangle?" traps, remember **square ⊂ rectangle ⊂ parallelogram** and **square ⊂ rhombus ⊂ parallelogram** — a rhombus is a rectangle only if it's a square.
- **Sector formulas** (Ch.11): arc length = (angle/360) × 2πr, sector area = (angle/360) × πr².
- **Regular polygons** (Ch.9): hexagon area = 6 × (√3/4) × side², long diagonal = 2 × side; octagon area = 2(1+√2) × side².
- **Belt/rope around touching circles:** total length = straight tangent parts (each = sum of the two radii it touches) + curved arcs, and **the curved parts always sum to exactly one full circle**, no matter how many circles.
- **Symmetry:** a regular n-gon has n lines of symmetry and **rotational symmetry angle = 360°/n**.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Exterior angle | = sum of two far interior angles |
| 3 exterior angles | sum to 360° (any convex polygon) |
| n-gon angle sum | (n−2)×180° |
| Parallel lines | every angle equals it or its supplement |
| Vertical angles | always equal |
| Congruence tests | SSS, SAS, ASA, AAS (SSA is NOT one) |
| Similarity tests | AA, SAS, SSS; area ratio = k², volume = k³ |
| Same height triangles | area ratio = base ratio |
| Midpoint segment | half the third side, parallel |
| Parallelogram diagonals | bisect each other |
| Inscribed angle (vertex on) | = half its arc; semicircle → 90° |
| Angle vertex inside | = half the SUM of the two arcs |
| Angle vertex outside | = half the DIFFERENCE of the arcs |
| Tangent | ⊥ radius at the touch point |
| Two tangents from a point | equal length |
| Power of a Point | (PU)(PV) constant; tangent² = (PB)(PA) |
| Cyclic quadrilateral | opposite angles add to 180° |
| Pythagoras | a² + b² = c² (c = hypotenuse) |
| 45-45-90 | hypotenuse = leg·√2 |
| 30-60-90 | sides 1 : √3 : 2 |
| Heron | Area = √(s(s−a)(s−b)(s−c)), s=(a+b+c)/2 |
| Triangle inequality | each side < sum of other two |
| Centroid | medians meet, 2:1 from vertex |
| Shaded area | whole minus holes |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Angle chasing (exterior/interior/parallel)**
- [Mock Q4-18](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_18.png) — after 9 o'clock, when the hour & minute hands are symmetric about 12
- [Mock Q4-24](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_24.png) — a rectangle built from 6 squares; find angle ABC
- [RI 2022 Q07](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/07.png) — two parallelograms with AC = AD = CF; find angle ECD
- [RI 2024 Q20](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/20.png) — a star shape; find the sum of angles C+D+E+F+G

**② Similarity & triangle/quadrilateral properties**
- [RI 2022 Q02](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/02.png) — from a parallelogram area, find the area of triangle ABC
- [Mock Q1-10](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_10.png) — a hexagon and pentagon joined; find angle BAC
- [Mock Q2-14](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_14.png) — count the triangles in an octagon figure
- [RI 2023 Q14](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/14.png) — overlap area is 578; find length AF
- [AP 2025 Q28](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/28.png) — a regular 12-gon; count the obtuse triangles
- [Mock Q4-34](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_34.png) — BE + BF = 49; find the smallest area of triangle DEF
- [Mock Q5-14](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_14.png) — a staircase cut into a square; find ratio AB : BC
- [Mock Q2-15](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_15.png) — a rectangle split into small squares; find the perimeter

**③ Circle properties**
- [RI 2022 Q14](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/14.png) — digit sum of a fraction-sum expression
- [RI 2022 Q19](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/19.png) — two cyclists on a circular track meeting; find the track length
- [RI 2023 Q08](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/08.png) — a circle rolling inside a square; find the area it covers
- [AP 2021 Q10](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/10.png) — 7 unit squares; find the area of the circle around them
- [AP 2021 Q24](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/24.png) — two perpendicular chords; find the area difference of the 4 regions

**④ Pythagoras & area cutting**
- [Mock Q1-27](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_27.png) — fold the paper so A lands on C; find EF
- [Mock Q1-16](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_16.png) — from two triangle areas, find the area ADOE
- [RI 2023 Q15](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/15.png) — three squares of sides 3, 5, 8; find the diagonal shaded area
- [AP 2025 Q06](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/06.png) — two shaded triangles inside a square

---

## Quick Check

1. A triangle has interior angles 55° and 65°. What is the exterior angle at the third corner?
2. What is the total of all interior angles in a hexagon (6 sides)?
3. Two triangles are similar with side ratio 3. What is their area ratio? Their volume ratio if they were solids?
4. A right triangle has legs 5 and 12. How long is the hypotenuse?
5. In a circle, an inscribed angle on an arc is 40°. What is the central angle on the same arc?
6. An isosceles right triangle has legs of length 7. How long is the hypotenuse?
7. In a 30-60-90 triangle the hypotenuse is 10. Find the two legs.
8. Can 4, 5, and 10 be the sides of a triangle?
9. Find the area of a triangle with sides 5, 5, 6 (use Heron, or split it).
10. Why must the three exterior angles of any triangle add to 360°?
11. From a point P outside a circle, a tangent has length 6 and a secant hits the circle at distances 4 and x from P. Find x.

<details>
<summary>Answers</summary>

1. 55° + 65° = **120°**
2. (6−2)×180° = **720°**
3. area = 3² = **9**; volume = 3³ = **27**
4. 5-12-13 triple → **13**
5. 2 × 40° = **80°**
6. hypotenuse = leg·√2 = **7√2**
7. short leg (opposite 30°) = 10/2 = **5**, long leg = 5√3 → legs are **5 and 5√3**
8. Need 4 + 5 > 10? No (9 < 10). **Not a triangle.**
9. s = 8, area = √(8·3·3·2) = √144 = **12**. (Check: base 6, height 4 → ½·6·4 = 12 ✓)
10. Each exterior angle = sum of its two far interior angles, so the three add to 2(∠A+∠B+∠C) = 2·180° = **360°**.
11. Power of a Point: tangent² = (near)(far) → 6² = 4·x → 36 = 4x → **x = 9**.

</details>

---
*Source map: `약점진단/02_각도_닮음_원.md` · Plane geometry continues in [[03_Special_Theorems_Coordinates_Solids]]*
