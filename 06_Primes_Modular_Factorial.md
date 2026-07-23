# 06. Primes, Modular Arithmetic & Factorials

> **Unit:** Number Theory Basics (Unit 06 of 14) · **11 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Primes are the building blocks of every number. Modular arithmetic ("clock maths") lets you find last digits and remainders of huge powers. Factorials hide primes inside them. These three ideas turn "impossible" big-number questions into quick ones.

---

## Lesson Overview
What this note covers:

1. Primes and Composites
2. Euler's phi φ(n) — *Sec, advanced*
3. Modular Arithmetic — *Sec 1*
4. Fermat & CRT — *Sec, advanced*
5. Factorials and Legendre's Formula — *Sec 1*
6. Multiplicative Magic Square

---

## 1. Primes and Composites

- **Prime:** a number with **exactly two divisors**, 1 and itself. Example: 2, 3, 5, 7, 11, …
- **Composite:** a number with **more than two divisors** (it can be split into smaller factors). Example: 4, 6, 8, 9.
- **The number 1** is neither prime nor composite. **2** is the only **even** prime.
- **Prime test (must-know):** to check if n is prime, **divide it by every prime up to √n**. If none divides it, n is prime.
  - Example: is 97 prime? √97 ≈ 9.8, so test 2, 3, 5, 7. None divides 97 → **97 is prime**.
- **The 25 primes under 100 (memorise!):** 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97.

> 💡 **Competition point:** When a problem says "distinct primes" or "always prime", first list the small primes and test the edge cases. Watch out: **any expression that is always a multiple of some fixed number** (except that number itself) is composite (→ RMO 2025 Q13 below).

---

## 2. Euler's phi φ(n) — *Sec, advanced*

- **Euler's phi φ(n):** how many numbers from 1 to n are **coprime** to n (share no prime factor with n).
  - Example: φ(10) = 4, because 1, 3, 7, 9 are coprime to 10.
  - For a prime p, φ(p) = **p − 1** (every smaller number is coprime to a prime).

> 💡 **Competition point:** φ is the "size" you need for Fermat/Euler power tricks below. For primary contests, knowing φ(p) = p − 1 is usually enough.

---

## 3. Modular Arithmetic — *Sec 1*

- **Idea:** "mod n" means **keep only the remainder** after dividing by n. Think of a clock: 15 o'clock is 3 o'clock, so 15 ≡ 3 (mod 12).
- **Addition rule:** (a + b) mod n = ((a mod n) + (b mod n)) mod n.
- **Multiplication rule:** (a × b) mod n = ((a mod n) × (b mod n)) mod n. **You can take the remainder at every step** — the numbers never blow up.
- **Cycles (the power trick):** powers a^k mod n **repeat with a short period**.
  - Example: 7^k mod 100 → 07, 49, 43, 01, then **07 again** → period **4**. So 7^2020 = 7^(4×505) ends in **01**.
- **Last-two-digits = mod 100.** Last digit = mod 10.

> 💡 **Competition point:** For "last two digits of a huge power", work **mod 100** and find the cycle length. Then reduce the exponent by that cycle (→ Mock Q4-33 below).

---

## 4. Fermat & CRT — *Sec, advanced*

- **Fermat's little theorem:** if p is prime and gcd(a, p) = 1, then **a^(p−1) ≡ 1 (mod p)**.
  - Example: mod 7, 3^6 ≡ 1, so 3^600 ≡ 1 too. Big exponents collapse instantly.
- **Chinese Remainder Theorem (CRT):** if you know a number's remainder for **coprime** moduli (say mod 4 and mod 25), you can **combine them** into a single remainder mod their product (mod 100).
  - This is why mod 100 problems are often split into **mod 4 and mod 25**, solved separately, then glued back.

> 💡 **Competition point:** CRT + Fermat is the "adult" way to do last-two-digit problems. For primary level, the **cycle method in Section 3 does the same job** with no theory — use whichever you remember.

---

## 5. Factorials and Legendre's Formula — *Sec 1*

- **Factorial:** n! = n × (n−1) × … × 2 × 1. Example: 5! = 120.
- **Legendre's formula (power of a prime in n!):** the number of times prime **p** divides n! is
  **⌊n/p⌋ + ⌊n/p²⌋ + ⌊n/p³⌋ + …** (⌊ ⌋ means round down).
  - Example: power of 3 in 10! = ⌊10/3⌋ + ⌊10/9⌋ = 3 + 1 = **4**.
- **Trailing zeros of n!** = the **power of 5** in n! (there are always more 2s than 5s, so 5 is the limit).
  - Example: 26! → ⌊26/5⌋ + ⌊26/25⌋ = 5 + 1 = **6 trailing zeros**.

> 💡 **Competition point:** "How many zeros at the end of n!?" → **just count the 5s** with Legendre's formula (→ RMO 2025 Q15 below).

---

## 6. Multiplicative Magic Square

