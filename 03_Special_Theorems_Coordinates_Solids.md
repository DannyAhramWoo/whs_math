# 03. Special Theorems, Coordinates & Solids

> **Unit:** Geometry Tools (Unit 03 of 14) · **7 linked problems**
> **For:** primary students — concepts go up to **Secondary 2** level
> **Why it matters:** These are the "special weapons" of geometry. One clever theorem (like the British Flag Theorem), the coordinate method, or good solid-shape thinking can turn a scary problem into a one-line answer.

---

## Lesson Overview
What this note covers:

1. British Flag Theorem
2. Coordinate Geometry — *Sec 1*
3. Solids: Volume, Surface Area & Cross-Section
4. More Tools (Pick's Theorem, nets, Euler's Formula)

---

## 1. British Flag Theorem

> 📖 *Source: standard competition theorem (not in the AOPS core chapters); provable from the Pythagorean theorem in [[02_Angles_Similarity_Circles]] §8.*

- **British Flag Theorem:** take a **rectangle** and any point **P inside** it. Label the corners A, B, C, D in order. Then the two "opposite corner" distance pairs are equal:
  - **PA² + PC² = PB² + PD²**
  - A and C are opposite corners; B and D are the other opposite corners.
  - Example: if PA = 3, PB = 4, PC = 5, then PA² + PC² = 9 + 25 = 34, so PB² + PD² = 34 → 16 + PD² = 34 → PD² = 18 → PD = √18.
- **How to use it:** whenever you see a **rectangle + a point inside + three given distances**, the theorem gives you the **fourth distance instantly**. No hard geometry needed.

> 💡 **Competition point:** The theorem still works even when the point is **outside** the rectangle, and it can hide inside area problems (→ Mock Q5-31 below, where squares are built on the distances).

---

## 2. Coordinate Geometry — *Sec 1*

> 📖 *Source: AOPS Introduction to Algebra Ch.8 (Graphing Lines) — §8.1 (Number Line & Cartesian Plane / distance formula), §8.2 (slope, slope-intercept form), §8.7 Summary (point-slope & standard form, systems of two lines).*

**The plane and a point's coordinates.** The Cartesian plane locates a point by (x, y): x is how far right of the y-axis, y is how far above the x-axis. The little numbers in (x₁, y₁) and (x₂, y₂) are **subscripts** — they tag *which* point each coordinate belongs to.

- **Distance formula:** the distance from (x₁, y₁) to (x₂, y₂) is **√((x₂−x₁)² + (y₂−y₁)²)**.
  - This is **just the Pythagorean theorem**: drop a horizontal and a vertical segment to make a right triangle with legs (x₂−x₁) and (y₂−y₁); the distance is the hypotenuse. So you never need to memorise it separately.
  - Example: from (−3, −5) to (5, 1) → legs 8 and 6 → √(64 + 36) = √100 = **10**. From (0,0) to (3,4) → √(9+16) = **5**.
- **Slope** measures steepness: **m = (y₂−y₁)/(x₂−x₁) = rise/run**.
  - **Positive slope** goes up left-to-right; **negative** goes down. **Slope 0** is horizontal (y₂ = y₁); a **vertical line has undefined slope** (x₂ = x₁, division by zero).
  - A large slope (like 10) is nearly vertical; a slope near 0 (like 1/10) is nearly horizontal.
- **Three ways to write a line** (know all three — problems hand you whichever is convenient):
  - **Slope-intercept form: y = mx + b.** **m** is the slope, **b** the y-coordinate of the y-intercept. Best for reading off the slope.
    - Example: 3x − 5y = 7 → y = (3/5)x − 7/5 → slope = **3/5**, y-intercept (0, −7/5).
  - **Point-slope form: y − y₁ = m(x − x₁).** Best when you know the slope **m** and one point (x₁, y₁) — write it straight down, no solving for b.
    - Example: slope 2 through (3, 1) → y − 1 = 2(x − 3).
  - **Standard form: Ax + By = C** (A, B, C integers, A > 0, no common factor). Every such equation is a straight line, with **slope = −A/B**. Best for grid/intercept work.
