# 10. Distance, Speed & Time

> **Unit:** Rate Word Problems (Unit 10 of 14) · **8 linked problems**
> **For:** primary students — concepts go up to **Secondary 1** level
> **Why it matters:** Almost every competition has a "who meets whom" or "how fast is the train" question. Once you lock in the three-way rule *distance = speed × time* and know how to handle relative speed, these become fast, safe points.

---

## Lesson Overview
What this note covers:

1. The Basic Rule (d = v × t)
2. Average Speed
3. Meeting & Overtaking (Relative Speed)
4. Trains, Bridges & Escalators
5. Streams & Boats — *Sec 1*

---

## 1. The Basic Rule (d = v × t)

> 📖 *Source: AOPS Prealgebra §7.5 "Speed" — speed = distance ÷ time, and the rule that "**per** means divided by".*

- **Distance:** how far you travel. **Speed:** how fast. **Time:** how long.
- **Golden triangle:** **distance = speed × time**. Cover the one you want:
  - speed = distance ÷ time
  - time = distance ÷ speed
  - Example: 90 km/h for 2 h → distance = 90 × 2 = **180 km**.
- **"Per" means "divided by".** "Miles *per* hour" literally means miles ÷ hours. Any units work — km/h, m/s, ft/min — the rule is the same, so **always check your units match** before plugging in. 30 min = **0.5 h**.
- **Speed is a conversion factor between time and distance.** Because 70 km/h means "70 km per 1 h", you can multiply to cancel units: `2 h × (70 km / 1 h) = 140 km`. Writing it this way makes it obvious whether to multiply or divide.
- **Same time, then compare distance:** if two people travel for the **same time**, their distances are in the **same ratio as their speeds**.

> 💡 **Competition point:** When two people set off and meet, they have both travelled for the **same time**. Write both distances as speed × (that same time) — this is the key that unlocks most "when do they meet" problems (→ NM 2010 Q15 below).

---

## 2. Average Speed

> 📖 *Source: AOPS Prealgebra §7.5 "Speed" — average speed = total distance ÷ total time, the "Bogus Solution" trap, and the harmonic-mean Sidenote.*

- **Average speed = total distance ÷ total time.** Never just average the two speeds!
- **⚠️ The book's "Bogus Solution":** for 60 km at 60 km/h then 60 km at 30 km/h, averaging the speeds gives the **wrong** (60+30)/2 = 45 km/h. The **right** way: total 120 km ÷ total 3 h = **40 km/h**. The two answers differ because you spend **more time** at the slower speed, so it counts for more.
- **Round trip, equal distances (must-know):** go at v₁, return at v₂ over the **same distance**. The average is the **harmonic mean**:
  - **average = 2 × v₁ × v₂ ÷ (v₁ + v₂)**
  - Example: 60 km/h out, 40 km/h back → 2×60×40 ÷ 100 = **48 km/h**.
- **Split trip (fractions):** if part of the journey is at one speed and part at another, work out the **time for each part** and add them, then divide total distance by total time.

> 💡 **Competition point:** "First ⅓ of the way at 90 km/h, the rest at 45 km/h" — pick a friendly total distance (like 3 units), find the time for each piece, then use total ÷ total (→ NM 2010 Q24 below).

---

## 3. Meeting & Overtaking (Relative Speed)

> 📖 *Source: AOPS Prealgebra §7.5 "Speed" — relative/closing speed (meeting, chasing, and the circular-track problem). The train-length trap below is also §7.5 (the tunnel exercise).*

- **Relative speed** is how fast the gap between two movers changes.
- **Opposite directions (moving toward each other):** the gap closes at **v₁ + v₂**.
  - Time to meet = starting gap ÷ (v₁ + v₂).
- **Same direction (one chasing / overtaking):** the gap closes at **|v₁ − v₂|** (the difference).
  - Time to catch up = starting gap ÷ (v₁ − v₂).
