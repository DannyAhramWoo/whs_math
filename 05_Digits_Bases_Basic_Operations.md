# 05. Digits, Bases & Basic Operations

> **Unit:** Number Theory Basics (Unit 05 of 14) · **23 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** So many problems talk about "a 3-digit number" or "swap the digits". If you know how to write digits as letters (abc = 100a+10b+c), these turn from tricky puzzles into simple equations.

---

## Lesson Overview
What this note covers:

1. Letting Digits Be Variables & Bases — *Sec 1*
2. Divisibility by 9 and 11
3. Digit Patterns (numbers written in a row)
4. Basic Operations (fractions, decimals, units, days of week)
5. More Tools (fractions, decimals, exponents, bases)

---

## 1. Letting Digits Be Variables & Bases — *Sec 1*

> 📖 *Source: AOPS Introduction to Number Theory Ch.8 (Base Numbers) — §8.1–8.2 (digit bundles, numerals), §8.4 (base digits), §8.5 (converting between bases)*

**Place value = "digit bundles."** A number's digits are just the coefficients of powers of the base. In base 10, the numeral 3572 *means*
`3·10³ + 5·10² + 7·10¹ + 2·10⁰` — four "digit bundles" of sizes 1000, 100, 10, 1 added together. (A **numeral** is the symbol we write; the **number** is the amount it stands for.)

- **Write a number by its digits:** a 3-digit number with digits a, b, c means **abc = 100a + 10b + c**.
  - Example: 375 = 100×3 + 10×7 + 5.
  - A 4-digit number: **abcd = 1000a + 100b + 10c + d**.
- **Swap the two end digits (abc → cba):** the difference is always **99(c − a)** — the middle digit never matters.
  - Example: 375 − 573 = 99(3−5) = −198.
- **Swap tens and units (abc → acb):** the difference is always **9(c − b)**.

**Bases — bundling in a different size.** A **base number system** groups quantities into powers of the base instead of powers of 10. In **base n**, each place is worth ×n instead of ×10, and you may use only the digits 0 … (n−1). When you collect n of one bundle, you carry it up to the next place — e.g. in base 3, `5·3² = 1·3³ + 2·3²`.

- **Base b → base 10:** add up the decimal value of every digit bundle.
  - `514₉ = 5·9² + 1·9¹ + 4·9⁰ = 405 + 9 + 4 = 418`.
  - `234₅ = 2·25 + 3·5 + 4 = 69`.
- **Base 10 → base b:** repeatedly divide by b; the remainders, read **bottom-to-top**, are the digits.
  - `65 → base 3`: 65÷3 = 21 r2, 21÷3 = 7 r0, 7÷3 = 2 r1, 2÷3 = 0 r2 → **2102₃** (keep the 0!).
- **Bases above 10 need extra digit symbols.** In base 12 we use A for ten and B for eleven, so `1B7₁₂ = 1·144 + 11·12 + 7 = 283`.
- **Base names worth knowing:** base 2 *binary*, 3 *ternary*, 8 *octal*, 12 *duodecimal*, 16 *hexadecimal*, 60 *sexagesimal*.

> 💡 **Competition point:** When a problem says "reverse the digits" or "move the first digit to the end," **write the number with letters first** (a·place-value form). It becomes an equation you can solve (→ Mock Q1-12, Mock Q5-25). For base problems, always fall back on the digit-bundle meaning: a base-b numeral is just a sum of `digit × bⁿ`.

---

## 2. Divisibility by 9 and 11

> 📖 *Source: AOPS Introduction to Number Theory Ch.7 (Divisibility Rules — the "digit sum" rules for 3 and 9, the alternating-sum rule for 11)*

- **Multiple of 9:** a number is a multiple of 9 exactly when its **digit sum is a multiple of 9**.
  - Example: 738 → 7+3+8 = 18 → multiple of 9 ✓
