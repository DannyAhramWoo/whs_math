# 06. Primes, Modular Arithmetic & Factorials

> **Unit:** Number Theory Basics (Unit 06 of 14) · **11 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Primes are the building blocks of every whole number. Modular arithmetic ("clock maths") lets you find last digits and remainders of gigantic powers without ever computing them. Factorials hide long strings of primes inside them. These three ideas turn "impossible" big-number questions into quick ones.

---

## Lesson Overview
What this note covers:

1. Primes and Composites
2. Special Primes — Mersenne, Fermat, Twin — *Sec, advanced*
3. Modular Arithmetic — *Sec 1*
4. Power Cycles and Last Digits — *Sec 1*
5. Fermat, Euler & CRT — *Sec, advanced*
6. Factorials and the Power of a Prime — *Sec 1*
7. Perfect, Abundant & Deficient Numbers
8. Multiplicative Magic Square
9. More Number-Theory Tools

---

## 1. Primes and Composites

- **Prime:** a whole number greater than 1 with **exactly two divisors** — 1 and itself. Example: 2, 3, 5, 7, 11, …
- **Composite:** a whole number with **more than two divisors** (it splits into smaller factors). Example: 4, 6, 8, 9.
- **The number 1** is neither prime nor composite — it has only *one* divisor. **2** is the only **even** prime; every other even number is divisible by 2.
- **Prime test (must-know):** to check whether *n* is prime, **divide it by every prime up to √n**. If none divides it, *n* is prime.
  - Why only up to √n? If *n = a·b* with *a ≤ b*, then *a ≤ √n*. So if there is any factor at all, the *smaller* one is already ≤ √n — no need to test higher.
  - Example: is 97 prime? √97 ≈ 9.8, so test 2, 3, 5, 7. None divides 97 → **97 is prime**.
- **The 25 primes under 100 (memorise!):** 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97.
- **Fundamental Theorem of Arithmetic:** every whole number greater than 1 is either prime or can be written as a **product of primes in exactly one way** (ignoring order). This is *why* primes are called the building blocks of numbers.

> 💡 **Competition point:** When a problem says "distinct primes" or "always prime", first list the small primes and test the edge cases. Watch out: **any expression that is always a multiple of some fixed number** (other than that number itself) is composite (→ RMO 2025 Q13 below).

---

## 2. Special Primes — Mersenne, Fermat, Twin — *Sec, advanced*

> 📖 *Source: AOPS* Introduction to Number Theory *§6.2 "Some Special Primes" (pp.109–110).*

Mathematicians have studied a few families of primes for centuries.

- **Mersenne primes:** primes of the form **2ᵖ − 1**. Long ago some people believed 2ᵖ − 1 was *always* prime when *p* is prime — but it can fail. Still, this form gives many of the largest primes ever found.
  - Example: 2² − 1 = 3, 2³ − 1 = 7, 2⁵ − 1 = 31 are prime; but 2¹¹ − 1 = 2047 = **23 × 89** is *not*.
- **Fermat primes:** primes of the form **2^(2ⁿ) + 1**. Fermat *conjectured* these are always prime. About a century later **Euler** showed 2^(2⁵) + 1 = 4 294 967 297 = **641 × 6 700 417** is composite. The only Fermat primes known are the five: **3, 5, 17, 257, 65537**.
- **Twin primes:** a pair of primes that **differ by 2**, like 3 & 5, 5 & 7, 11 & 13, 17 & 19, 29 & 31. The **twin prime conjecture** says there are infinitely many such pairs — believed true but never proven.
  - Smallest twin-prime pair greater than 100: **101 and 103** (the first two odd numbers past 100, both prime).

> **Concept:** A **conjecture** is a statement believed true but **not yet proven**. Once it is proven, it becomes a **theorem**. Fermat's "conjecture" about 2^(2ⁿ)+1 was disproved; the twin-prime and Goldbach conjectures are still open.

---

## 3. Modular Arithmetic — *Sec 1*