- **Circular track (the book's example):** two runners on a loop of length L. **Opposite ways** → they meet every L ÷ (v₁ + v₂). **Same way** → the faster one **laps** the slower, gaining a full track L each time, so they meet every L ÷ |v₁ − v₂|.
- **Round-trip meetings:** on a there-and-back path, a mover can turn around at the end and meet the other one again. Track **total distance each has covered** since the start, not just their position.

> 💡 **Competition point:** For a **second meeting** on a round trip, the two together have often covered **3 × the full path** by the second meet (1 path for the first meet, 2 more paths for the second). Compare distances to pin the exact spot (→ RI 2023 Q11 below).

---

## 4. Trains, Bridges & Escalators

> 📖 *Source: the train-length trap (a train clears its own length plus the bridge) is in AOPS Prealgebra §7.5 (the tunnel exercise). Train-overtaking-train and escalators are standard competition extensions, not in Prealgebra.*

- **Train crossing a bridge/tunnel:** the train must clear its **own length too**.
  - **distance travelled = bridge length + train length.**
  - Example: 100 m train, 200 m bridge → the train moves **300 m** from nose-on to tail-off.
- **Train overtaking another train (same direction):** the faster train must cover the **sum of both train lengths** at the **relative speed** |v₁ − v₂|.
- **Escalator (moving stairs):** speeds **add up**.
  - Walking on a moving escalator: **your speed + step speed = total speed** (in steps per second).
  - If you **stand still**, only the escalator moves you. Count the steps and divide by the step speed to get the time.

> 💡 **Competition point:** For "train overtakes train", the distance is **length₁ + length₂** (not just one length) — this is the classic trap (→ Mock Q5-11 below). For escalators, first find the **total number of steps** using a walking case, then answer the standing case (→ Mock Q2-28 below).

---

## 5. Streams & Boats — *Sec 1*

> 📖 *Source: standard competition topic (rate addition/subtraction). Not in Prealgebra §7.5, but it's the same idea as the book's combined-rate work problems in §7.6 — a rate helping (add) or opposing (subtract), just like a faucet-and-drain.*

- **Downstream (going with the current):** the water pushes you → **effective speed = boat + current**.
- **Upstream (going against the current):** the water slows you → **effective speed = boat − current**.
- **Split them apart with two facts:**
  - **boat speed = (downstream + upstream) ÷ 2**
  - **current speed = (downstream − upstream) ÷ 2**
  - Example: down 12 km/h, up 8 km/h → boat = 10, current = **2 km/h**.
- **Same idea for wind:** a plane with a tailwind vs a headwind works exactly the same way.
- **Same idea for any rate:** speed is just a *rate* (something per unit time). The book (Prealgebra §7.6) extends this to **work rates** — a tap filling and a drain emptying add and subtract exactly like boat and current. Those combined-rate problems live in [[11_Work_Percent_Concentration_Profit]].

> 💡 **Competition point:** If the current changes and the **meeting point shifts**, set up the down/up speeds with the current as an unknown, then solve (→ Mock Q1-33 below).

---

## Cheat Sheet

| Idea | Key point |
|------|-----------|
| Basic rule | distance = speed × time |
| "Per" | means "divided by"; speed = a conversion factor |
| Average speed | total distance ÷ total time (never average the two speeds) |
| Circular track, same way | meet every L ÷ \|v₁−v₂\| (lapping) |
| Round trip, equal distance | average = 2·v₁·v₂ ÷ (v₁+v₂) |
| Meeting (opposite ways) | relative speed = v₁ + v₂ |
| Overtaking (same way) | relative speed = \|v₁ − v₂\| |
| Train + bridge | distance = bridge length + train length |
| Train overtakes train | distance = sum of both train lengths |
| Escalator | person speed + step speed |
| Downstream / upstream | boat + current / boat − current |
| Split boat & current | boat = (down+up)/2, current = (down−up)/2 |

---

## 🔗 Linked Competition Problems

These concepts appear in real problems on the quiz app. Learn the idea, then click a problem and try it.

**① Basic (d = v × t)**
- [NM 2010 Q15](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/15.png) — Tom and Harry with rest patterns; find when they meet
- [NM 2010 Q24](https://dannyahramwoo.github.io/math-quiz/problems/02.%20NM%202010/24.png) — first ⅓ at 90 km/h, the rest at 45 km/h; find the average speed
- [RI 2024 Q04](https://dannyahramwoo.github.io/math-quiz/problems/54.%20RI%202024/04.png) — A goes 15% faster, B goes 12 km/h faster, same meeting point
- [RMO 2025 Q16](https://dannyahramwoo.github.io/math-quiz/problems/55.%20RMO%202025/16.png) — Alice's round trip; find when she meets Bob

**② Meeting & overtaking**
- [RI 2023 Q11](https://dannyahramwoo.github.io/math-quiz/problems/53.%20RI%202023/11.png) — Alice and Bob round trips; second meeting is 350 m in → find XY

**③ Train / bridge / escalator**
- [Mock Q5-11](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/5_11.png) — 72 m express overtakes a 108 m local; find the local's speed
- [Mock Q2-28](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/2_28.png) — steps-per-time speed and step count; find the time if standing still

**④ Stream / boat speed**
- [Mock Q1-33](https://dannyahramwoo.github.io/math-quiz/problems/31.%20Mock/1_33.png) — river meeting point changes; find the current speed

---

## Quick Check

1. A car goes 240 km in 3 hours. What is its speed?
2. You drive 30 km at 60 km/h, then 30 km at 20 km/h. What is your average speed?
3. Two people 300 m apart walk toward each other at 3 m/s and 2 m/s. How long until they meet?
4. A 150 m train passes over a 350 m bridge at 20 m/s. How long does it take from nose-on to tail-off?
5. A boat goes 15 km/h downstream and 9 km/h upstream. Find the boat's own speed and the current speed.
6. Two runners on a 400 m circular track go the **same way** at 6 m/s and 4 m/s. How often does the fast one lap the slow one?
7. A cyclist rides for 90 minutes at 16 km/h. Using speed as a conversion factor, how far does she go?

<details>
<summary>Answers</summary>

1. speed = 240 ÷ 3 = **80 km/h**
2. times: 0.5 h + 1.5 h = 2 h for 60 km → 60 ÷ 2 = **30 km/h** (not 40!)
3. relative speed = 3 + 2 = 5 m/s → 300 ÷ 5 = **60 s**
4. distance = 350 + 150 = 500 m → 500 ÷ 20 = **25 s**
5. boat = (15+9)/2 = **12 km/h**, current = (15−9)/2 = **3 km/h**
6. lapping speed = 6 − 4 = 2 m/s → 400 ÷ 2 = **every 200 s**
7. 90 min = 1.5 h; 1.5 h × (16 km / 1 h) = **24 km**

</details>

---
*Source map: `약점진단/10_거리_속도_시간.md` · Rate problems continue in [[11_Work_Percent_Concentration_Profit]]*
