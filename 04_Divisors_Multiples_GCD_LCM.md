# 04. Divisors, Multiples, GCD & LCM

> **Unit:** Number Theory Basics (Unit 04 of 14) · **16 linked problems**
> **For:** primary competition students (SMO · NMOS · IMSO) — concepts go up to **Secondary 1** level
> **Why it matters:** This is the base of number theory. If you don't know the "number of divisors" formula and the GCD/LCM rule, half of all number theory problems get stuck.

---

## Lesson Overview
What this note covers:

1. Divisors and Multiples
2. Primes, Composites & Divisibility Rules
3. Prime Factorisation — *Sec 1*
4. Number and Sum of Divisors
5. GCD and LCM — *Sec 1*
6. Euclidean Algorithm — *Sec, advanced*
7. More Tools (extra divisibility & GCD/LCM tricks)

---

## 1. Divisors and Multiples

> 📖 *Source: AOPS Introduction to Number Theory §1.5 "Divisors" and Ch.3 §3.6 (sums & differences of multiples)*

- **Divisor (Factor):** d is a **divisor** of n when n ÷ d is a whole number (no remainder). "Divisor" and "factor" mean the same thing.
  - Example: divisors of 12 → 1, 2, 3, 4, 6, 12 (six of them).
  - Divisors come **in pairs**: 12 = 1×12 = 2×6 = 3×4. Test from the smallest number up and you'll never miss one.
- **Four ways to say the same thing** (for d ≠ 0): "n is a multiple of d" = "n is divisible by d" = "d is a divisor of n" = "d divides n."
- **Multiple:** a number you reach by multiplying. Multiples of 3 → 3, 6, 9, 12, … (never ending).
- **Every integer (except 0) is a divisor of itself** (n = n·1), and **every integer is a divisor of 0** (0 ÷ n = 0).
- **You only need to test 1 up to n** for divisors: a number bigger than n can't divide n (e.g. 0 < 14/36 < 1 means 36 is not a divisor of 14).
- **Divisibility is "transitive":** if a divides b and b divides c, then **a divides c**. (Every divisor of 6 is automatically a divisor of 18, because 6 divides 18.)

**A key competition tool — sums and differences of multiples.** If n divides both a and b, then n divides **a + b** and **a − b**.

- *Why:* write a = xn and b = yn; then a ± b = (x ± y)n, which is n times an integer, hence a multiple of n.
- Restated: **a common divisor of two numbers is also a divisor of their sum and of their difference.** (This one fact powers the Euclidean Algorithm in §6.)

> 💡 **Competition point:** A number with an **odd** number of divisors must be a **perfect square** (36 = 6² → 9 divisors), because only a square has an unpaired divisor (the √). Negative integers can be divisors too (−2 is a divisor of 6), though competition problems usually mean positive ones.

---

## 2. Primes, Composites & Divisibility Rules

> 📖 *Source: AOPS Introduction to Number Theory §2.3 "Identifying Primes" (Sieve of Eratosthenes) and the divisibility-rule sections of Ch.2*