- **Multiple of 11:** take (sum of digits in **odd** positions) − (sum of digits in **even** positions). If that is **0 or a multiple of 11**, the number is a multiple of 11.
  - Example: 2354 → (2+5) − (3+4) = 0 → multiple of 11 ✓
- **Finding an unknown digit:** if a number with a missing digit must be a multiple of 9 (or 11), set up the digit-sum condition and solve for that one digit.

> 💡 **Competition point:** "Digit sum equals 12" or "largest prime you can make" problems (→ NM 2010 Q29, Mock Q2-19) all start from these digit-sum rules.

---

## 3. Digit Patterns (numbers written in a row)

> 📖 *Source: standard competition counting technique (group by digit-length); the "how many digits does each range use" idea underlies AOPS Introduction to Number Theory palindrome/digit problems (Ch.8).*

- **Count digits by how many digits each number has:**
  - 1–9 → **9 numbers × 1 digit = 9 digits**
  - 10–99 → **90 numbers × 2 digits = 180 digits**
  - 100–999 → **900 numbers × 3 digits = 2700 digits**
- **Find the N-th digit:** keep subtracting these totals until you land in the right group. That tells you **which number** you are inside, and then **which digit** of that number.
  - Example: the 15th digit of "123456789101112..." → first 9 digits are 1–9, so digit 15 is the 6th digit into the 2-digit numbers → 10,11,12 → "1 0 1 1 1 2" → the 6th of these is **2**.

> 💡 **Competition point:** Always split by digit-length first. Never count one by one (→ RMO 2025 Q01, Mock Q5-35).

---

## 4. Basic Operations (fractions, decimals, units, days of week)

> 📖 *Source: AOPS Prealgebra Ch.6 §6.5 Summary (decimals, terminating vs repeating), Ch.6.33 (scientific notation); day-of-week is a standard mod-7 technique.*

- **Fractions:** to add or subtract, make a **common denominator** first, then add the tops. Always **simplify** at the end. A mixed number like 2⅓ = improper fraction 7/3.
- **Decimals:** a decimal is just base 10 extended past the point. **Line up the decimal points** before adding or subtracting. Multiplying or dividing by a power of 10 only **moves the decimal point** (×10 moves it one place right, ÷10 one place left).
- **Terminating vs repeating (know this rule):** a fraction in lowest terms is a **finite (terminating) decimal** exactly when its denominator's only prime factors are **2 and/or 5**; any other prime factor forces an **infinite repeating** decimal.
  - `n/9 = 0.n̄` (the digit n repeats): 7/9 = 0.777…. A famous special case: **0.9̄ = 1** exactly.
- **Scientific notation:** write a number as `a·10ᵇ` with `1 ≤ a < 10`. `38100 = 3.81·10⁴`, `0.025 = 2.5·10⁻²`. Multiply by adding exponents, then fix `a` back into range: `(3·10⁵)(4·10⁶) = 12·10¹¹ = 1.2·10¹²`.
- **Unit change:** 1 hour = 60 min, 1 min = 60 sec; 1 m = 100 cm. Convert everything to the **same unit** before comparing.
- **Day of the week:** days repeat every **7**, so use **mod 7**. If today is Thursday, then 7, 14, … days later are all Thursday; 100 days later = 100 mod 7 = 2 → Saturday.

> 💡 **Competition point:** For "what day of the week" problems, count the total days and take the remainder mod 7 (→ AP 2025 Q04). For a long chain of fractions, look for terms that **cancel** or **telescope** (→ RI 2023 Q01, RI 2024 Q05).

---

## 5. More Tools (fractions, decimals, exponents, bases)

> 📖 *Source: AOPS Prealgebra Ch.6 §6.5 Summary (terminating vs repeating decimals, repeating-decimal → fraction), Ch.2 (exponent laws); base conversion from AOPS Introduction to Number Theory §8.5.*

