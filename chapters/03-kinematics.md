# Chapter 3 — Kinematics

**Suggested titles**

1. Kinematics: The Language of Motion
2. Where Position Becomes Velocity Becomes Acceleration
3. Apollo 15 and the Equations of Falling

**TL;DR.** Kinematics is the part of physics that describes motion *without* asking what causes it — that question waits for Chapter 4. This chapter installs the vocabulary (position, displacement, velocity, acceleration), the toolkit (the four kinematic equations of constant acceleration), and the most universal application (objects in free fall). By the end, you can predict where a moving object will be at any future time, given its starting state and its acceleration, with the precision your inputs allow.

---

## A hammer and a feather, August 2, 1971

Astronaut David Scott is standing on the surface of the Moon. It is the final hour of Apollo 15's third moonwalk. He is wearing a white pressure suit, gloves the size of oven mitts, and a boom-mounted camera is trained on his outstretched hands. In one glove he holds a 1.32-kilogram aluminum geological hammer. In the other, a 0.030-kilogram falcon feather donated by the U.S. Air Force Academy.

He looks into the camera and explains the experiment to a television audience back on Earth. "In my left hand, I have a feather; in my right hand, a hammer. I guess one of the reasons we got here today was because of a gentleman named Galileo a long time ago, who made a rather significant discovery about falling objects in gravity fields."

He releases them at the same instant. The feather falls. The hammer falls. They strike the lunar regolith together, four-tenths of a second later. Scott shouts: "How about that! Mr. Galileo was correct in his findings."

This is the Galilean claim made experimentally true. On Earth, air resistance dominates. A feather flutters; a hammer plummets. On the Moon, where there is no atmosphere worth mentioning, the only force on each object is the Moon's gravity, and the Moon's gravity accelerates every object at the same rate — about $1.62 \text{ m/s}^2$, roughly one-sixth of Earth's. Mass does not matter. Shape does not matter. Whatever you drop falls at the same acceleration. The hammer and the feather hit the ground together because *gravity does not care what they are*.

What you have just watched is one full chapter of physics in 1.4 seconds of broadcast television. By the end of this chapter, you will be able to write down the equations that predicted the timing of that drop before Scott pressed record. You will be able to solve the same problem on the Moon, on Mars, on a hypothetical asteroid; you will be able to compute how high a basketball bounces, how long an airplane needs to brake on a runway, how far a thrown rock travels before it hits the ground.

**Learning objectives.** By the end of this chapter you should be able to:

1. Distinguish position, displacement, and distance, and choose the correct one for a given problem.
2. Calculate average and instantaneous velocity, and average and instantaneous acceleration, from position and time data.
3. Apply the four equations of motion under constant acceleration to solve kinematics problems in one dimension.
4. Recognize when an object is in free fall and apply the kinematic equations with $a = -g$ to predict its motion.
5. Read position-time, velocity-time, and acceleration-time graphs, and translate between them.

**Prerequisites.** Chapter 1 (units, significant figures, uncertainty). Algebra, including the quadratic formula. Basic trigonometry helps but is not strictly required for this chapter — Chapter 3 is where vectors and angles come into play.

**Why this chapter matters.** Newton's mechanics (Chapter 4) is built on top of kinematics. So is rotational motion (Chapter 10), oscillation (Chapter 16), and the orbital mechanics of satellites and planets (Chapter 6). Kinematics is the language those chapters speak. Without fluency here, the rest of the course is unreadable.

---

## Concept 1 — Position, displacement, velocity

### A traffic camera over an intersection

A traffic camera mounted above the intersection of King Street and Main is recording for an automated study of traffic flow. At 8:14:03 AM, a sedan crosses into the camera's field of view from the north. At 8:14:07 AM, it crosses out of view, having passed cleanly through the intersection going south. Between those two timestamps, four seconds elapsed; the camera saw a metal box move from one position to another.

That is the entire content of kinematics in one sentence. We had a position; time passed; we had a different position. The job of this concept is to make those words — *position, time, displacement, velocity* — precise enough that we can do arithmetic with them.

### The mechanism — the kinematic vocabulary, defined

**Position** is where an object is, measured along some chosen axis from some chosen origin. We give it the symbol $x$ when the motion is along a horizontal axis, $y$ when vertical. Position has units of length — meters, in SI.

The choice of origin and the choice of positive direction are arbitrary, but you must commit to one before you do any calculation. *"Where is the car?"* has no answer until you pick a coordinate system and say "the car is $30 \text{ m}$ north of the traffic light, with north as positive."

**Displacement** is the change in position. We write it $\Delta x = x - x_0$, where $x_0$ is the initial position and $x$ is the final position, and the Greek letter $\Delta$ ("delta") means "change in." Displacement has units of length and a sign — positive if the object moved in the positive direction, negative if it moved in the negative direction.