- **Prime:** a natural number (> 1) whose only divisors are 1 and itself (2, 3, 5, 7, 11, 13, …). **Composite:** more than two divisors (4, 6, 8, 9, …). **1 is neither** prime nor composite. **2 is the only even prime.**
- **Sieve of Eratosthenes** (finding all primes up to N): list 2, 3, 4, …, N; circle 2 and cross out every larger multiple of 2; circle the next uncrossed number (3) and cross out its multiples; repeat. Whatever's circled is prime. (Named for Eratosthenes, ~230 BC.)
- **There are infinitely many primes** (Euclid's proof): if there were only finitely many p₁,…,pₙ, then p₁p₂…pₙ + 1 leaves remainder 1 when divided by each pᵢ, so it has a *new* prime divisor — contradiction.

**Divisibility rules:**

- **Divisible by 2:** last digit is **0, 2, 4, 6, 8** (even)
- **Divisible by 3:** the **sum of the digits** is a multiple of 3 (e.g. 123 → 1+2+3 = 6 ✓)
- **Divisible by 4:** the **last two digits** form a multiple of 4
- **Divisible by 5:** last digit is **0 or 5**
- **Divisible by 9:** the sum of the digits is a multiple of **9** (a stronger version of the rule for 3)
- **Divisible by 11:** (sum of odd-position digits) − (sum of even-position digits) is **0 or a multiple of 11** *(Sec)*

> 💡 **Competition point:** Problems like "digit sum is a multiple of 7" (→ AP 2021 Q26 below) start from this idea.

---

## 3. Prime Factorisation — *Sec 1*

> 📖 *Source: AOPS Introduction to Number Theory Ch.4 (Prime Factorization / Fundamental Theorem of Arithmetic)*

- **Definition:** writing a number as a **product of prime numbers only**. Example: 60 = 2² × 3 × 5
- **Method (factor tree):** 60 → 6×10 → (2×3)×(2×5) → 2×2×3×5. However you split it, the **answer is always the same** (this is unique).
- **Index (power) notation (Sec 1):** group the same prime as a power. 2×2×2 = 2³.
- **Why learn it:** it lets you solve steps 4 and 5 below **with a formula**. It is the **starting point of every number theory problem.**

> 💡 **Tip:** When you meet a number theory problem, **start by prime factorising.**

---

## 4. Number and Sum of Divisors

> 📖 *Source: AOPS Introduction to Number Theory Ch.4–5 (Divisors from prime factorization — number & sum of divisors)*

- **Number of divisors formula:** if n = pᵃ × qᵇ × rᶜ, then number of divisors = **(a+1)(b+1)(c+1)**
  - Add **1** to each power, then multiply. (You may use the prime 0 to a times → a+1 choices.)
  - Example: 72 = 2³×3² → (3+1)(2+1) = **12 divisors**
- **Sum of divisors (advanced):** σ(n) = (1+p+…+pᵃ)(1+q+…+qᵇ)…
  - Example: 12 = 2²×3 → (1+2+4)(1+3) = 7×4 = **28**
- **Coprime:** two numbers whose GCD is 1, i.e. they **share no prime factor**.

> 💡 **Competition point:** "9 divisors" → 9 = 3×3 = (2+1)(2+1) → the number is **p²q²**. "Exactly 3 divisors" → a prime squared (4, 9, 25, …).

---

## 5. GCD and LCM — *Sec 1*

> 📖 *Source: AOPS Introduction to Number Theory Ch.3 (Multiples and Divisors — common divisors) & Ch.6 (GCD/LCM from prime factorization)*

- **GCD (Greatest Common Divisor):** the **biggest** shared divisor. From prime factors, take **each shared prime with the smaller power**.
- **LCM (Lowest Common Multiple):** the **smallest** shared multiple. Take **every prime with the larger power**.
- **Example:** 12 = 2²×3, 18 = 2×3² → GCD = 2×3 = **6**, LCM = 2²×3² = **36**
- **Golden formula:** **GCD × LCM = product of the two numbers** → 6×36 = 216 = 12×18 ✓
- **Letting variables (must-know):** if GCD = k, then A = k·a and B = k·b (where a and b are coprime).
  - Then **A + B = k(a+b)** and **LCM = k·a·b** → the condition breaks apart nicely.

> 💡 **Competition point:** When both GCD and LCM are given, **always set A = ka, B = kb** (→ Mock Q2-21: A+B = 2024, LCM = 3795).

---

## 6. Euclidean Algorithm — *Sec, advanced*

> 📖 *Source: AOPS Introduction to Number Theory §3.7 "The Euclidean Algorithm"*

- **Why it works:** a common divisor of two numbers also divides their **difference** (§1). So the pairs (a, b) and (a−b, b) have *exactly the same* common divisors — and therefore the same GCD.
  - **Subtraction form:** gcd(m, n) = gcd(m − n, n) for m > n. Example: gcd(990, 720) = gcd(270, 720) = gcd(270, 450) = gcd(270, 180) = gcd(90, 180) = gcd(90, 90) = **90**.
- **Faster division form:** gcd(a, b) = gcd(b, a mod b) — replace the pair by the **remainder** of dividing the bigger by the smaller, repeat until one is 0.
  - Example: gcd(48, 18) → gcd(18, 12) → gcd(12, 6) → gcd(6, 0) = **6**.
- **Why useful:** it finds the GCD of **large numbers** (too big to prime-factorise) in just a few steps — e.g. gcd(819, 504) without factoring either one.

> 💡 **Competition point:** Word problems that ask for the largest equal-size piece (e.g. two rectangles of area 1086 and 828 sharing an integer width → the width is a common divisor, so the largest is gcd(1086, 828)) are Euclidean-algorithm problems in disguise.

---

## 7. More Tools (extra divisibility & GCD/LCM tricks)

> 📖 *Source: divisibility rules for 7/8/13/etc. and conditional divisor-counting extend AOPS Introduction to Number Theory Ch.2–5; some (fraction GCD/LCM) are standard competition results.*

- **GCD/LCM scaling rule:** if you multiply both numbers by the same n, then GCD(na, nb) = n×GCD(a,b) and LCM(na, nb) = n×LCM(a,b). Spot an obvious common factor **first**, then only prime-factorise the leftover (smaller) numbers.
  - Example: GCD(24, 36) — 24 = 4×6, 36 = 4×9 → GCD = 4×GCD(6,9) = 4×3 = **12**
- **Divisibility by 6:** divisible by 6 exactly when divisible by **both 2 and 3**. This works because 2 and 3 are **coprime**. Careful: 18 is divisible by both 2 and 6, but that does **not** mean it's divisible by 12 — 2 and 6 are **not** coprime (they share the factor 2), so the trick breaks.
- **More last-digits rules:** divisible by **8** → last 3 digits divisible by 8. By **16** → last 4 digits. By **25** → last 2 digits. By **125** → last 3 digits. By **625** → last 4 digits.
- **Divisibility by 7 (advanced trick):** double the last digit, subtract it from the rest of the number, repeat if needed — divisible by 7 iff the result is.
  - Example: is 616 divisible by 7? → 61 − (6×2) = 49 → yes, divisible by 7.
- **Divisibility by 13 (advanced trick):** remove the last digit, subtract **9×** that digit from what's left, repeat if needed.
- **Counting divisors with a condition:** for "even divisors" / "multiples of m" / "perfect square divisors" etc., **factor out** the required piece first, then apply the (power+1) rule to what remains.
  - Example: 72 = 2³×3² → even divisors → factor out one 2, leaving 2²×3² → (2+1)(2+1) = **9 even divisors**
- **Perfect-square divisors:** a divisor is a perfect square only if **every prime's power in it is even**.
- **LCM or GCD — which one?** Things **recurring/coinciding again** (flashing lights, buses meeting, gears lining up) → **LCM** of the cycle lengths. Things being **cut/split into equal pieces** → **GCD**.
- **GCD/LCM of fractions (Sec):** LCM(a/b, c/d) = LCM(a,c) / GCD(b,d), and GCD(a/b, c/d) = GCD(a,c) / LCM(b,d). Same prime-power idea also works for GCD/LCM of **algebraic terms** (treat each variable's exponent like a prime's power).

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Odd number of divisors | perfect square only |
| Only even prime | 2 |
| The number 1 | neither prime nor composite |
| d divides a and b | then d divides a+b and a−b |
| a\|b and b\|c | then a\|c (transitive) |
| Sieve of Eratosthenes | cross out multiples to find primes |
| Number-of-divisors formula | multiply (power + 1) |
| Sum of divisors | (1+p+…+pᵃ)(1+q+…+qᵇ)… |
| 9 divisors | of the form p²q² |
| GCD × LCM | = product of the two numbers |
| GCD/LCM problem | set A = ka, B = kb (a, b coprime) |
| Euclidean algorithm | gcd(m,n) = gcd(m−n, n) |
| "coincide again" / "equal pieces" | LCM / GCD |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Divisors & multiples**
- [NM 2010 Q23](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/23.png) — three-digit X and its reverse Y
- [Mock Q4-29](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_29.png) — three consecutive numbers that are multiples of 4, 7, 9; smallest sum
- [RI 2024 Q16](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/16.png) — 2024 as a sum of n consecutive numbers; largest n
- [AP 2021 Q26](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/26.png) — counting numbers whose digit sum is a multiple of 7
- [AP 2025 Q9](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/09.png) — smallest positive integer whose prime factors sum to 2025

**② GCD / LCM**
- [Mock Q2-21](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_21.png) — A+B = 2024, LCM = 3795; find the larger → *set A = ka, B = kb*
- [AP 2021 Q7](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/07.png) — four different numbers summing to 1111; greatest common divisor

**③ Number of divisors & coprime**
- [RI 2022 Q11](https://dannyahramwoo.github.io/math-quiz/problems/52.%20RI%202022/11.png) — labels 1–1000, using number of divisors
- [AP 2021 Q13](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/13.png) — divisors by 2 or 7 but not both
- [AP 2025 Q5](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/05.png) — 20th special number coprime to the previous sum

---

## Quick Check

1. How many divisors does 48 have?
2. What is the LCM of 24 and 36?
3. Two numbers have product 216 and GCD 6. What is their LCM?
4. Find all two-digit numbers with exactly 3 divisors.
5. Find GCD(60, 36) using the Euclidean algorithm.
6. Both 51 and 34 are multiples of 17. Explain why 51 − 34 = 17 must also be a multiple of 17.
7. How many divisors of 72 are **even**?
8. Is 1 prime? Is 2? Why is 2 special among primes?
9. What is the sum of all divisors of 12?
10. A light flashes every 12 s, another every 18 s. They just flashed together. When do they next flash together?

<details>
<summary>Answers</summary>

1. 48 = 2⁴×3 → (4+1)(1+1) = **10**
2. 24 = 2³×3, 36 = 2²×3² → LCM = 2³×3² = **72**
3. GCD × LCM = product → 216 ÷ 6 = **36**
4. Squares of primes that are two-digit: **25 (5²), 49 (7²)**
5. GCD(60,36)→(36,24)→(24,12)→(12,0) = **12**
6. 51 = 3·17, 34 = 2·17, so 51 − 34 = (3−2)·17 = 17 — a common divisor divides the difference.
7. 72 = 2³×3²; factor out one 2, leaving 2²×3² → (2+1)(2+1) = **9 even divisors**
8. 1 is **not** prime (a prime needs exactly two divisors). 2 **is** prime, and it's the **only even prime**.
9. σ(12) = (1+2+4)(1+3) = 7×4 = **28**
10. LCM(12, 18) = 2²×3² = **36 s**

</details>

---
*Source map: `약점진단/04_약수_배수_GCDLCM.md` · Number theory continues in [[06_Primes_Modular_Factorial]]*
