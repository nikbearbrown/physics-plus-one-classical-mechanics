# Chapter 12 — Statics and Torque

**Suggested titles**

1. Statics and Torque
2. Why Bridges Don't Fall
3. The Two Conditions for Standing Still

**TL;DR.** Statics is the physics of *not moving* — and it turns out to require not one but two conditions: total force on the system must be zero (no translational acceleration), *and* total torque about any point must be zero (no rotational acceleration). This chapter installs torque ($\tau = r F \sin\theta$), shows how the two equilibrium conditions combine to determine forces in real structures (a beam, a ladder, a forearm holding a weight), and introduces simple machines (lever, pulley) as torque-trade systems.

---

## A bridge over the Tagus, 1998

The Vasco da Gama Bridge, just outside Lisbon, opened in March 1998. It spans the Tagus estuary for about $17 \text{ km}$ — at the time, the longest bridge in Europe. The main cable-stayed section is about $830 \text{ m}$ long, with a deck supported by steel cables anchored to two towers each rising $148 \text{ m}$ above the waterline.

A car driving across the bridge weighs maybe $1{,}500 \text{ kg}$. The bridge deck weighs many millions of kilograms more. Wind loads add lateral forces of perhaps $10$–$50 \text{ kN}$ per meter of deck during a storm. Earthquakes — the region experienced a magnitude $8.7$ event in 1755 — could add lateral accelerations of fractions of $g$.

For the bridge to do its job, it has to stay still. *Every part of it.* The deck doesn't translate (no net force in any direction). The deck doesn't rotate (no net torque about any axis). Each cable carries a specific tension, computed during design, that contributes to making both sums vanish at every cross-section. Each tower bears a specific load, distributed across its concrete base, that keeps it from leaning.

This is the work of **statics**: solving for the forces and torques in a system *that doesn't move* so that all sums vanish. Bridges are perhaps the showcase application, but statics is everywhere — in your kitchen table not collapsing, in the hinges of every door, in the muscles of your arm holding a book, in the tendons supporting your weight when you stand still. Anything that is at rest under load is doing the static-equilibrium calculation, whether the engineer who designed it did the math or evolution did.

This chapter is about the two equilibrium conditions, the concept of torque, and the analysis that lets you solve for unknown forces in a static system.

**Learning objectives.** By the end of this chapter you should be able to:

1. State the two conditions for static equilibrium ($\sum \mathbf{F} = 0$ and $\sum \tau = 0$) and apply them.
2. Compute torque ($\tau = rF\sin\theta = r_\perp F = rF_\perp$) about any chosen pivot.
3. Solve for unknown forces in static structures: beams supported at two points, suspended objects, leaning ladders, forearm-and-bicep systems.
4. Distinguish stable, unstable, and neutral equilibrium and identify each from a diagram.
5. Compute mechanical advantage of simple machines (lever, pulley, inclined plane) and apply energy conservation to verify trade-offs.