**Distance** is the total length of the path traveled, regardless of direction. It is always positive.

These two are the same when motion is one-directional. They differ when motion changes direction. A jogger who runs $400 \text{ m}$ down the street and then $400 \text{ m}$ back has a displacement of $0$ (started and ended in the same place) but a distance of $800 \text{ m}$ (their feet covered that much ground). The distinction matters because some questions are about the geometry of the path and some are about the start-to-end change. Pick the right one.

**Average velocity** is displacement divided by elapsed time:

$$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x - x_0}{t - t_0}.$$

The bar over the $v$ marks it as an average. Velocity has units of length per time — $\text{m/s}$ in SI — and a sign that indicates direction. Negative velocity does not mean "slow"; it means "moving in the negative direction along the chosen axis."

**Average speed** is distance divided by elapsed time, without the sign — speed is the magnitude of velocity. That same jogger had average speed $800 \text{ m} / 600 \text{ s} \approx 1.3 \text{ m/s}$ but average velocity zero. The numerator is different.

**Instantaneous velocity** is the velocity at one specific instant — what your speedometer reads at a single moment. Mathematically, it is the limit of average velocity as the time interval shrinks to zero, written

$$v = \lim_{\Delta t \to 0} \frac{\Delta x}{\Delta t}.$$

The notation is from calculus; the idea is intuitive. As your time window gets smaller, the average velocity over that window gets closer to a definite value — the velocity *right now*.

### The trade-off

The kinematic vocabulary trades **everyday looseness for arithmetic precision.** In casual speech, "speed" and "velocity" are synonyms. In physics they are distinct because the calculations require the distinction. The cost is one extra symbol and a vocabulary discipline. The benefit is that every later equation in the book actually works.

### Worked example — distance vs. displacement

Suppose a runner laps a $400 \text{ m}$ oval track exactly three times.

**Reasoning.** What is her *distance*? Three laps times $400 \text{ m}$ per lap equals $1{,}200 \text{ m}$. Her feet covered that much ground.

What is her *displacement*? She finished where she started — at the start/finish line. Displacement is final position minus initial position, and final equals initial. So $\Delta x = 0$.

If she ran the three laps in $4 \text{ minutes} = 240 \text{ s}$, her average **speed** is $1{,}200 \text{ m} / 240 \text{ s} = 5.0 \text{ m/s}$. Her average **velocity** is $0 \text{ m} / 240 \text{ s} = 0$.

**Sanity check.** Average velocity $= 0$ for a closed loop is correct. The runner's *position* never permanently changed; it just oscillated. Average velocity captures the net effect of motion; speed captures the totality. For a loop, these are different objects.

**The general lesson.** The right question to ask determines the right quantity to compute. *"How fast was she moving on average?"* — speed. *"What was her net displacement per unit time?"* — velocity. Sloppy questions produce sloppy answers; precise questions select precise quantities.

### Common misconceptions

- *"Velocity and speed are the same."* No. Velocity is signed (or vector); speed is unsigned (magnitude only). For one-dimensional motion in one direction they have the same magnitude, but the sign matters as soon as direction can change.
- *"The instantaneous velocity at a turning point is the average of nearby velocities."* No — a more careful idea. At a turning point, instantaneous velocity is exactly zero (the object is momentarily at rest before reversing). Averages over windows that bracket the turning point will be small but nonzero.

↳ **Dig Deeper — Why velocity needs to be defined as a derivative**

*The chapter introduces instantaneous velocity through a limiting process. The cleaner formulation, in calculus, is that instantaneous velocity is the derivative of position with respect to time: $v = dx/dt$. Understanding this calculus framing earlier rather than later pays back across the whole physics curriculum.*

**Prompt:**
> Explain why the instantaneous velocity of an object cannot be defined simply as "displacement over a very short time interval" without taking a formal limit. Give one specific example where the naive definition gives a clearly wrong answer (e.g., for an object whose position is given by $x(t) = t^2$). Then walk me through the formal definition $v = dx/dt$, showing how it gives the correct $v(t) = 2t$ for the example. End with one sentence on why this matters in practice.

**What to do with the output:** Save it. The same logic — define an instantaneous quantity as the derivative of an accumulated one — will recur for acceleration ($a = dv/dt$), force ($F = dp/dt$ for varying mass), and many other places. Lock the pattern in early.

---

## Concept 2 — Acceleration and the kinematic equations

### A 747 on the runway, brakes on full

A Boeing 747 lands at $70.0 \text{ m/s}$ — about $250 \text{ km/h}$, or $156 \text{ mph}$. It has roughly $40$ seconds and roughly $2$ kilometers of runway in which to slow to zero. The pilot deploys the thrust reversers, applies maximum braking, lifts the spoilers. The plane decelerates at about $1.50 \text{ m/s}^2$ — every second, its speed drops by $1.5 \text{ m/s}$.