- **Product magic square:** every row, column and diagonal has the **same product** (instead of the same sum).
- **Log trick:** take the **logarithm** of every cell → the products become **sums**, so it turns into an ordinary (additive) magic square.
- **3×3 sum square fact:** the **centre = the average of all nine numbers**. For a product square, the centre = the **9th root of the total product** (equivalently the "middle-sized" balanced value).

> 💡 **Competition point:** For a 3×3 product magic square, the centre is fixed by the nine numbers. Multiply all nine, then the centre is the number whose cube is that product ÷ (centre²)… simplest: **centre³ = full product**, so centre is the cube root (→ Mock Q4-26 below).

---

## 📚 From the Books (extra tricks)

- **Parity invariant:** the parity (odd/even) of a sum depends **only on how many odd numbers** you add — even numbers never change it. An **even count** of odd numbers → sum is **even**; an **odd count** of odd numbers → sum is **odd**.
  - Example: sum of 30 consecutive integers has 15 odd + 15 even terms → 15 (odd count) odds → the **total is odd**.
- **a² − b² = (a−b)(a+b), matched-parity trick:** (a−b) and (a+b) are **always the same parity** (both odd or both even). So to solve a² − b² = N, split N into two factors **of the same parity**.
  - Example: a² − b² = 143 = 11 × 13 (both odd) → a−b=11, a+b=13 → **a = 12, b = 1**.
- **Switch/toggle parity:** if something is flipped cyclically among several objects, a total of N times, use **N mod (number of objects)** to see which objects get one **extra** (odd) flip — those are the ones that end up changed.
- **Twin primes & Goldbach:** twin primes are a pair differing by 2 (like 11 and 13). **Goldbach's Conjecture:** every even number > 2 is the sum of two primes — never proven, but believed true and useful for "write X as a sum of two primes" questions.
- **"Odd sum of primes → one prime is 2" trick:** every prime except 2 is odd. So if a sum of primes is **odd**, exactly **one of them must be 2**.
  - Example: two primes sum to 39 (odd) → one prime is 2, the other is **37**.
- **Division Algorithm (the formal remainder rule):** for integer a and positive integer b, **a = bq + r** with 0 ≤ r < b (q = quotient, r = remainder). This is just "long division" written properly.
- **Same-remainder trick (mini CRT):** if x leaves the **same remainder r** for several divisors, then **x − r is a common multiple** of all of them — so x − r is a multiple of their **LCM**.
  - Example: x leaves remainder 1 when divided by 2, 3, 4, or 5 → x − 1 is a multiple of LCM(2,3,4,5) = 60 → smallest x = **61**.
- **Calendar problems:** divide the number of days by **7**, then use the remainder to count forward/backward through the days of the week.
- **Perfect / abundant / deficient numbers:** let s(n) = sum of n's **proper divisors** (all divisors except n itself). s(n) = n → **perfect** (6: 1+2+3=6). s(n) > n → **abundant** (12: 1+2+3+4+6=16). s(n) < n → **deficient** (every prime is deficient, since s(p) = 1).
- **Palindromes:** a number that reads the same forwards and backwards (like 434 or 13731). Fun fact: **every 2-digit palindrome** (11, 22, …, 99) is a multiple of 11.

> 💡 **Competition point:** "sum of primes is odd" and "a² − b² = N" are two of the fastest tricks to spot in a contest — they turn a search problem into a one-line factoring problem.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Prime test | divide by every prime up to √n |
| Only even prime | 2 |
| The number 1 | neither prime nor composite |
| Primes under 100 | there are exactly 25 |
| φ(p) for a prime | p − 1 |
| Mod arithmetic | take the remainder at every step |
| Last two digits | work mod 100; find the cycle |
| Fermat | a^(p−1) ≡ 1 (mod p) |
| Trailing zeros of n! | count the 5s (Legendre) |
| Power of p in n! | ⌊n/p⌋ + ⌊n/p²⌋ + … |
| Product magic square | take logs → sum square; centre³ = full product |

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
- [Mock Q4-33](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/4_33.png) — difference of 2^2020 and 3^2020, taken mod 100
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
2. What are the last two digits of 7^2020?
3. How many trailing zeros does 100! have?
4. What is φ(13)?
5. What is (3^100) mod 7? (Hint: Fermat says 3^6 ≡ 1 mod 7)

<details>
<summary>Answers</summary>

1. Test 2, 3, 5, 7, 11 → 143 = 11 × 13, so **not prime (composite)**
2. 7^k mod 100 has cycle 07, 49, 43, 01 (period 4); 2020 = 4 × 505 → **01**
3. ⌊100/5⌋ + ⌊100/25⌋ = 20 + 4 = **24 zeros**
4. 13 is prime → φ(13) = 13 − 1 = **12**
5. 100 = 6 × 16 + 4, so 3^100 ≡ 3^4 = 81 ≡ **4 (mod 7)**

</details>

---
*Source map: `약점진단/06_소수_모듈러_팩토리얼.md` · Number theory continues in [[07_Inclusion_Exclusion]]*