> 📖 *Source: standard number theory — matches AOPS* Introduction to Number Theory *Ch.12 "Introduction to Modular Arithmetic" (Congruence, Residues, §12.2–12.5). Those pages are absent from our book scan, so this section is written from the standard results.*

- **Idea:** "**mod n**" means **keep only the remainder** after dividing by *n*. Think of a clock: 15 o'clock is really 3 o'clock, so **15 ≡ 3 (mod 12)**.
- **Congruence:** we write **a ≡ b (mod n)** to mean "a and b leave the **same remainder** when divided by n" — equivalently, **n divides (a − b)**.
  - Example: 38 ≡ 2 (mod 12), because 38 − 2 = 36 is a multiple of 12.
- **Residue:** the remainder itself (from 0 to n − 1) is called the **residue** of a mod n.
- **Addition rule:** (a + b) mod n = ((a mod n) + (b mod n)) mod n.
- **Subtraction rule:** (a − b) mod n = ((a mod n) − (b mod n)) mod n.
- **Multiplication rule:** (a × b) mod n = ((a mod n) × (b mod n)) mod n.

> ⚠️ **Warning:** You may take the remainder **at every step** of an addition, subtraction, or multiplication — the numbers never blow up. But you may **not** simply "take the remainder of the exponent"; powers follow the *cycle* rule in Section 4 instead.

> 💡 **Competition point:** Whenever a problem asks for a **remainder** or a **last digit** of something big, switch to mod n immediately and reduce every piece before combining.

---

## 4. Power Cycles and Last Digits — *Sec 1*

> 📖 *Source: standard number theory (units-digit cycles); parallels AOPS* Introduction to Number Theory *Ch.10 "Units Digits" and §12.5 "Multiplication and Exponentiation" — not in our scan.*

- **Powers repeat.** For a fixed base, the values **aᵏ mod n cycle** with a short period.
- **Last digit = mod 10. Last two digits = mod 100.**
- **Units-digit cycles (mod 10) — worth memorising:**
  - 2: 2, 4, 8, 6, 2, … (period **4**)
  - 3: 3, 9, 7, 1, 3, … (period **4**)
  - 7: 7, 9, 3, 1, 7, … (period **4**)
  - 8: 8, 4, 2, 6, 8, … (period **4**)
  - 4: 4, 6, 4, 6, … (period 2) 9: 9, 1, 9, 1, … (period 2)
  - 5 always ends in 5, 6 always ends in 6, and 0/1 stay the same.
- **How to use a cycle:** to find aᵏ, divide the exponent *k* by the period and use the **remainder** to pick the right spot in the cycle.
  - Example (last digit of 3¹⁰⁰): period 4, and 100 = 4 × 25 remainder 0 → the 4th (last) entry of 3's cycle → **1**.
- **Last-two-digit example:** 7ᵏ mod 100 runs 07, 49, 43, 01, then **07 again** → period **4**. So 7²⁰²⁰ = 7^(4×505) ends in **01**.

> 💡 **Competition point:** For "last digit / last two digits of a huge power", find the **cycle length** first, then reduce the exponent by that cycle (→ Mock Q4-33 below).

---

## 5. Fermat, Euler & CRT — *Sec, advanced*

> 📖 *Source: standard number theory. AOPS* Introduction to Number Theory *develops the ingredients across Ch.12 and Ch.14 "Linear Congruences" — those chapters are missing from our scan, so the theorems are stated from standard results.*

- **Euler's phi φ(n):** how many numbers from 1 to *n* are **coprime** to *n* (share no prime factor with n).
  - Example: φ(10) = 4, because 1, 3, 7, 9 are coprime to 10.
  - For a prime *p*, **φ(p) = p − 1** (every smaller number is coprime to a prime).
- **Fermat's little theorem:** if *p* is prime and gcd(a, p) = 1, then **a^(p−1) ≡ 1 (mod p)**.
  - Example: mod 7, 3⁶ ≡ 1, so 3⁶⁰⁰ = (3⁶)¹⁰⁰ ≡ 1 too. Huge exponents collapse instantly.