We have seen *position* and *velocity*. Now we add *acceleration*: the rate at which velocity changes. The 747 is decelerating because its velocity is decreasing in magnitude; the sign convention says that if velocity is positive (forward) and decreasing, acceleration is negative (backward). Some textbooks call the magnitude of negative acceleration "deceleration"; it is more honest to say *acceleration is $-1.50 \text{ m/s}^2$* and to let the sign carry the information.

This concept assembles the four equations of constant acceleration — the workhorse toolkit of intro mechanics. With them, you can answer essentially any one-dimensional kinematics question about an object whose acceleration is constant (or close enough to constant).

### The mechanism — average acceleration and the four kinematic equations

**Average acceleration** is change in velocity divided by elapsed time:

$$\bar{a} = \frac{\Delta v}{\Delta t} = \frac{v - v_0}{t - t_0}.$$

Units are length per time per time — $\text{m/s}^2$ in SI. Like velocity, acceleration is signed. Negative acceleration means *the velocity is becoming more negative* (speeding up if already moving in the negative direction; slowing down if moving in the positive direction).

For the rest of this chapter we make a simplifying assumption that gets us much further than you might expect: we assume **acceleration is constant**. Many real-world problems satisfy this assumption naturally (free fall on the Moon for short distances; a car braking at a steady rate). For problems where acceleration varies, we will often break the motion into segments, each of which has its own constant acceleration.

With that assumption, four equations relate the kinematic quantities. We let $t_0 = 0$ to simplify (so $\Delta t = t$), and use subscript $0$ for initial values:

**Equation 1 — average velocity for constant acceleration:**

$$\bar{v} = \frac{v_0 + v}{2}.$$

This is just the arithmetic mean of the initial and final velocities, which is exactly the right answer when velocity changes linearly in time.

**Equation 2 — position from average velocity:**

$$x = x_0 + \bar{v} \, t.$$

This is the definition of average velocity, solved for $x$. If you know how fast you went on average and for how long, you know how far you got.

**Equation 3 — final velocity from acceleration:**

$$v = v_0 + a t.$$

Direct from the definition of acceleration. After time $t$ at constant acceleration $a$, your velocity has changed by $a t$.

**Equation 4 — position from initial velocity and acceleration:**

$$x = x_0 + v_0 t + \tfrac{1}{2} a t^2.$$

This combines Equations 2 and 3. The first two terms describe motion at constant velocity $v_0$; the third term is the additional displacement contributed by acceleration.

A fifth equation, useful when you need final velocity and don't know elapsed time, follows by eliminating $t$ between Equations 3 and 4:

**Equation 5 — final velocity from displacement:**

$$v^2 = v_0^2 + 2 a (x - x_0).$$

These are the five kinematic equations of constant acceleration. Memorize them. Better — internalize what each one solves for, so you can pick the right one for any problem you face.

### The trade-off

Constant-acceleration kinematics trades **generality for tractability.** The real world has variable acceleration constantly (a car's acceleration depends on its speed, the wind, the road; a falling object's acceleration depends on air drag). The constant-$a$ assumption gives you closed-form algebraic answers; relaxing it requires calculus and often numerical methods. For introductory problems, the assumption is good enough. For aerospace engineering, it isn't — and the techniques for handling variable acceleration build directly on this foundation.

### Worked example — the airplane on the runway

Recall the 747 above: $v_0 = 70.0 \text{ m/s}$, $a = -1.50 \text{ m/s}^2$.

**Question 1.** What is the plane's velocity after $40.0$ seconds of braking?

Apply Equation 3:

$$v = v_0 + a t = 70.0 \text{ m/s} + (-1.50 \text{ m/s}^2)(40.0 \text{ s}) = 70.0 - 60.0 = 10.0 \text{ m/s}.$$

After 40 seconds the plane is still moving at $10 \text{ m/s}$ — about $36 \text{ km/h}$. It has not yet stopped.

**Question 2.** How long until it does stop?

Set $v = 0$ in Equation 3 and solve for $t$:

$$0 = 70.0 + (-1.50) t \implies t = \frac{70.0}{1.50} \approx 46.7 \text{ s}.$$

The plane stops about $7$ seconds after the $40$-second mark.

**Question 3.** How far does the plane travel before stopping?

Apply Equation 5 with $v = 0$, taking $x_0 = 0$:

$$0 = (70.0)^2 + 2(-1.50) x \implies x = \frac{(70.0)^2}{2 \times 1.50} = \frac{4900}{3.00} \approx 1{,}633 \text{ m}.$$

The plane needs about $1.6 \text{ km}$ of runway. With three significant figures of input precision, we report $x = 1.63 \times 10^3 \text{ m}$.