- **Comparing fractions without a common denominator:** cross-multiply — for a/b vs c/d, compare a×d vs b×c (bigger product wins). Or compare each fraction to a nearby "nice" benchmark like 1/3 or 1/2.
  - Example: order 5/19, 7/21, 9/23 → 7/21 = 1/3 exactly; 5/19 < 1/3; 9/23 > 1/3. So **5/19 < 7/21 < 9/23**, no common denominator needed.
- **Continued fractions:** expressions like 1/(1+1/(1+1/(1+1/2))) are worked out from the **innermost term outward**.
- **Unit-fraction inequalities:** e.g. 1/2+1/5+1/8 > 1/x+1/6+1/8 → cancel the shared terms, isolate 1/x, then remember: taking **reciprocals flips the inequality**.
- **Repeating decimal → fraction:**
  - one repeating digit → digit/9 (0.777... = 7/9)
  - two repeating digits → digits/99
  - non-repeating part + repeating part → (whole digit string − non-repeating part) ÷ (a 9 for each repeating digit, then a 0 for each non-repeating digit)
  - Example: 0.7245... (72 fixed, 45 repeats) → (7245−72)/9900 = 7173/9900 = **797/1100**.
- **Terminating vs repeating decimals:** a fraction in lowest terms terminates only if its denominator's prime factors are just 2s and/or 5s — otherwise it repeats forever. Number of decimal places = the **larger** of the powers of 2 or 5 in the denominator.
- **Exponent laws:** aᵐ×aⁿ=aᵐ⁺ⁿ, aᵐ÷aⁿ=aᵐ⁻ⁿ, (aᵐ)ⁿ=aᵐⁿ, aⁿ×bⁿ=(ab)ⁿ, a⁻ⁿ=1/aⁿ, a⁰=1 (a≠0).
- **Decimal → base n:** divide by n repeatedly and read the remainders **last to first**.
  - Example: 65 to base 3 → 65÷3=21 R2, 21÷3=7 R0, 7÷3=2 R1, 2÷3=0 R2 → reading bottom-up: **65 = 2102 in base 3** (don't drop the 0!).
- **×base shifts digits left** — appending a zero, just like ×10 does in base 10.
- **Trailing zeros in base b:** a number ends in k zeros in base b exactly when bᵏ divides it. Factor b into primes to see how many zeros are possible.

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Digit bundles | 3572 = 3·10³+5·10²+7·10¹+2·10⁰ |
| 3-digit number | abc = 100a + 10b + c |
| Reverse end digits | difference = 99(c − a) |
| Swap tens & units | difference = 9(c − b) |
| Base b → base 10 | add up digit×bⁿ |
| Base 10 → base b | divide by b, read remainders bottom-up |
| Bases > 10 | A = 10, B = 11, … as single digits |
| Multiple of 9 | digit sum is a multiple of 9 |
| Multiple of 11 | (odd places) − (even places) = multiple of 11 |
| Digits in a row | 1–9: 9, 10–99: 180, 100–999: 2700 |
| Terminating decimal | denominator's only primes are 2 and/or 5 |
| n/9 | = 0.n̄ ; and 0.9̄ = 1 |
| Scientific notation | a·10ᵇ with 1 ≤ a < 10 |
| Day of week | use mod 7 |
| Chain of fractions | look for cancelling / telescoping terms |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Letting digits be variables & bases**
- [Mock Q1-12](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_12.png) — a 4-digit number where 2×(abcd) + 1000 = dcba
- [Mock Q2-23](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_23.png) — a 3-digit number meeting two digit conditions
- [Mock Q2-31](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_31.png) — six 3-digit numbers in arithmetic progression; smallest possible sum
- [Mock Q5-25](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_25.png) — moving the first digit to the end makes it 4707 bigger; smallest such number
- [RI 2021 Q14](https://dannyahramwoo.github.io/math-quiz/problems/51.%20RI%202021/14.png) — list palindromes from 11 upward; find the 661st digit
- [RMO 2025 Q12](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/12.png) — a 3-digit number whose tens digit is the average of the other two
- [AP 2021 Q20](https://dannyahramwoo.github.io/math-quiz/problems/56.%20AP%202021/20.png) — 7n has 2021 digits; units digit of the smallest such n
- [AP 2025 Q14](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/14.png) — count x where x/3 and 3x are both 5-digit numbers
- [AP 2025 Q27](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/27.png) — after some digit transforms the result equals the original 4-digit number
- [AP 2025 Q30](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/30.png) — 4-digit ABCD = (AB + CD)²; sum of all such numbers

**② Divisibility by 9 and 11**
- [NM 2010 Q29](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/29.png) — dates in 2010 whose digits add up to 12
- [Mock Q2-19](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_19.png) — use each of 1–9 once; largest prime in a group
- [Mock Q2-35](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_35.png) — rows sorted by digit sum; find the position of 9799

**③ Digit patterns (numbers written in a row)**
- [Mock Q5-35](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_35.png) — write 1–100 in a row, group by 3; max − min difference
- [RMO 2025 Q01](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/01.png) — the n-th integer repeats n times; find the 2025th digit

**④ Basic operations (fractions, decimals, units, days of week)**
- [Mock Q2-12](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_12.png) — integer part of 1 ÷ (1/2016 + … + 1/2011)
- [Mock Q5-8](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_8.png) — sharing $480 among Sandra, Hans, Joe; Hans' first amount
- [RI 2021 Q11](https://dannyahramwoo.github.io/math-quiz/problems/51.%20RI%202021/11.png) — sum of 1/Σ terms
- [RI 2023 Q01](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/01.png) — smallest n with sum of 1/[k(k+1)] greater than 1823/2023
- [RI 2024 Q05](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/05.png) — 1/(2²−1) + … + 1/(2024²−1); digit sums of numerator and denominator
- [RI 2024 Q10](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/10.png) — rearrange a double sum into integer sums
- [NM 2008 Q02](https://dannyahramwoo.github.io/math-quiz/problems/01.%20NM%202008/02.png) — running 12 hours a day; days to print $864000 worth
- [AP 2025 Q04](https://dannyahramwoo.github.io/math-quiz/problems/60.%20AP%202025/04.png) — Feb 29 2024 is a Thursday; next leap-year Feb 29 that is also Thursday

---

## Quick Check

1. Write the 3-digit number with digits a=4, b=0, c=7 in the form 100a+10b+c. What is its value?
2. The number 673 has its end digits swapped to make 376. What is 673 − 376, and does 99(c−a) give the same answer?
3. Convert 143 in base 5 into base 10.
4. Is 8291 a multiple of 11? Use the odd−even position rule.
5. If today is Thursday, what day of the week is it 100 days from now?
6. Convert the decimal number 65 into base 3.
7. Does 7/40 terminate or repeat as a decimal? Why?
8. Does 5/12 terminate or repeat? Why?
9. Write 0.9̄ (0.999…) as a fraction.
10. Write 48000 in scientific notation.

<details>
<summary>Answers</summary>

1. 100×4 + 10×0 + 7 = **407**
2. 673 − 376 = **297**; 99(c−a) = 99(3−6) = 99×(−3) = −297, same size ✓
3. 1×25 + 4×5 + 3 = **48**
4. (8+9) − (2+1) = 14, not 0 or a multiple of 11 → **not a multiple of 11**
5. 100 ÷ 7 = 14 remainder 2 → 2 days after Thursday = **Saturday**
6. 65÷3=21 r2, 21÷3=7 r0, 7÷3=2 r1, 2÷3=0 r2 → read up → **2102₃**
7. 40 = 2³×5 → only primes 2 and 5 → **terminates** (7/40 = 0.175)
8. 12 = 2²×3 → has the prime 3 → **repeats** (5/12 = 0.41666…)
9. **1** (0.9̄ = 1 exactly)
10. 48000 = **4.8 × 10⁴**

</details>

---
*Source map: `약점진단/05_자릿수_진법_기초연산.md` · Number theory continues in [[06_Primes_Modular_Factorial]]*