- **Euler's theorem (the general version):** if gcd(a, n) = 1, then **a^φ(n) ≡ 1 (mod n)**. Fermat's is the special case when n is prime.
- **Chinese Remainder Theorem (CRT):** if you know a number's remainder for several **coprime** moduli (say mod 4 and mod 25), you can **combine them** into a single remainder mod their product (mod 100).
  - This is why mod-100 problems are often split into **mod 4 and mod 25**, solved separately, then glued back.

> 💡 **Competition point:** CRT + Fermat is the "adult" way to do last-two-digit problems. For primary level the **cycle method in Section 4 does the same job** with no theory — use whichever you remember.

---

## 6. Factorials and the Power of a Prime — *Sec 1*

> 📖 *Source: AOPS* Introduction to Number Theory *§6.3 "Factorials, Exponents and Divisibility" (pp.111–114).*

- **Factorial:** *n!* = *n* × (n−1) × … × 2 × 1 — the product of every natural number up to *n*.
  - 1! = 1, 2! = 2, 3! = 6, 4! = 24, 5! = 120, 6! = 720.
- **Recurrence (very useful):** **(n + 1)! = (n + 1) · n!**. So once you know 5! = 120, then 6! = 6 · 120 = 720 with no re-multiplying.
- **Factoring a sum of factorials** — turn a hard sum into a neat product:
  - 5! + 6! = 5! + 6·5! = (1 + 6)·5! = **7 · 5!**. Its largest prime factor is **7** (bigger than any prime inside 5!).

> **Concept:** Many number-theory sums get simpler by **factoring out the common factorial** first, instead of multiplying everything out and adding — exactly what turns 5! + 6! into 7·5!.