**Sanity check.** A 747 lands at roughly $250 \text{ km/h}$ and uses roughly $1.5$–$2 \text{ km}$ of runway under normal conditions. Our calculation lands inside that range. The answer is in the right ballpark.

**The general lesson.** Pick your kinematic equation based on what you know and what you want. If you have $v_0$, $a$, $t$, and want $v$ — Equation 3. If you have $v_0$, $a$, $v$, and want displacement without using time — Equation 5. The five equations form a complete enough toolkit that, for any constant-acceleration problem, at least one of them gives the answer in one line.

### Common misconceptions

- *"Negative acceleration always means slowing down."* No. Negative acceleration means *acceleration in the negative direction*. If velocity is also negative (object moving in the negative direction), negative acceleration speeds it up (more negative). The relationship between sign of $a$ and sign of $v$ determines whether the object is speeding up or slowing down — not the sign of $a$ alone.
- *"Average velocity is always the average of initial and final velocity."* True only for constant acceleration. If acceleration varies, the average velocity depends on the actual time-history of motion, not just the endpoints.

↳ **Dig Deeper — Why $\frac{1}{2}a t^2$? The geometric origin of the kinematic equations.**

*Equation 4 has a curious factor of $\frac{1}{2}$ multiplying $a t^2$. It's not arbitrary — it has a clean geometric interpretation as the area under a velocity-time graph. Seeing this once makes the equation memorable rather than memorized.*

**Prompt:**
> Walk me through why the displacement of an object under constant acceleration equals $v_0 t + \tfrac{1}{2} a t^2$, by interpreting the $v$-vs-$t$ graph geometrically. Sketch (or describe) the velocity-time graph for an object with initial velocity $v_0$ and constant acceleration $a$. Show that the displacement is the area under that line, decompose the area into a rectangle (height $v_0$, width $t$) plus a triangle (base $t$, height $at$), and explain how this gives the equation. End with a one-sentence explanation of why this geometric reasoning extends to non-constant acceleration via integration.

**What to do with the output:** Save it. Reading equations as graph areas is one of the durable bridges between visual and algebraic physics — useful in this chapter and again in chapters on work-energy (Chapter 7) and impulse-momentum (Chapter 8).

---

## Concept 3 — Free fall

### Galileo at the Tower, Apollo at the Moon

The story is well-known and probably wrong: Galileo, climbing the Leaning Tower of Pisa with two cannonballs of different masses, dropping them simultaneously, watching them strike the ground together, and proving Aristotle wrong about heavy objects falling faster than light ones. Most historians think Galileo did the experiment with rolling balls on inclined planes, in his lab, slowed down enough that he could time them carefully — not in front of a crowd from the Tower. The Tower story is the legend, not the history.

The physics is real either way. **In a vacuum, every object falls at the same acceleration**, regardless of mass. On Earth, that acceleration is approximately

$$g = 9.80 \text{ m/s}^2,$$

directed downward. Strictly, $g$ varies a little — from about $9.78 \text{ m/s}^2$ at the equator to $9.83 \text{ m/s}^2$ at the poles, with smaller corrections for altitude and local geology — but $9.80$ is the standard value we'll use unless a problem says otherwise. On the Moon, $g_{\text{Moon}} \approx 1.62 \text{ m/s}^2$. On Mars, $g_{\text{Mars}} \approx 3.71 \text{ m/s}^2$. These are the local-gravity-only figures; air resistance modifies the picture on Earth and Mars but not on the airless Moon.