- **Quick graphing:** find the **x- and y-intercepts** (set y=0, then x=0), plot those two points, draw the line through them.
- **Parallel & perpendicular:** parallel lines have **equal slopes** (careful: equal slopes could also mean the *same* line); perpendicular lines have slopes whose product is **−1** (each is the negative reciprocal of the other).
- **Two lines / two equations — three outcomes:** solving a pair of linear equations gives either **one solution** (lines cross — different slopes), **no solution** (parallel — same slope, different intercept), or **infinitely many** (the *same* line — same slope *and* intercept). Checking slopes and intercepts tells you which case before you solve.
- **Triangle area (Shoelace formula):** for corners (x₁,y₁), (x₂,y₂), (x₃,y₃), area = **½ × |x₁(y₂−y₃) + x₂(y₃−y₁) + x₃(y₁−y₂)|**. The bars | | mean "take the positive value."

> 💡 **Competition point:** When a shape sits on a grid, **give every corner coordinates** — then distances and areas come from formulas, not guessing (→ AP 2025 Q21). Always be ready to **rearrange an equation into a handier form** (e.g. into y = mx + b to read the slope instantly).

---

## 3. Solids: Volume, Surface Area & Cross-Section

> 📖 *Source: AOPS Introduction to Geometry Ch.14 §14.5 Summary (Prisms, Pyramids, Regular Polyhedra) & Ch.15 §15.5 Summary (Cylinders, Cones, Spheres)*

**Vocabulary first.** A **polyhedron** is a solid with polygon faces. A **prism** has two congruent parallel faces (the **bases**) with parallelograms for the other faces; in a **right prism** those side faces are rectangles. A **pyramid** connects every vertex of a base polygon to a single point (the **apex**) off the plane; its side faces are all triangles, and a **tetrahedron** is a pyramid with a triangular base. **Volume** measures the space inside (how many 1×1×1 blocks fit); **surface area** is the total area of the boundary faces.

**Prisms and boxes:**

- **Prism volume = base area × height** (the distance between the two bases). This one rule covers *every* prism.
- **Cuboid / rectangular box** (dimensions l, w, h): Volume = **lwh**, Surface area = **2(lw + wh + lh)**, **space diagonal = √(l² + w² + h²)**.
- **Cube (edge s):** Volume = **s³**, Surface area = **6s²**, **space diagonal = s√3**.

**Pyramids and cones (the "⅓" family):**

- **Pyramid volume = ⅓ × base area × height.** Lateral surface area of a *regular* pyramid = ½ × slant height × base perimeter.
- **Cone** (a pyramid with a circular base; radius r, height h, slant height l = √(r²+h²)): Volume = **⅓πr²h**, lateral area = **πrl**, total area = **πrl + πr²**.

**Round solids:**

- **Cylinder** (radius r, height h): Volume = **πr²h**, lateral area = **2πrh**, total area = **2πrh + 2πr²**.
- **Sphere** (radius r): Volume = **4πr³/3**, surface area = **4πr²**. **Every cross-section of a sphere is a circle**, and the line from the sphere's center to that circle's center is perpendicular to the cutting plane.

**Net thinking & cross-sections:**

- A **net** is a solid **unfolded flat**. If a path or length wraps around a solid, unfold it first — the shortest path then becomes a **straight line** you can measure with Pythagoras. A cylinder unrolls to a **rectangle**; a cone unrolls to a **sector** (radius = slant height, arc = base circumference).
- A **cross-section** is the flat shape from **slicing** a solid. Slicing a cube can give a square, rectangle, triangle, or even a hexagon.