- **Power of a prime in n! (Legendre's formula):** the number of times a prime **p** divides *n!* is
  **⌊n/p⌋ + ⌊n/p²⌋ + ⌊n/p³⌋ + …**   (⌊ ⌋ means round down; stop once pᵏ > n).
  - **Why it works** (from the book, for p = 2, n = 30): among 1…30 there are ⌊30/2⌋ = 15 multiples of 2, then ⌊30/4⌋ = 7 that carry a *second* 2, then ⌊30/8⌋ = 3 with a *third*, then ⌊30/16⌋ = 1 with a *fourth*. Total powers of 2 in 30! = **15 + 7 + 3 + 1 = 26**, so 2²⁶ is the highest power of 2 dividing 30!.
  - Power of 3 in 10! = ⌊10/3⌋ + ⌊10/9⌋ = 3 + 1 = **4**.
- **Trailing zeros of n!** = the **power of 5** in n! (there are always more 2s than 5s, so 5 is the bottleneck).
  - Example: 26! → ⌊26/5⌋ + ⌊26/25⌋ = 5 + 1 = **6 trailing zeros**.

> 💡 **Competition point:** "How many zeros at the end of n!?" → **just count the 5s** with Legendre's formula (→ RMO 2025 Q15 below).

---

## 7. Perfect, Abundant & Deficient Numbers

> 📖 *Source: AOPS* Introduction to Number Theory *§6.4 "Perfect, Abundant, and Deficient Numbers" (pp.115–116).*

Let **s(n)** = the **sum of the proper divisors** of *n* (all divisors *except n itself*). We classify *n* by comparing s(n) to n:

- **Perfect:** s(n) = n. Example: s(6) = 1 + 2 + 3 = 6, and s(28) = 1 + 2 + 4 + 7 + 14 = 28. The three smallest perfect numbers are **6, 28, 496**.
- **Abundant:** s(n) > n. The smallest is **12**: s(12) = 1 + 2 + 3 + 4 + 6 = 16 > 12.
- **Deficient:** s(n) < n. **Every prime is deficient**, since s(p) = 1.

> 💡 **Competition point:** To classify a number fast, list its proper divisors and add. Perfect numbers are rare and famous (6, 28, 496, 8128) — recognising them saves time.

---

## 8. Multiplicative Magic Square

- **Product magic square:** every row, column and diagonal has the **same product** (instead of the same sum).
- **Log trick:** take the **logarithm** of every cell → the products become **sums**, so it turns into an ordinary (additive) magic square, which you already know how to solve.
- **3×3 fact:** in a 3×3 product magic square the **centre cube equals the full product** of all nine cells (centre³ = product of all 9). So the centre is the **cube root of the total product**.

> 💡 **Competition point:** For a 3×3 product magic square, multiply all nine numbers, then the centre is the number whose **cube** is that product (→ Mock Q4-26 below).

---

## 9. More Number-Theory Tools

> 📖 *Source: parity/factoring facts — AOPS* Introduction to Number Theory *§6.5 (Palindromes) and standard contest number theory.*

- **Parity of a sum:** the parity (odd/even) of a sum depends **only on how many odd numbers** you add — even terms never change it. **Even count** of odds → sum even; **odd count** of odds → sum odd.
  - Example: a sum of 30 consecutive integers has 15 odd + 15 even terms → 15 (odd count) odds → the **total is odd**.
- **a² − b² = (a − b)(a + b), matched-parity trick:** (a − b) and (a + b) are **always the same parity**. So to solve a² − b² = N, split N into two factors **of the same parity**.
  - Example: a² − b² = 143 = 11 × 13 (both odd) → a − b = 11, a + b = 13 → **a = 12, b = 1**.
- **"Odd sum of primes → one prime is 2":** every prime except 2 is odd. So if a sum of primes is **odd**, exactly **one** of them must be 2.
  - Example: two primes sum to 39 (odd) → one is 2, the other is **37**.
- **Goldbach's conjecture:** every even number > 2 is a sum of two primes — never proven, but useful for "write X as a sum of two primes" questions.
- **Division Algorithm (formal remainder rule):** for integer *a* and positive integer *b*, **a = bq + r** with 0 ≤ r < b (q = quotient, r = remainder). This is "long division" written properly.
- **Same-remainder trick (mini CRT):** if *x* leaves the **same remainder r** for several divisors, then **x − r is a common multiple** of all of them — so *x − r* is a multiple of their **LCM**.
  - Example: x leaves remainder 1 when divided by 2, 3, 4, or 5 → x − 1 is a multiple of LCM(2,3,4,5) = 60 → smallest such x = **61**.
- **Palindromes:** a number reading the same forwards and backwards (434, 13731). Fun fact: **every 2-digit palindrome** (11, 22, …, 99) is a multiple of 11.
- **Calendar problems:** divide the number of days by **7**, then use the remainder to step forward/backward through the days of the week — modular arithmetic in disguise.

> 💡 **Competition point:** "sum of primes is odd" and "a² − b² = N" are two of the fastest tricks in a contest — they turn a *search* into a one-line *factoring* problem.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Prime test | divide by every prime up to √n |
| Only even prime | 2 |
| The number 1 | neither prime nor composite |
| Primes under 100 | there are exactly 25 |
| Fundamental Thm of Arithmetic | one prime factorisation, up to order |
| Mersenne prime | 2ᵖ − 1 (not always prime) |
| Fermat prime | 2^(2ⁿ) + 1 (only 3, 5, 17, 257, 65537 known) |
| Twin primes | differ by 2 (11 & 13); 101 & 103 first past 100 |
| Conjecture vs theorem | believed vs proven |
| a ≡ b (mod n) | n divides (a − b) |
| Mod arithmetic | take the remainder at every step (+, −, ×) |
| Last digit / two digits | mod 10 / mod 100; find the cycle |
| Units-digit cycles | 2,3,7,8 have period 4; 4,9 period 2 |
| φ(p) for a prime | p − 1 |
| Fermat's little theorem | a^(p−1) ≡ 1 (mod p) |
| Euler's theorem | a^φ(n) ≡ 1 (mod n) |
| (n + 1)! | = (n + 1) · n! |
| Sum of factorials | factor out the common factorial (5!+6! = 7·5!) |
| Power of p in n! | ⌊n/p⌋ + ⌊n/p²⌋ + … |
| Trailing zeros of n! | count the 5s (Legendre) |
| s(n) < / = / > n | deficient / perfect / abundant |
| Perfect numbers | 6, 28, 496, 8128 |
| Product magic square | logs → sum square; centre³ = full product |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Primes and composites**
- [Mock Q1-19](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_19.png) — 3P + 7Q = 335 with P + Q a perfect square; find Q − P
- [RI 2023 Q09](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/09.png) — a, b, c, d distinct primes with a condition; find ab + bc + cd + da
- [RMO 2025 Q13](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/13.png) — count triples where 42 − x − y − z is always prime
- [AP 2021 Q17](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/17.png) — smallest n with both 4n+1 and 4n−1 composite
- [AP 2025 Q02](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/02.png) — smallest n so that p² + n is composite for every prime p

**② Modular arithmetic (congruence, cycles)**
- [Mock Q4-33](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_33.png) — difference of 2²⁰²⁰ and 3²⁰²⁰, taken mod 100
- [RMO 2025 Q04](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/04.png) — modular/number problem (see paper)
- [Mock Q2-32](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_32.png) — last two digits of (2¹+1)(2²+1)…(2²⁰¹¹+1)

**③ Factorials**
- [Mock Q2-33](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_33.png) — 26! written out; find A + B + C + D
- [RMO 2025 Q15](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/15.png) — number of trailing zeros of 2025!

**④ Multiplicative magic square**
- [Mock Q4-26](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_26.png) — nine divisors of 1225 in a product magic square; find the centre

---

## Quick Check

1. Is 143 prime? (Hint: test primes up to √143 ≈ 11.9)
2. What is the last digit of 3¹⁰⁰?
3. What are the last two digits of 7²⁰²⁰?
4. How many trailing zeros does 100! have?
5. What is φ(13)?
6. What is 3¹⁰⁰ mod 7? (Hint: Fermat says 3⁶ ≡ 1 mod 7)
7. Write 6! in terms of 5!, then give its value.
8. Is 12 perfect, abundant, or deficient?
9. Factor 6! + 7! and give its largest prime factor.
10. Two primes add up to 45. What are they?

<details>
<summary>Answers</summary>

1. Test 2, 3, 5, 7, 11 → 143 = 11 × 13, so **not prime (composite)**
2. 3's cycle is 3, 9, 7, 1 (period 4); 100 = 4 × 25 → last entry → **1**
3. 7ᵏ mod 100 cycles 07, 49, 43, 01 (period 4); 2020 = 4 × 505 → **01**
4. ⌊100/5⌋ + ⌊100/25⌋ = 20 + 4 = **24 zeros**
5. 13 is prime → φ(13) = 13 − 1 = **12**
6. 100 = 6 × 16 + 4, so 3¹⁰⁰ ≡ 3⁴ = 81 ≡ **4 (mod 7)**
7. 6! = 6 · 5! = 6 · 120 = **720**
8. s(12) = 1 + 2 + 3 + 4 + 6 = 16 > 12 → **abundant**
9. 6! + 7! = 6! + 7·6! = (1 + 7)·6! = 8·6! = 8 · 720 = 5760; largest prime factor comes from 8·6! = 2⁶·3²·5 → largest prime is **5**
10. Odd sum → one prime is 2, the other is **43**

</details>

---
*Source map: `약점진단/06_소수_모듈러_팩토리얼.md`. Book sources tagged per section (AOPS* Introduction to Number Theory *Ch.6). Modular-arithmetic chapters (Ch.12–14) are absent from our book scan, so those sections are written from standard number theory and tagged as such. Number theory continues in [[07_Inclusion_Exclusion]].*