What David Scott demonstrated on August 2, 1971 was that *with no air, all objects do fall at the same rate*. The hammer-and-feather experiment was as much a vindication of Galileo (and Newton, who built mechanics on Galileo's insight) as it was good television.

### The mechanism — the kinematic equations applied to free fall

When an object is in free fall — meaning the only force on it is gravity, with air resistance ignored — its acceleration is constant in magnitude ($g$) and directed downward. Set up the coordinate system. If you take *up* as positive, then $a = -g = -9.80 \text{ m/s}^2$ (the acceleration is negative because it points down, opposite to your chosen positive direction). If you take *down* as positive, $a = +g$. Either convention is valid; just pick one and stay with it through the entire problem.

Re-write the kinematic equations with $y$ (vertical) replacing $x$ and $a = -g$:

$$v = v_0 - g t,$$

$$y = y_0 + v_0 t - \tfrac{1}{2} g t^2,$$

$$v^2 = v_0^2 - 2 g (y - y_0).$$

These are not new equations. They are Equations 3, 4, and 5 from Concept 2 with the specific value $a = -g$ substituted in. The reason free fall gets a separate concept section is not new physics; it is that free fall is the most common kinematic scenario in nature and worth practicing thoroughly.

### The trade-off

Free fall as treated here trades **realism for tractability.** Real objects falling through air encounter drag, which depends on speed, shape, and the density of the air. A skydiver in free fall does *not* keep accelerating forever; eventually drag balances gravity and the diver reaches *terminal velocity* (about $55 \text{ m/s}$ for a face-down skydiver in stable position). The free-fall idealization is excellent for short falls of dense objects (a stone, a basketball, a hammer dropped from chest height) and progressively worse for low-density objects (a feather on Earth) or long falls. We use the idealization where it is good and switch tools where it isn't.

### Worked example — a rock thrown upward off a cliff

A person standing on the edge of a cliff throws a rock straight up with initial velocity $v_0 = 13.0 \text{ m/s}$. The rock misses the cliff edge as it falls back down. Take *up* as positive, $y_0 = 0$ at the throwing point.

**Question 1.** Where is the rock at $t = 1.00 \text{ s}$? At $t = 2.00 \text{ s}$? At $t = 3.00 \text{ s}$?

Apply $y = y_0 + v_0 t - \tfrac{1}{2} g t^2$ at each time.

At $t = 1.00 \text{ s}$:

$$y_1 = 0 + (13.0)(1.00) - \tfrac{1}{2}(9.80)(1.00)^2 = 13.0 - 4.90 = 8.10 \text{ m}.$$

At $t = 2.00 \text{ s}$:

$$y_2 = 0 + (13.0)(2.00) - \tfrac{1}{2}(9.80)(2.00)^2 = 26.0 - 19.6 = 6.40 \text{ m}.$$

At $t = 3.00 \text{ s}$:

$$y_3 = 0 + (13.0)(3.00) - \tfrac{1}{2}(9.80)(3.00)^2 = 39.0 - 44.1 = -5.10 \text{ m}.$$

At $t = 1$ second, the rock is $8.10 \text{ m}$ above the throwing point and still rising. At $t = 2$ seconds, it is $6.40 \text{ m}$ above and already on the way back down (it passed through its peak between $t = 1$ and $t = 2$). At $t = 3$ seconds, it is $5.10 \text{ m}$ *below* the throwing point — it has fallen past the cliff edge.

**Question 2.** What is its velocity at each time?

Apply $v = v_0 - g t$:

At $t = 1.00 \text{ s}$: $v = 13.0 - 9.80 = 3.20 \text{ m/s}$ — still going up.

At $t = 2.00 \text{ s}$: $v = 13.0 - 19.6 = -6.60 \text{ m/s}$ — moving downward.

At $t = 3.00 \text{ s}$: $v = 13.0 - 29.4 = -16.4 \text{ m/s}$ — moving downward faster.

**Question 3.** When does the rock momentarily stop at the top of its arc?

At the peak, $v = 0$. Set $v = v_0 - g t = 0$ and solve:

$$t_{\text{peak}} = \frac{v_0}{g} = \frac{13.0}{9.80} \approx 1.33 \text{ s}.$$

The rock peaks at about $t = 1.33$ seconds — between the $t = 1$ and $t = 2$ snapshots, consistent with the position results.

**Sanity check.** A person can throw a rock up at maybe $13 \text{ m/s} \approx 30 \text{ mph}$ (think pitching a baseball, gently). It should peak in a little over a second, which it does. The numbers are physically reasonable.

**The general lesson.** Free-fall problems are a special case of constant-acceleration kinematics — apply the equations, substitute $a = -g$, watch your sign conventions, and the algebra falls out cleanly. The trickiest part is keeping the directions straight, especially when the object reverses direction.

### Common misconceptions

- *"At the peak of its trajectory, the rock's acceleration is zero."* No. Velocity is zero; acceleration is still $-g = -9.80 \text{ m/s}^2$. The rock is still being pulled down by gravity at the peak — that's *why* it starts falling immediately. Acceleration is the rate of change of velocity, and velocity is changing rapidly at the peak (from positive to negative), so acceleration there is large, not zero.
- *"Heavier objects fall faster."* In a vacuum, they do not. In air, they often appear to, but only because air resistance affects light objects more (relative to gravity) than heavy ones. Drop a coin and a piece of paper crumpled into a tight ball from chest height — they reach the floor at nearly the same time, because both are dense enough that air resistance is negligible over a short fall.

↳ **Dig Deeper — Terminal velocity and the limits of free fall**

*The chapter assumes free fall — gravity only, no air resistance. In real applications (skydivers, raindrops, the design of parachutes), air resistance dominates the long-time behavior. The concept of terminal velocity is where the free-fall idealization stops working and the real story takes over.*

**Prompt:**
> Explain the concept of terminal velocity for an object falling through air. Walk through (a) the physical mechanism — drag force balancing gravitational force; (b) the typical terminal velocity for a human skydiver in stable face-down position (cite a specific number); (c) how terminal velocity changes when the diver pulls into a streamlined dive vs. opens a parachute; (d) the kinematic difference between "object in free fall" and "object at terminal velocity" — what's the acceleration in each case? End with one sentence on what shape of object would have the highest terminal velocity.

**What to do with the output:** Save it. The drag-balances-gravity logic returns in fluid dynamics (Chapter 12) and in any engineering problem involving wind loading or air braking.

---

## Synthesis — kinematics as scaffold for everything that follows

Step back. The three concepts of this chapter — vocabulary, equations, free fall — are scaffolding. They describe motion without explaining what causes it. *Why* does the rock decelerate going up and accelerate coming down? *Why* does the airplane brake at $1.50 \text{ m/s}^2$ and not some other rate? *Why* does the Moon's gravity have one-sixth the strength of Earth's? Those questions live in Chapter 4 (forces) and Chapter 6 (gravitation). What this chapter gave you is the descriptive language those later chapters will use.

The pattern is general. In physics, you almost always learn *kinematics first, dynamics second*. Position-velocity-acceleration before forces. Charge-position-current before fields. Particle wavelengths before Schrödinger's equation. The reason: dynamics tells you how things change, but to write that down you need a vocabulary for the change itself. Kinematics is that vocabulary.

There is also a quieter, deeper move you should notice. Each of the four kinematic equations is exact only for constant acceleration. The real world rarely has exactly constant acceleration. But for short enough time intervals, *any* acceleration is approximately constant — over a millisecond of a real situation, $a$ doesn't change much. The kinematic equations, applied piecewise to short intervals, become the basis of every numerical simulation of motion ever written. Open a video game's physics engine, and underneath, the engine is doing kinematic-equation updates thousands of times per second on every moving object. You are about to learn the math that runs the world's video games.

### A worked example using all three concepts — a tossed object's full trajectory

A juggler tosses a ball straight up with $v_0 = 5.00 \text{ m/s}$. She catches it at the same height as where she released it. Using each concept in turn:

**Concept 1 — vocabulary.** The motion is one-dimensional and vertical. Let $y$ be position (up positive) with origin at the release point. Initial position $y_0 = 0$. The displacement from release to catch is $\Delta y = 0$ (same height), but the *distance* the ball traveled is twice the height of its peak.

**Concept 2 — kinematic equations.** The ball is in free fall the whole time except at the moments of release and catch. Apply $y = y_0 + v_0 t - \tfrac{1}{2} g t^2$ with $y = 0$ (returning to start) and solve for $t$:

$$0 = 0 + (5.00) t - \tfrac{1}{2}(9.80) t^2 \implies t (5.00 - 4.90 t) = 0.$$

Two solutions: $t = 0$ (the initial release, trivial) and $t = 5.00 / 4.90 \approx 1.02 \text{ s}$ (the catch). So the ball is in the air for about $1.02$ seconds.

**Concept 3 — free fall structure.** The peak occurs at $t_{\text{peak}} = v_0 / g = 5.00 / 9.80 \approx 0.51 \text{ s}$, which is half the total flight time. The peak height: $y_{\text{peak}} = v_0 t_{\text{peak}} - \tfrac{1}{2} g t_{\text{peak}}^2 = (5.00)(0.51) - \tfrac{1}{2}(9.80)(0.51)^2 \approx 2.55 - 1.27 \approx 1.28 \text{ m}$. The total *distance* traveled by the ball: $2 \times 1.28 = 2.56 \text{ m}$.

The displacement from start to end is zero. The distance is $2.56 \text{ m}$. The flight time is $1.02 \text{ s}$. Three answers, all derived from the same three constant-acceleration kinematic equations applied with $a = -g$.

**Scale shift.** That $1.02$-second juggle is the same physics that, scaled up by a factor of $10^7$, governs the orbit of a satellite around Earth (gravity pulling it inward, momentum pushing it tangentially). The same three equations will not literally describe the orbit — orbital motion is two-dimensional and gravity isn't constant once altitude varies meaningfully — but the *kind* of analysis (define position, identify acceleration, integrate forward in time) is identical. From a juggler's hand to a satellite's orbit, kinematics is the single language.

---

## Exercises

### Warm-up

**2.1** *(LO 1)* A swimmer in a $50 \text{ m}$ pool swims one full lap (down and back) in $42 \text{ s}$. Compute (a) total distance, (b) net displacement, (c) average speed, (d) average velocity.

**2.2** *(LO 2)* A car accelerates from rest to $25 \text{ m/s}$ in $8.0 \text{ s}$. What is its average acceleration?

**2.3** *(LO 3)* A bicyclist initially traveling at $4.0 \text{ m/s}$ accelerates at $0.50 \text{ m/s}^2$ for $6.0 \text{ s}$. What is her final velocity?

**2.4** *(LO 4)* Drop a small dense object (a coin) from rest. How far does it fall in $0.50$ seconds, ignoring air resistance? In $1.0$ seconds?

### Application

**2.5** *(LO 3)* A car traveling at $30.0 \text{ m/s}$ decelerates at $5.0 \text{ m/s}^2$. (a) How far does it travel before stopping? (b) How long does the deceleration take?

**2.6** *(LO 3)* You throw a baseball straight up with initial velocity $20.0 \text{ m/s}$. Compute (a) the time to reach peak height, (b) the peak height, (c) the time at which the ball returns to your hand.

**2.7** *(LO 4)* On the Moon, where $g_{\text{Moon}} = 1.62 \text{ m/s}^2$, you drop a hammer from $1.50 \text{ m}$ above the surface. (a) How long does it take to hit the ground? (b) On Earth (no air), how long would the same drop take? (c) Compare the two times qualitatively — does the Moon time match the rough sense you have from David Scott's Apollo 15 footage?

**2.8** *(LO 5)* The position of a particle is given by $x(t) = 2 t^2 - 5 t + 3$ (in meters, with $t$ in seconds). Compute its velocity and acceleration at $t = 2 \text{ s}$. (Hint: take the derivative if you know calculus; otherwise, compute average velocities over $\Delta t = 0.001 \text{ s}$ centered on $t = 2$.)

### Synthesis

**2.9** *(LO 3, LO 4)* You drop a stone into a vertical well and hear it splash $2.5 \text{ s}$ later. Estimate the depth of the well, ignoring (a) air resistance and (b) the time for the sound to travel back up. Then estimate how much the answer changes if you account for the speed of sound ($340 \text{ m/s}$) in the return travel.

**2.10** *(LO 3, LO 5)* Sketch position-vs-time, velocity-vs-time, and acceleration-vs-time graphs for a ball thrown straight up with initial velocity $10 \text{ m/s}$, caught at the same height $2 \text{ s}$ later. Show all three graphs on the same time axis. Mark the peak.

**2.11** *(LO 3, LO 4)* Two balls are dropped simultaneously from the same height — one a bowling ball, one a Styrofoam ball, both in air. In your everyday experience, which hits the ground first, and roughly by how much? Explain the discrepancy with free-fall theory using one sentence about air resistance and one about typical numerical magnitudes.

### Challenge

**2.12** *(beyond chapter)* A rocket fires its engine for the first $30 \text{ s}$ of vertical flight, producing constant acceleration $a = +20 \text{ m/s}^2$. After $30 \text{ s}$, the engine cuts out and the rocket continues in free fall. Compute (a) the rocket's velocity and altitude at engine cutoff, (b) the additional altitude gained after cutoff before the rocket reaches its peak, (c) the total flight time from launch to splashdown back at the launch altitude. Treat the entire problem with constant-acceleration kinematics in two segments.

**2.13** *(beyond chapter)* In your own words, explain why the four constant-acceleration kinematic equations would *not* correctly describe a freely falling object across the entire range from "released from $1$ km altitude" to "hitting the ground." What physical effect breaks the constant-$a$ assumption, at what altitude does it become significant, and what tool would you reach for to handle it?

---

## LLM Exercise — Chapter 2: Kinematics of Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A kinematic property of your anchor phenomenon — one motion-related quantity (a speed, an acceleration, a stopping distance, a free-fall time) — calculated from inputs and reported with proper units and uncertainty.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste the 1-sentence description from your Chapter 00 / Chapter 1 entry].

For Chapter 2, I want to apply kinematics — position, velocity, acceleration, the equations of constant acceleration, free fall — to one motion-related question about my phenomenon.

Please:

1. Identify ONE motion-related question I can ask about my phenomenon that uses Chapter 2 physics. Be specific. Examples: for a bike commute — what's the average acceleration during a stop at a traffic light? for an espresso machine — at what velocity does water emerge from the portafilter? for a basketball shot — what's the ball's velocity when it leaves my hand?

2. Walk me through which kinematic equation(s) apply. Identify the assumptions (constant acceleration? one dimension? free fall? air resistance ignored?) and flag where each assumption might fail for my real phenomenon.

3. Give me input numbers (sourced or measured). For each: where to get the value, what uncertainty to expect.

4. Solve the equation. Report the answer with proper units and uncertainty (use the percent-addition rule from Chapter 1).

5. One Fermi-style sanity check.

6. One sentence on how this entry will connect to Chapter 4 (forces) when we meet it.

Save the output as logbook/chapter-02-kinematics.md.
```

### What this produces

A second Logbook entry, building on Chapter 1's anchor quantity. By the end of Chapter 2 your Logbook has one foundation document and two physics entries.

### How to adapt this prompt

- *For phenomena involving rotation* (a spinning fan, a record player): replace "kinematics in 1D" with "wait for Chapter 10 — angular kinematics is the better tool." But you can still ask about linear motion of a point on the rotating object as a Chapter 2 exercise.
- *For phenomena involving fluids* (water flow, blood flow): the kinematics equations apply to the fluid speed, but the constant-acceleration assumption usually fails. Use them for an idealized "as-if" calculation and note the gap.
- *For ChatGPT or Gemini:* Identical, with the usual interface substitutions.

### Connection to previous chapters

Builds directly on Chapter 1's anchor quantity. The uncertainty propagation rule from Chapter 1 is applied here.

### Preview of next chapter

Chapter 3 extends kinematics to two dimensions — projectile motion, vectors, components. The Chapter 3 LLM Exercise will ask you to find a 2D motion in your phenomenon (an angled trajectory, a curving path) and analyze it using vector decomposition.

---

## Chapter summary

Kinematics is the mathematical description of motion *without* asking what causes it. Three commitments:

1. **A precise vocabulary** — position, displacement (signed), distance (unsigned), velocity (signed), speed (magnitude), acceleration (signed). The vocabulary distinctions matter because the equations require them.

2. **Five equations of constant acceleration** — two ($\bar{v}$ definitions), three ($v$, $x$, $v^2$). Pick the one that has the variables you know on the right and the variable you want on the left. For any one-dimensional kinematic problem with constant $a$, one equation gives the answer in one line.

3. **Free fall as the universal application** — the kinematic equations with $a = -g \approx -9.80 \text{ m/s}^2$ on Earth. Mass does not affect the acceleration; only the strength of the local gravitational field does.

The one idea that matters most: **acceleration is the rate of change of velocity, just as velocity is the rate of change of position.** Once that derivative-of-derivative structure is internalized, every kinematic equation falls out naturally — and the analogous structures in rotational motion, oscillation, and quantum mechanics become recognizable when you meet them.

The common mistake to watch for: **sign conventions.** Pick a positive direction at the start of the problem and never switch mid-calculation. A negative answer is meaningful — it means *in the negative direction* — not an error.

What you should now be able to teach someone else: how to set up a kinematic problem (pick origin, pick positive direction, identify what's known and what's wanted), how to choose the right equation, and how the apparent universality of free fall (Apollo 15's hammer-and-feather) is a direct prediction of the same equations you used for the airplane on the runway. If you can do that, you've understood this chapter.

---

## What would change my mind

The chapter argues that constant-acceleration kinematics, applied piecewise, is sufficient to describe most one-dimensional motion of interest in introductory physics. The argument would need revision if real-world motion problems where the acceleration varies smoothly (a falling object with quadratic air drag; a vehicle accelerating along a non-uniform power curve) were too poorly approximated by piecewise-constant treatment to be useful pedagogically — they aren't, with sensible time-step choices, but a student attacking a research-grade problem would need to graduate to the variable-$a$ tools.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is the gravitational acceleration the same for every mass?** Newton's law of gravity says force is proportional to mass; Newton's second law says acceleration equals force over mass; the masses cancel and you get a mass-independent acceleration. But why does the same quantity ("mass") appear in both the gravitational law and the inertial law? Einstein's general relativity makes this not a coincidence but a foundational principle (the equivalence principle). We will not resolve this until Chapter 28. Until then, hold the puzzle: gravity treats every object the same, and that fact is one of the deepest in physics.

---

## Connections forward

Chapter 3 extends kinematics from one dimension to two — projectiles, components, the same equations applied along $x$ and $y$ axes simultaneously. Chapter 4 finally tells you *what causes acceleration* — Newton's three laws of motion. Chapter 6 applies kinematics-plus-Newton to circular motion and gravitation. Chapter 10 generalizes everything in this chapter to rotation: position becomes angle, velocity becomes angular velocity, acceleration becomes angular acceleration, and the kinematic equations come back, structurally identical, with new symbols. The pattern this chapter installs — *write the equation of motion, integrate forward in time, sanity-check the result* — is the work of physics, repeated at every later scale.

---

**Tags:** kinematics, free-fall, constant-acceleration, position-velocity-acceleration, Apollo-15

---

## AI Wayback Machine

**Galileo Galilei** worked out the kinematics of falling bodies in the late 16th century — showing that distance scales with the square of time, independent of mass. He performed experiments by rolling balls down inclined planes when free-fall was too fast to measure.

**Run this:**

```
Who was Galileo Galilei, and how does his work on kinematics connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Galileo Galilei"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Galileo's inclined-plane experiment and the math he extracted from it.
- Ask it about Galileo's house arrest after his 1633 trial, and what he wrote during it.

What changes? What gets better? What gets worse?