**Prerequisites.** Chapter 4 (Newton's laws). Chapter 7 (work and energy, for mechanical advantage). Chapter 6 (angular vocabulary, for torque). Vector decomposition (Chapter 3) for resolving forces along chosen axes.

**Why this chapter matters.** Statics underlies every standing structure: bridges, buildings, towers, beams, scaffolds, prosthetics, bones. It's the most-used branch of mechanics in civil and mechanical engineering. The two conditions for equilibrium also generalize directly: in dynamics, what was zero net force becomes $\mathbf{F}_{\text{net}} = m\mathbf{a}$; what was zero net torque becomes $\tau_{\text{net}} = I\alpha$ (Chapter 10). Statics is the limiting case where both right-hand sides are zero.

---

## Concept 1 — The first condition: $\sum \mathbf{F} = 0$

### A book on a kitchen table

A $2 \text{ kg}$ book sits motionless on a level kitchen table. What forces are acting on it?

Two: the gravitational force pulling down ($W = mg = 2 \times 9.80 = 19.6 \text{ N}$ downward) and the normal force from the table pushing up ($N$ upward, magnitude unknown). Since the book is not moving, by Newton's second law the net force is zero. Therefore $N = 19.6 \text{ N}$ — exactly equal to the weight.

This is the simplest possible static-equilibrium problem. The first condition for equilibrium is:

$$\sum \mathbf{F}_{\text{external}} = 0,$$

which, in component form, is two equations in 2D (or three in 3D):

$$\sum F_x = 0, \qquad \sum F_y = 0.$$

The book example uses one of these (the vertical balance). The horizontal balance is also satisfied trivially (no horizontal forces). The two-equation system tells us $N$.

For more complex problems, the first condition gives two (or three) equations among the unknown forces. Often these are not enough by themselves — we'll need the second condition (Concept 2) to add the remaining equation(s).

### The mechanism — applying $\sum \mathbf{F} = 0$ in components

The procedure is identical to Chapter 4's free-body diagrams. Identify the system. Identify all external forces (weight, normals, tensions, friction, applied forces). Decompose each into chosen-axis components. Sum each axis to zero.

A subtlety from Chapter 5 returns here: in static problems, friction is often *static* friction, which can take any value from $0$ to $\mu_s N$. You don't always know its magnitude in advance — you solve for whatever value is needed to make the equilibrium work, then check that it's below the maximum.

### The trade-off

Static analysis trades **dynamic flexibility for fully-determined geometry.** A system at rest has no acceleration — so all forces must balance exactly. This makes equilibrium problems more restrictive than dynamic ones (everything has to be just-so), but it also means you can solve for unknown forces from the requirement of balance alone, without knowing anything about masses or moments.

### Worked example — a sign hanging from two ropes

A $200 \text{ N}$ sign hangs from two ropes attached to a ceiling. Rope 1 is at $30°$ from vertical; Rope 2 is at $45°$ from vertical (on the opposite side). Find the tension in each rope.

**Free-body diagram.** Sign as a point. Forces: weight $200 \text{ N}$ down. Tension $T_1$ along Rope 1 (up-and-left, $30°$ from vertical). Tension $T_2$ along Rope 2 (up-and-right, $45°$ from vertical).

**Components.**
- $T_{1,x} = -T_1 \sin 30° = -0.5 T_1$.
- $T_{1,y} = T_1 \cos 30° \approx 0.866 T_1$.
- $T_{2,x} = +T_2 \sin 45° \approx 0.707 T_2$.
- $T_{2,y} = T_2 \cos 45° \approx 0.707 T_2$.

**Horizontal equilibrium.** $-0.5 T_1 + 0.707 T_2 = 0 \implies T_1 = 1.414 T_2$.

**Vertical equilibrium.** $0.866 T_1 + 0.707 T_2 = 200$.

Substitute: $0.866 (1.414 T_2) + 0.707 T_2 = 200 \implies 1.225 T_2 + 0.707 T_2 = 200 \implies 1.932 T_2 = 200$.

$$T_2 = 103.5 \text{ N}, \quad T_1 = 1.414 \times 103.5 \approx 146.4 \text{ N}.$$

The steeper rope (Rope 1, $30°$ from vertical) carries more of the load — about $146 \text{ N}$ vs. $103 \text{ N}$ for Rope 2.

**Sanity check.** The vertical components must add to $200 \text{ N}$: $0.866(146.4) + 0.707(103.5) = 126.8 + 73.2 = 200 \text{ N}$ ✓. The horizontal components must cancel: $0.5(146.4) = 73.2 = 0.707(103.5)$ ✓.

**The general lesson.** With two unknowns (the two tensions) and two equations (one per axis), the system is fully determined by the first equilibrium condition alone. Many structural problems work this way; others require torque to close.

### Common misconceptions

- *"At rest means no forces."* No — at rest means the *sum* of forces is zero. Many forces can act simultaneously (a book has gravity and normal force; a bridge has many cable tensions and weight at every point) — they just sum to zero in static equilibrium.
- *"The normal force always equals weight."* Only when the surface is horizontal and there's no other vertical force. On an incline, $N = mg\cos\theta < mg$. With an additional downward force (someone pressing on the book), $N > mg$.

↳ **Dig Deeper — Statically determinate vs. indeterminate problems**

*A statically determinate problem has the same number of unknown forces as equilibrium equations — solvable by statics alone. A statically indeterminate problem has more unknowns than equations — requires additional information (material elasticity, deformations) to solve. Understanding the distinction is the entry to structural engineering.*

**Prompt:**
> Explain the distinction between statically determinate and statically indeterminate structures. Give one example of each: (a) a beam supported at two points (determinate — 3 equilibrium equations, 3 reaction-force unknowns), (b) a beam supported at three points (indeterminate — 3 equations, 4 unknowns). For the indeterminate case, explain what additional information (material stiffness via Hooke's law from Ch. 5) is needed to solve. End with one sentence on why most real engineered structures are designed to be statically determinate or only mildly indeterminate.

**What to do with the output:** Save it. The determinate/indeterminate distinction is foundational to structural engineering and clarifies why simple beam-and-truss problems are tractable while complex frames require finite-element analysis.

---

## Concept 2 — The second condition: $\sum \tau = 0$, and what torque is

### A wrench on a stuck bolt

You're trying to loosen a stuck bolt. You grip a wrench at the end of its handle and pull. The wrench rotates the bolt. Two physical features of how you pull determine how much rotational effect you get:

1. *How hard you pull* (the magnitude of the force).
2. *How far from the bolt your hand is* (the lever arm).

If you grip the wrench close to the bolt's head, you have to pull very hard. If you grip the end of the handle, you can pull less hard. A long-handled wrench (the box-end of a "breaker bar") can free a bolt that the same force on a short wrench couldn't budge.

Pulling perpendicular to the wrench works best. Pulling along the wrench (toward or away from the bolt) does nothing — it doesn't rotate the bolt at all. The angle between your pull and the wrench matters.

These three observations — magnitude of force, distance from pivot, angle — combine into a single quantity called **torque**:

$$\tau = r F \sin\theta,$$

where $r$ is the distance from the pivot to the point where the force is applied, $F$ is the force magnitude, and $\theta$ is the angle between $\mathbf{F}$ and $\mathbf{r}$.

### The mechanism — torque, the perpendicular lever arm, and the second condition

Equivalently, you can write torque as $\tau = r_\perp F$, where $r_\perp$ is the perpendicular distance from the pivot to the line of the force. (This is the "lever arm.") Or as $\tau = r F_\perp$, the distance times the perpendicular component of the force. All three forms give the same number.

Units: $\text{N·m}$. (Same units as energy, which is unfortunate. They're not the same physical quantity. Torque is a rotational analog of force; energy is energy.)

Sign: positive for counterclockwise rotation (by convention), negative for clockwise. In 3D, torque is properly a vector ($\boldsymbol{\tau} = \mathbf{r} \times \mathbf{F}$), pointing along the axis of rotation by the right-hand rule. For introductory 2D problems, just track signs.

The **second condition for equilibrium** is:

$$\sum \tau_{\text{external}} = 0,$$

evaluated about *any chosen pivot point*. Crucially, the pivot point is your choice — and a clever choice makes the algebra easy. If you put the pivot at the location where an unknown force is applied, that unknown contributes zero torque (its $r = 0$) and drops out of the equation. This is the chief trick of statics problems.

### The trade-off

Adding torque to the equilibrium analysis trades **a single force-balance equation system** for **a force-and-torque pair**. The added complexity is real — three equations in 2D instead of two. The benefit is enormous: many problems that are underdetermined by force balance alone become solvable when torque is included. Most structural problems require both.

### Worked example — a beam supported at two ends

A uniform $50 \text{ kg}$ beam of length $4.0 \text{ m}$ is supported at both ends. A $100 \text{ kg}$ person stands on the beam $1.0 \text{ m}$ from the left support. Find the support force at each end.

**Free-body diagram.** Beam horizontal. Forces: weight of beam ($W_b = 50 \times 9.80 = 490 \text{ N}$) at the beam's center ($2.0 \text{ m}$ from each support); weight of person ($W_p = 100 \times 9.80 = 980 \text{ N}$) at $1.0 \text{ m}$ from left support; left support force $F_L$ upward; right support force $F_R$ upward.

**Vertical equilibrium.** $F_L + F_R - 490 - 980 = 0 \implies F_L + F_R = 1470 \text{ N}$.

**Torque equilibrium about the left support** (so $F_L$ contributes zero torque): Counterclockwise positive.

- $F_R$ acts $4.0 \text{ m}$ to the right, upward → torque $+4.0 \times F_R$.
- Beam weight acts $2.0 \text{ m}$ to the right, downward → torque $-2.0 \times 490 = -980$.
- Person weight acts $1.0 \text{ m}$ to the right, downward → torque $-1.0 \times 980 = -980$.

Setting the sum to zero:

$$4.0 F_R - 980 - 980 = 0 \implies F_R = 490 \text{ N}.$$

Then from vertical equilibrium: $F_L = 1470 - 490 = 980 \text{ N}$.

The left support carries $980 \text{ N}$ (the heavier load, because the person is closer to it); the right support carries $490 \text{ N}$.

**Sanity check.** The total ($980 + 490 = 1470 \text{ N}$) equals the total weight ($490 + 980 = 1470 \text{ N}$) ✓. The left support carries more because the person stands closer to it; the lever arm of the person's weight about the right support is $3.0 \text{ m}$, while about the left it's $1.0 \text{ m}$. The torque-balance equation distributes the load proportionally.

### Common misconceptions

- *"The pivot is wherever the object actually rotates about."* No — for static problems, the object isn't rotating at all. The "pivot" is just a point you choose for taking torque. Any point works; clever choices simplify the algebra.
- *"A force directed through the pivot has no effect."* Correct, in the rotational sense — its torque about that pivot is zero. But it still contributes to the *force* balance (Concept 1's equations). It's eliminated from the *torque* equation only.
- *"Torque is the same as force."* No — torque is force times lever arm. A small force with a long lever arm can produce more torque than a large force with a short lever arm.

↳ **Dig Deeper — Why "any pivot" works for the torque equation**

*The chapter says you can choose any point as pivot for the torque equation, and it always works for an object in static equilibrium. This is non-trivial — a point off the object, or a moving point, all give the same equilibrium condition. Why?*

**Prompt:**
> Explain why, for an object in static equilibrium, the equation $\sum \tau = 0$ holds about *any* chosen point — not just the actual pivot or the center of mass. Walk through the algebra: show that if both $\sum \mathbf{F} = 0$ and $\sum \tau = 0$ about one point, then $\sum \tau = 0$ about any other point. (Hint: the change in pivot adds the same $-\mathbf{r}_{\text{pivot shift}} \times \mathbf{F}_{\text{net}}$ to every force's torque, and the sum of these is zero because $\mathbf{F}_{\text{net}} = 0$.) End with one sentence on why this is the key to choosing a clever pivot point.

**What to do with the output:** Save it. The "any pivot works" theorem is the heart of strategic statics problem-solving — without it, you'd have to commit to a single pivot and live with the consequences.

---

## Concept 3 — Stability, mechanical advantage, and the body as a structure

### A pencil balanced on its tip

Stand a pencil on its tip. It topples. The pencil was in equilibrium for an instant — net force zero, net torque zero — but the equilibrium was *unstable*. Any tiny perturbation (a breath, a draft, the unevenness of the table) tipped it past the point where gravity could no longer be balanced.

Now stand the same pencil on its eraser end (or lay it flat). Now perturbations don't matter — small disturbances die out, and it returns to its equilibrium. *Stable* equilibrium.

A ball on a flat table is in *neutral* equilibrium — perturbed, it stays where you put it but doesn't return to a particular spot.

The distinction is about what happens when you perturb the system. Stable: the perturbation creates a restoring torque/force pulling it back. Unstable: the perturbation creates a torque pushing it further away. Neutral: no restoring force (the system is indifferent to position).

### The mechanism — three types of equilibrium

For a static object, equilibrium is:

- **Stable** if any small displacement raises the center of mass (so gravity pulls it back).
- **Unstable** if any small displacement lowers the center of mass (so gravity pulls it further away).
- **Neutral** if displacement leaves the center of mass at the same height.

A stool standing on three legs is stable. A ball on top of a hill is unstable. A puck on a flat air-hockey table is neutral (in the horizontal direction).

### Mechanical advantage and simple machines

A **lever** lets you trade force for distance. Push down with a small force on the long end, and a large force is exerted on the short end — but the short end moves a much smaller distance than the long end. Energy is conserved (input work equals output work, in a frictionless ideal lever).

The **mechanical advantage** of a simple machine:

$$MA = \frac{F_{\text{output}}}{F_{\text{input}}}.$$

For an ideal lever (frictionless), MA equals the ratio of the two lever arm lengths:

$$MA = \frac{r_{\text{input}}}{r_{\text{output}}}.$$

A lever with input arm $0.5 \text{ m}$ and output arm $0.05 \text{ m}$ has $MA = 10$: a $100 \text{ N}$ push produces $1{,}000 \text{ N}$ of output force. But the output moves only $1/10$ the distance the input does.

Other simple machines: pulley (single fixed pulley has $MA = 1$ but redirects force; movable pulley systems can have $MA > 1$); inclined plane ($MA$ = length / height); wedge; screw. All trade force for distance, conserving the work product.

### The forearm as a third-class lever

Your forearm holding a book is a lever — and an unfavorable one. The biceps muscle attaches to the forearm bone (radius) about $5 \text{ cm}$ from the elbow joint. A book in your hand sits about $30 \text{ cm}$ from the elbow. The book's weight produces a torque about the elbow of $W_b \times 0.30 \text{ m}$. The biceps must produce an equal and opposite torque about the elbow: $F_{\text{biceps}} \times 0.05 \text{ m}$. So:

$$F_{\text{biceps}} = W_b \times \frac{0.30}{0.05} = 6 W_b.$$

To hold a $5 \text{ kg}$ book ($W_b = 49 \text{ N}$), the biceps must pull with $\sim 294 \text{ N}$ — about $30 \text{ kg}$ of force. Six times the book's weight. (The trade-off: the biceps moves a small distance; the hand moves six times further. Speed and range of motion are bought at the cost of force.)

### The trade-off

Stability/instability and mechanical-advantage analyses trade **detailed force-by-force calculation for a structural overview.** Knowing that an equilibrium is unstable doesn't tell you the exact restoring torque — but it tells you the system will not stay there under any real-world disturbance. Knowing that a lever has MA = 6 doesn't tell you the exact biomechanics of the muscle — but it tells you the muscle force is six times the load. These are rough but useful tools.

### Worked example — a ladder against a wall

A $5.0 \text{ m}$ uniform ladder of mass $20 \text{ kg}$ leans against a frictionless vertical wall, making an angle of $60°$ with the ground. The base of the ladder rests on a floor with friction coefficient $\mu_s = 0.40$. (a) Find the forces from the wall and the floor on the ladder. (b) Will the ladder slip?

**Free-body diagram.** Ladder of weight $W = 196 \text{ N}$ acting at its center ($2.5 \text{ m}$ along its length). Normal force from floor $N_f$ upward at the base. Friction force from floor $f$ horizontal at the base (toward the wall). Normal force from wall $N_w$ horizontal at the top (away from wall).

**Vertical equilibrium.** $N_f - W = 0 \implies N_f = 196 \text{ N}$.

**Horizontal equilibrium.** $f - N_w = 0 \implies f = N_w$.

**Torque about base** (so $N_f$ and $f$ contribute zero torque, leaving only the weight and $N_w$):

- Weight torque (clockwise, negative): $-W \times (2.5 \cos 60°) = -196 \times 1.25 = -245 \text{ N·m}$.
- Wall normal torque (counterclockwise, positive): $+N_w \times (5.0 \sin 60°) = +N_w \times 4.33$.

Setting sum to zero:

$$N_w \times 4.33 - 245 = 0 \implies N_w \approx 56.6 \text{ N}.$$

So $f \approx 56.6 \text{ N}$ also.

**Will it slip?** Maximum available static friction: $f_{\text{max}} = \mu_s N_f = 0.40 \times 196 = 78.4 \text{ N}$. Required: $56.6 \text{ N}$. Since required $<$ available, the ladder does not slip.

**Sanity check.** A common rule of thumb says ladders should be steeper than $\sim 70°$ for safety. At $60°$, our analysis says the ladder is stable for $\mu_s \geq 56.6/196 = 0.29$. With $\mu_s = 0.40$, we're above threshold. If the floor were oilier (smaller $\mu_s$) or the ladder shallower (larger $\theta$ from vertical), it would slip.

### Common misconceptions

- *"A simple machine creates energy."* No — it trades force for distance. Output work equals input work (or less, if friction is present). The mechanical advantage tells you the force ratio; the inverse is the distance ratio.
- *"The biceps muscle pulls the book up directly."* The biceps pulls the forearm up, and the forearm rotates about the elbow joint. The mechanical structure is a lever with very poor mechanical advantage (force-multiplying *down*, by a factor of ~6). The body trades force for speed/range.
- *"Stable equilibrium means very strong."* No — stable means restoring under small perturbations. A teacup on a saucer is in stable equilibrium but a strong gust will still knock it over. Stable is qualitative; "how stable" is about perturbation magnitude.

↳ **Dig Deeper — Center of mass and stability**

*An object's stability is closely tied to whether its center of mass falls within its base of support. If you tilt an object and the center of mass passes outside the base of support, the object tips over. This is why semi trucks roll over in tight turns and why a person bends at the waist while carrying a heavy load.*

**Prompt:**
> Explain the relationship between center of mass and stability for a freestanding object. Walk through the geometric criterion: an object is stable if the vertical line through its center of mass passes through its base of support. Apply this to: (a) a person standing upright, (b) a person carrying a heavy backpack and leaning forward, (c) a tractor-trailer in a tight turn (where lateral acceleration shifts the effective gravity vector). End with one sentence on why a wider base or a lower center of mass increases stability.

**What to do with the output:** Save it. The center-of-mass-over-base-of-support criterion is the most useful intuitive rule in statics and explains a remarkable amount of everyday stability behavior.

---

## Synthesis — statics as the gateway to structural physics

Step back. Two equilibrium conditions:

**Force balance:** $\sum \mathbf{F} = 0$. Every translational tendency cancels.

**Torque balance:** $\sum \tau = 0$ about any chosen pivot. Every rotational tendency cancels.

Together: two (or three) equations from force, plus one (or three) from torque. Solve for the unknown forces. Apply the result to design a beam, choose a tension cable, predict whether a ladder slips, compute how hard a muscle pulls.

The **scale shift** I want you to feel: the same two equations describe a $0.5 \text{ kg}$ book on a kitchen table ($\sum F$ has just two terms), a $1{,}500 \text{ kg}$ car parked on a level driveway, a $5 \text{ m}$ ladder leaning at $60°$, and a $17 \text{ km}$ Vasco da Gama Bridge with hundreds of cable tensions and millions of newtons of deck weight. The first equation says nothing translates; the second says nothing rotates; the rest is bookkeeping at whatever scale the structure demands.

### A worked example using all three concepts — a person doing a one-arm pull-up

A $70 \text{ kg}$ person hangs from a horizontal bar by one hand. (a) What is the tension in the supporting arm? (b) The deltoid muscle in the shoulder attaches to the upper-arm bone (humerus) about $10 \text{ cm}$ from the shoulder joint, at an angle of $15°$ from the bone. The hand grips the bar $40 \text{ cm}$ from the shoulder joint. What force does the deltoid muscle exert?

**(a) Vertical equilibrium of the body** (Concept 1). Bar tension up = body weight down. So $T = mg = 70 \times 9.80 = 686 \text{ N}$. About $700 \text{ N}$ — equivalent to lifting a 70 kg weight, which is exactly what the person is doing.

**(b) Torque about the shoulder joint** (Concept 2). The arm is approximately horizontal from shoulder to hand. Forces on the arm: weight of the arm (ignore for simplicity), tension at the hand pulling down ($T = 686 \text{ N}$ at $40 \text{ cm}$ from shoulder), deltoid muscle pulling at $15°$ above the bone, $10 \text{ cm}$ from shoulder.

Torque from hand tension (clockwise): $T \times 0.40 = 686 \times 0.40 = 274 \text{ N·m}$.

Torque from deltoid (counterclockwise): $F_d \sin 15° \times 0.10 = F_d \times 0.0259$.

Set equal:

$$F_d \times 0.0259 = 274 \implies F_d \approx 10{,}600 \text{ N}.$$

About $10{,}600 \text{ N}$ — over a metric ton of force. To support a $700 \text{ N}$ body weight, the deltoid muscle pulls with about $15$ times that.

**Concept 3 — mechanical advantage.** The lever arm of the muscle ($\sin 15° \times 0.10 \approx 0.026 \text{ m}$) is much shorter than the lever arm of the load ($0.40 \text{ m}$). The mechanical advantage is *less than one* — about $0.07$. The muscle has to work much harder than the body would weigh if simply lifted directly.

This is biology. Skeletal muscles are attached close to joints (small lever arms) to provide range and speed of motion at the cost of requiring high muscle forces. We trade force for speed. The cost: muscles are typically working at ten times or more the load they're moving. A weightlifter "lifting" $200 \text{ kg}$ is internally producing forces of thousands of newtons in their tendons.

---

## Exercises

### Warm-up

**9.1** *(LO 1)* A $5 \text{ kg}$ box sits on a level floor. (a) What is the normal force? (b) What if you press down on it with $20 \text{ N}$?

**9.2** *(LO 2)* A force of $40 \text{ N}$ is applied perpendicular to the end of a wrench $0.20 \text{ m}$ long. What is the torque?

**9.3** *(LO 3)* A $10 \text{ kg}$ uniform beam of length $2.0 \text{ m}$ is supported at one end by a pin and at the other by an upward vertical rope. Find the rope tension.

**9.4** *(LO 4)* Identify each as stable, unstable, or neutral equilibrium: (a) a marble at the bottom of a bowl, (b) a marble at the top of a hill, (c) a marble on a flat table, (d) a coin balanced on its edge.

### Application

**9.5** *(LO 1, 2, 3)* A $4.0 \text{ m}$ uniform $30 \text{ kg}$ plank is supported at both ends. A $60 \text{ kg}$ person stands $1.0 \text{ m}$ from the left end. Find the support force at each end.

**9.6** *(LO 1, 2)* A $5.0 \text{ m}$ uniform $15 \text{ kg}$ ladder leans against a frictionless wall at $70°$ from the ground. (a) Find the wall normal force. (b) Find the floor friction force. (c) What minimum coefficient of static friction is required?

**9.7** *(LO 5)* A lever has input arm $1.0 \text{ m}$ and output arm $0.20 \text{ m}$. (a) What is the mechanical advantage? (b) If you push down with $50 \text{ N}$ on the input, what output force do you get? (c) If your input end moves $0.5 \text{ m}$, how far does the output move?

**9.8** *(LO 3)* A $200 \text{ N}$ sign hangs from a horizontal beam supported by a hinge on the wall. A cable from the top of the beam to the wall is attached at $40°$ above horizontal. Find the cable tension and the force from the hinge on the beam.

### Synthesis

**9.9** *(LO 1, 2, 3)* A $1{,}000 \text{ kg}$ truck is parked halfway across a uniform $5{,}000 \text{ kg}$ bridge $30 \text{ m}$ long, supported at both ends. Find the support force at each end.

**9.10** *(LO 2, 5)* A person's forearm is modeled as a $3 \text{ kg}$ lever pivoted at the elbow. The biceps attaches $5 \text{ cm}$ from the elbow; the forearm + hand is $35 \text{ cm}$ long; the person holds a $5 \text{ kg}$ weight in the hand. Find: (a) the torque from the weight about the elbow, (b) the torque from the forearm's own weight (acting at its center, $17.5 \text{ cm}$), (c) the biceps force needed to hold the arm horizontal.

**9.11** *(LO 4)* A semi truck has its center of mass $1.5 \text{ m}$ above the road and a track width (distance between left and right wheels) of $2.6 \text{ m}$. (a) On what slope angle (sideways tilt) will it tip? (b) Compare to a passenger car with center of mass $0.5 \text{ m}$ up and track width $1.6 \text{ m}$.

### Challenge

**9.12** *(LO 1, 2, beyond chapter)* A uniform door of mass $30 \text{ kg}$, height $2.0 \text{ m}$, and width $0.80 \text{ m}$ hangs from two hinges, one $0.30 \text{ m}$ from the top and one $0.30 \text{ m}$ from the bottom. The door's weight acts at its center. Find the horizontal and vertical force components on each hinge.

**9.13** *(LO 5, beyond chapter)* The Egyptian pyramids were partially built using ramps and inclined planes. A $2{,}500 \text{ kg}$ stone block is to be raised $4 \text{ m}$ vertically. (a) If lifted directly, what work is required? (b) If pushed up a frictionless ramp $40 \text{ m}$ long, what force is required and what work is done? (c) With friction coefficient $0.3$ between block and ramp, what force is required, and what is the new work?

---

## LLM Exercise — Chapter 9: Statics in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A static-equilibrium analysis of one part of your anchor phenomenon at rest.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 9, I want to apply the two conditions of static equilibrium ($\sum F = 0$, $\sum \tau = 0$) to one stationary element of my phenomenon. Please:

1. Identify ONE stationary structural element in my phenomenon. Examples:
   - Bike commute: bike at rest leaning against a wall — what tension in any straps, what friction at floor?
   - Coffee maker: brewing chamber gasket under pressure load — what static force balance keeps it sealed?
   - Basketball: a basketball balanced on a fingertip — what center-of-mass condition?
   - Marathon: a runner standing at the starting line — what muscles are active to maintain posture?
   - Espresso: portafilter handle locked into the group head — what torque balance holds it in place under 9 bar?

2. Draw (in ASCII or describe) the free-body diagram. Identify all external forces and where they act.

3. Apply $\sum F = 0$ along each axis. Apply $\sum \tau = 0$ about a clever pivot.

4. Solve for the unknown forces. Report with units, sig figs, and percent uncertainty.

5. Sanity-check: does the magnitude of the muscle/cable/contact force surprise you? (Most do — they're often much larger than expected.)

6. Identify stability (stable, unstable, neutral) and the geometric criterion (does center of mass fall within base of support?).

7. One sentence on how this connects to Chapter 10 (rotational dynamics) — when torques don't balance, the object accelerates rotationally.

Save the output as logbook/chapter-09-statics.md.
```

### What this produces

A ninth Logbook entry: an equilibrium analysis revealing the often-surprising forces in stationary structures.

### How to adapt this prompt

- *For phenomena that don't have obvious static structures* (a moving phenomenon): focus on a moment when the system is briefly at rest (a basketball at the apex, a runner at the moment of foot plant, a bike at a traffic light).
- *For ChatGPT or Gemini:* identical with substitutions.
- *For Claude Code:* if you have a CAD model or measurements, paste dimensions.

### Connection to previous chapters

Builds directly on Chapter 4 (force balance is part of Newton's first law). Adds rotational equilibrium. Uses vector decomposition (Chapter 3) and friction (Chapter 5).

### Preview of next chapter

Chapter 10 generalizes everything in this chapter to *moving* rotational systems. Where statics had $\sum \tau = 0$, dynamics has $\sum \tau = I\alpha$ — the rotational analog of $F = ma$. The framework is the same; only the right-hand side moves from zero to mass-times-acceleration.

---

## Chapter summary

Two equilibrium conditions. **Force balance** $\sum \mathbf{F} = 0$ ensures no translational acceleration. **Torque balance** $\sum \tau = 0$ about any chosen pivot ensures no rotational acceleration. Together, they let you solve for unknown forces in any statically determinate structure.

The one idea that matters most: **statics requires both conditions, not just one.** A system can have balanced forces and still rotate (e.g., a wheel spinning freely about its center). It can have balanced torques and still translate (e.g., an object subject to two equal-and-opposite forces applied at the same point — net force zero, but each force could be displaced). Equilibrium needs both.

The common mistake to watch for: **forgetting that the choice of pivot matters strategically, not physically.** Any pivot works mathematically (the chapter's Dig Deeper proves this). But choosing a pivot at the location of an unknown force eliminates that unknown from the torque equation, simplifying the algebra dramatically. Strategic pivot choice is the chief skill of statics problem-solving.

What you should now be able to teach someone else: how to draw a free-body diagram for a static structure, how to write force-balance equations along chosen axes, how to write torque-balance equations about a clever pivot, and how to solve the resulting system. Plus how to identify stable/unstable/neutral equilibrium from geometry. Five skills, two underlying conditions.

---

## What would change my mind

The chapter argues that the two equilibrium conditions ($\sum F = 0$, $\sum \tau = 0$) are exact in classical mechanics for any rigid body at rest. The argument would need revision if a structural problem at rest required a third equation in 2D (or more than six in 3D) to solve — which would mean the system is statically indeterminate, requiring deformation analysis. This isn't a refutation of the framework; it's an extension into elasticity (Chapter 5) and the modern field of finite-element analysis.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is rigid-body assumption ever a good approximation?** All real materials deform under load (Hooke's law, Chapter 5). Yet treating a beam as perfectly rigid for the purpose of calculating support reactions almost always gives the right answer. Why? The answer involves the smallness of typical strains compared to the geometric dimensions — but the question of when the approximation breaks down (slender structures, dynamic loading, near material limits) is the whole subject of structural mechanics, beyond what we'll resolve here.

---

## Connections forward

Chapter 10 generalizes statics to dynamics: the analog of $\sum F = ma$ for rotation is $\sum \tau = I\alpha$, where $I$ is moment of inertia and $\alpha$ is angular acceleration. Statics is the limiting case ($\alpha = 0$). Chapter 11 (fluid statics) applies the static-equilibrium framework to fluids — pressure as the fluid analog of force, with the same balancing requirements. Chapters 14–15 (heat, thermodynamics) introduce thermal equilibrium, a different kind of "nothing changing" condition. The pattern that runs through is: equilibrium, in any branch of physics, means *whatever quantity could change is balanced so it doesn't*.

---

**Tags:** statics, torque, equilibrium, mechanical-advantage, free-body-diagram

---

## AI Wayback Machine

**Archimedes of Syracuse** worked out the law of the lever and the basics of static equilibrium in the 3rd century BCE — "Give me a place to stand, and I will move the Earth." His treatises on mechanics established statics as a quantitative science.

**Run this:**

```
Who was Archimedes, and how does his work connect to the statics and torque we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Archimedes"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Archimedes's geometric proof of the law of the lever.
- Ask it about the loss of Archimedes's writings — and their partial recovery from the Archimedes Palimpsest.

What changes? What gets better? What gets worse?