> **Concept:** **Most 3-D problems are 2-D problems in disguise.** Take a **cross-section through the important points** (for a sphere, one through the center; if it's tangent to something, one through the point of tangency) and your ordinary 2-D tools — above all **building a right triangle for Pythagoras** — solve it.

> 💡 **Competition point:** For an **n×n×n painted cube** cut into unit cubes, sort by how many faces are painted instead of counting one by one: corner cubes (3 faces) = 8, edge cubes (2) = 12(n−2), face-center cubes (1) = 6(n−2)², interior (0) = (n−2)³ (→ RI 2021 Q19). For net problems, mentally **fold the flat shape back up** to test it (→ AP 2021 Q30).

---

## 4. More Tools (grids, nets, polyhedra formulas)

> 📖 *Source: Pick's Theorem & Euler's Formula are standard competition/olympiad results; the 11 nets, Platonic-solid counts, and extra volume/surface-area formulas extend AOPS Introduction to Geometry Ch.14–15.*

- **Pick's Theorem:** for any polygon whose corners all sit on **grid (lattice) points**, Area = **I + B/2 − 1**, where I = number of grid points **strictly inside**, B = number of grid points **on the boundary** (including all 4 corners of a rectangle, not just the corners).
  - Example: a shape with I = 5 interior points and B = 8 boundary points → Area = 5 + 4 − 1 = **8**.
  - Great shortcut for messy grid shapes where the shoelace formula would need many corners.
- **Cube and octahedron nets:** there are exactly **11 different nets** that fold into a cube, and also **11** that fold into an octahedron.
  - To check which points land on top of each other when folded: draw a straight line across two neighbouring squares of the net, from your target point through the fold line between them. Points that are the **same distance** from that crossing point end up meeting at the same corner.
  - Remember: **3 faces meet at every cube corner**, but **4 faces meet at every octahedron corner** — use this to check a folding answer makes sense.
- **Euler's Formula (any convex polyhedron):** **Faces + Vertices = Edges + 2**.
  - Also handy: **Edges = (Faces × sides per face) / 2** (each edge is shared by 2 faces).
  - The 5 Platonic solids (Faces / Vertices / Edges): Tetrahedron 4/4/6, Cube 6/8/12, Octahedron 8/6/12, Dodecahedron 12/20/30, Icosahedron 20/12/30.
- **More surface area formulas:**
  - Cylinder (radius r, height h): S = **2πr² + 2πrh**.
  - Cone (radius r, height h, slant length l = √(r² + h²)): S = **πrl + πr²**.
  - Sphere (radius r): S = **4πr²**.
- **More volume formulas:**
  - Any pyramid: V = **⅓ × base area × height**.
  - Regular tetrahedron (edge s): V = **(√2/12)s³**.
  - Square pyramid with all edges = s: V = **(√2/6)s³**.
  - Frustum of a cone (top radius r, bottom radius R, height h): V = **⅓πh(R² + r² + Rr)**.
- **Similar solids:** if the scale factor between two similar solids is **k**, surface area scales by **k²** and volume scales by **k³** — the 3D partner of "area scales by k²" for flat shapes.
- **Space diagonal (corner to opposite corner through the inside):**
  - Cube (side a): diagonal = **a√3**.
  - Box (length, width, height): diagonal = **√(length² + width² + height²)**.
- **Unrolling trick (shortest path on a curved surface):** to find the shortest crawling distance for an ant on a cylinder or cone, **unroll the curved surface flat** — a cylinder becomes a rectangle, a cone becomes a sector (with radius = slant length and arc length = the base's circumference). Once it's flat, the shortest path is a straight line — just use Pythagoras.
- **Three views & base plans:** a solid built from unit cubes can be described by its **front / top / side views**, or by a **base plan** — a grid seen from above where each cell shows the **stack height** at that spot. These are used to find the minimum (or maximum) number of cubes that fit a given set of views.

> 💡 **Competition point:** For an n×n×n painted cube cut into unit cubes, don't count one by one — use the formulas: **corners (3 faces) = 8** always, **edges (2 faces) = 12(n−2)**, **face cubes (1 face) = 6(n−2)²**, **inside (0 faces) = (n−2)³**. Check they add up to n³.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| British Flag Theorem | PA² + PC² = PB² + PD² (rectangle + inside point) |
| Distance formula | √((dx)² + (dy)²) — it's Pythagoras |
| Slope | m = (y₂−y₁)/(x₂−x₁); horizontal 0, vertical undefined |
| Slope-intercept | y = mx + b (m = slope, b = y-intercept) |
| Point-slope | y − y₁ = m(x − x₁) |
| Standard form | Ax + By = C (slope = −A/B) |
| Two lines: cases | 1 solution / none (parallel) / infinite (same line) |
| Parallel / perpendicular | equal slopes / product = −1 |
| Triangle area (shoelace) | ½ \|x₁(y₂−y₃) + x₂(y₃−y₁) + x₃(y₁−y₂)\| |
| Cube | V = a³, S = 6a², diagonal = a√3 |
| Cuboid | V = abc, S = 2(ab+bc+ca), diag = √(a²+b²+c²) |
| Prism | V = base area × height |
| Pyramid / cone | V = ⅓ × base area × height |
| Cylinder | V = πr²h, S = 2πrh + 2πr² |
| Sphere | V = 4πr³/3, S = 4πr² |
| Similar solids (ratio k) | areas × k², volumes × k³ |
| Painted cube | count 3-, 2-, 1-, 0-face cubes |
| Wrap-around length | unfold the net → straight line |
| Pick's Theorem | Area = I + B/2 − 1 (lattice polygon) |
| Euler's Formula | F + V = E + 2 |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① British Flag Theorem**
- [Mock Q2-34](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_34.png) — a point inside a rectangle; relate PA, PB, PC, PD
- [Mock Q5-31](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_31.png) — square AEFG = 16, triangle BFD = 42; find the area of square ABCD

**② Coordinate geometry**
- [AP 2025 Q21](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/21.png) — a square built on a triangle; find the distance from A to B

**③ Solids (volume, surface area, cross-section)**
- [NM 2010 Q19](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/19.png) — five cubes; find the odd one out
- [Mock Q1-15](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_15.png) — fill a 4×3×5 tank; how many extra 1 cm cubes are needed
- [RI 2021 Q19](https://dannyahramwoo.github.io/math-quiz/problems/51.%20RI%202021/19.png) — a 4×4×4 cube; 37 small cubes have paint → count painted faces
- [AP 2021 Q30](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/30.png) — remove 2 of 8 cells to make a valid cube net

---

## Quick Check

1. In rectangle ABCD, point P is inside with PA = 6, PB = 7, PC = 9. Find PD².
2. Find the distance between the points (1, 2) and (7, 10).
3. A cube has edge length 5 cm. What is its volume, total surface area, and space diagonal?
4. A 3×3×3 cube is painted on all outside faces, then cut into 27 unit cubes. How many unit cubes have **no** paint on them?
5. Two lines are perpendicular. One has slope 2. What is the slope of the other?
6. Write 4x − 2y = 10 in slope-intercept form. What is its slope and y-intercept?
7. A cylinder has radius 3 and height 10. Find its volume (leave π in).
8. A square pyramid has a 6×6 base and height 10. Find its volume.
9. A convex polyhedron has 6 faces and 8 vertices. How many edges does it have?
10. A lattice polygon has 7 interior points and 10 boundary points. Find its area (Pick's Theorem).
11. Write the line through (2, 5) with slope 3 in point-slope form, then convert to slope-intercept form.
12. The lines y = 2x + 1 and y = 2x − 4 — how many points do they share?

<details>
<summary>Answers</summary>

1. PA² + PC² = PB² + PD² → 36 + 81 = 49 + PD² → 117 − 49 = **68**
2. √((7−1)² + (10−2)²) = √(36 + 64) = √100 = **10**
3. Volume = 5³ = **125 cm³**; surface area = 6 × 5² = **150 cm²**; diagonal = 5√3 ≈ **8.66 cm**
4. Only the very centre cube is hidden → **1**
5. slopes multiply to −1 → 2 × m = −1 → m = **−½**
6. −2y = −4x + 10 → y = 2x − 5 → slope = **2**, y-intercept = **(0, −5)**
7. V = πr²h = π·9·10 = **90π**
8. V = ⅓ × base × height = ⅓ × 36 × 10 = **120**
9. Euler: F + V = E + 2 → 6 + 8 = E + 2 → E = **12**
10. Area = I + B/2 − 1 = 7 + 5 − 1 = **11**
11. y − 5 = 3(x − 2); expand → y = 3x − 6 + 5 → **y = 3x − 1**
12. Same slope (2) but different intercepts → parallel → **0 points** (no solution)

</details>

---
*Source map: `약점진단/03_특수정리_좌표_입체.md` · Puzzle-style reasoning continues in [[13_Logic_and_Magic_Squares]]*
