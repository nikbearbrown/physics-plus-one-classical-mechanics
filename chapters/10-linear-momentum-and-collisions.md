# Chapter 10 — Linear Momentum and Collisions

**Suggested titles**

1. Linear Momentum and Collisions
2. Why a Cue Ball Stops Dead
3. The Other Conservation Law

**TL;DR.** Energy is conserved. Momentum is conserved. Two of the deepest principles in physics, two different kinds of accounting. This chapter installs momentum ($\mathbf{p} = m\mathbf{v}$) and impulse ($\mathbf{J} = \mathbf{F}\Delta t = \Delta\mathbf{p}$), shows that the total momentum of an isolated system never changes, and uses the principle to predict the outcome of collisions — elastic and inelastic, head-on and 2D, ball-on-ball and rocket-burns-fuel. The same idea explains why a cue ball stops when it hits another billiard ball squarely, why airbags reduce injury, and why rockets work in vacuum.

---

## A jet engine on the test stand, Wright-Patterson AFB, 1947

A General Electric J47 turbojet is bolted to a steel frame the size of a small building. The engine is connected to fuel lines, instrumentation, and a chain of strain gauges that measure the force it exerts on the test stand. The throttle goes to maximum.

The engine roars. Air rushes in the front, mixes with kerosene, ignites, expands, and rushes out the back at over $600 \text{ m/s}$. The strain gauges on the test stand register a steady forward push of about $25{,}000 \text{ N}$ — five tons of thrust, as engineers say. The engine isn't moving. It's bolted down. But it is *pushing* the test stand forward, and it would be pushing an aircraft forward too, if attached.

Where does the push come from? The engine is throwing mass (combustion products and accelerated air) backward. By Newton's third law, the mass throws the engine forward with equal and opposite force. The faster you throw the mass, or the more mass you throw per second, the bigger the forward force. There is no surrounding medium that the engine pushes against. There doesn't need to be. The engine's thrust depends entirely on what's exiting the back, not on anything the surrounding air does.

This is the central insight of momentum conservation. The total momentum of the engine + ejected gases is conserved. If the engine is to gain forward momentum, the gases must lose backward momentum (i.e., gain forward momentum) — which means, equivalently, the gases must travel backward fast. Throwing things backward is how you go forward. It works in air. It works in vacuum. It works in space.

In 1957, *Sputnik 1* (Chapter 6) was placed in orbit by exactly this principle, scaled up: the Soviet R-7 rocket throwing its kerosene-and-LOX exhaust products backward fast enough to push the rest of itself forward and upward, eventually leaving Earth's atmosphere altogether. Same physics as the engine on the test stand. Same conservation law.

This chapter installs that conservation law, and uses it to predict what happens in collisions, recoils, and rocket flights.

**Learning objectives.** By the end of this chapter you should be able to:

1. Compute linear momentum $\mathbf{p} = m\mathbf{v}$ and impulse $\mathbf{J} = \mathbf{F}\Delta t = \Delta\mathbf{p}$ for any moving object or system.
2. State and apply the conservation of linear momentum: in an isolated system (no net external force), $\mathbf{p}_{\text{total}}$ is constant.
3. Solve elastic 1D collision problems (where both momentum and kinetic energy are conserved).
4. Solve inelastic and perfectly-inelastic collision problems (momentum conserved; kinetic energy not).
5. Solve 2D collision problems by applying conservation of momentum along each axis separately.
6. Apply momentum conservation to a recoiling or thrust-producing system (gun firing, rocket burn).

**Prerequisites.** Chapter 4 (Newton's laws). Chapter 7 (kinetic energy). Vector decomposition from Chapter 3 (2D collisions).

**Why this chapter matters.** Conservation of momentum is what makes collisions tractable. Every car-crash analysis, every billiard-ball calculation, every astronaut-shoves-against-spacecraft scenario, every rocket flight, every particle-physics experiment in a collider relies on it. Combined with energy conservation (Chapter 7), momentum gives you the two-equation system that solves most collision problems in classical mechanics in closed form.

---

## Concept 1 — Momentum and impulse

### A tennis serve at 200 km/h

Roger Federer at full extension, racquet meeting ball at the apex of his serve, $200 \text{ km/h}$ ($55 \text{ m/s}$) of ball velocity transmitted in the contact, which lasts maybe $5 \text{ ms}$. Tennis ball mass: $0.057 \text{ kg}$. Change in ball velocity from rest (at the toss peak): $0$ to $55 \text{ m/s}$, so $\Delta v = 55 \text{ m/s}$.

The ball's momentum after contact: $p = m v = 0.057 \times 55 \approx 3.1 \text{ kg·m/s}$.

The force during contact: from $\mathbf{F} \cdot \Delta t = \Delta \mathbf{p}$, $F = \Delta p / \Delta t = 3.1 / 0.005 = 620 \text{ N}$. About $140$ pounds of force, applied for one two-hundredth of a second.

Two of these things — momentum and impulse — are what this concept is about. Momentum is the *amount of motion* an object has, equal to mass times velocity. Impulse is what changes momentum: a force applied over time.

### The mechanism — momentum, impulse, and Newton's second law (the original form)

**Momentum** is defined:

$$\mathbf{p} = m \mathbf{v}.$$

A vector. Units: $\text{kg·m/s}$. Same direction as velocity.

**Impulse** of a force is the integral of force over time, or, for constant force, simply force times time:

$$\mathbf{J} = \mathbf{F}_{\text{net}} \, \Delta t.$$

The **impulse-momentum theorem** says impulse equals change in momentum:

$$\mathbf{J} = \Delta \mathbf{p} = m \mathbf{v}_f - m \mathbf{v}_i.$$

This is just Newton's second law multiplied through by $\Delta t$:

$$\mathbf{F} = m \mathbf{a} = m \frac{\Delta \mathbf{v}}{\Delta t} \implies \mathbf{F} \, \Delta t = m \Delta \mathbf{v} = \Delta \mathbf{p}.$$

Newton himself originally wrote his second law in terms of momentum, not acceleration: *the rate of change of momentum is equal to the impressed force.* In symbols:

$$\mathbf{F}_{\text{net}} = \frac{d\mathbf{p}}{dt}.$$

For constant mass, this reduces to $F = ma$. For variable mass (a rocket burning fuel, water flowing through a hose), the momentum form is more general — it handles cases the constant-mass form fails.

### The trade-off

The momentum framework trades **the velocity-and-acceleration vocabulary** of Chapter 4 **for a quantity directly conserved**. Velocity is not conserved — it changes whenever a force acts. Momentum is conserved (as we'll see in Concept 2) when *external* forces are absent. The shift in vocabulary lets us solve problems where keeping track of every force during a brief collision would be infeasible.

### Worked example — the airbag

In a $30 \text{ km/h}$ ($8.3 \text{ m/s}$) head-on crash, a $70 \text{ kg}$ driver decelerates from $8.3 \text{ m/s}$ to $0$. (a) What is the change in momentum? (b) If the driver is stopped over $0.1 \text{ s}$ by an airbag, what is the average force on the driver? (c) Without an airbag, the driver hits the steering wheel and decelerates over $0.01 \text{ s}$. What is the force then?

**Change in momentum.**

$$\Delta p = m \Delta v = 70 \times (-8.3) = -581 \text{ kg·m/s}.$$

**With airbag.**

$$F = \frac{\Delta p}{\Delta t} = \frac{-581}{0.1} = -5810 \text{ N} \approx 6 \text{ kN}.$$

**Without airbag.**

$$F = \frac{-581}{0.01} = -58{,}100 \text{ N} \approx 58 \text{ kN}.$$

**Sanity check.** The airbag spreads the same change in momentum over ten times longer, reducing the peak force by a factor of ten. Same impulse; very different peak force. $6 \text{ kN}$ is uncomfortable but survivable; $58 \text{ kN}$ is bone-breaking. This is exactly why airbags work — they extend $\Delta t$, dropping $F$ for the same $\Delta p$.

### Common misconceptions

- *"Momentum and force are the same."* Momentum is a property of an object's motion; force is what changes that property over time. Their units are different ($\text{kg·m/s}$ vs. $\text{N}$).
- *"Larger momentum always means more dangerous in a collision."* Not necessarily — the danger is the *force*, which depends on how quickly the momentum changes. A large momentum dissipated slowly (parachutist landing, airbag) is safe; a small momentum stopped abruptly (head into a hard wall) can kill.

↳ **Dig Deeper — The momentum form of Newton's second law for variable mass**

*Newton's $F = dp/dt$ handles cases where mass changes — rockets, conveyors, falling chains. The constant-mass second law $F = ma$ silently assumes mass is unchanging. The momentum form is the correct general statement.*

**Prompt:**
> Walk through the momentum form $\mathbf{F} = d\mathbf{p}/dt$ for variable mass. Apply it to a rocket of mass $m(t)$ ejecting exhaust at speed $v_e$ relative to the rocket at rate $dm/dt$. Derive the rocket equation $\Delta v = v_e \ln(m_0 / m_f)$, where $m_0$ is initial mass and $m_f$ is final mass. Then explain (a) why this is called Tsiolkovsky's equation, (b) what it tells us about how to maximize $\Delta v$, (c) why staging (multiple rockets shed sequentially) is necessary for getting to orbit. End with one sentence on why the momentum form is required here and the constant-mass form would fail.

**What to do with the output:** Save it. The Tsiolkovsky rocket equation is the foundation of rocket science and one of the most consequential equations ever derived from $F = dp/dt$.

---

## Concept 2 — Conservation of momentum

### Two carts on an air track

Two carts on a low-friction air track. Cart A ($m_A = 1.0 \text{ kg}$) moves at $v_A = 2.0 \text{ m/s}$ to the right. Cart B ($m_B = 2.0 \text{ kg}$) is stationary. Cart A collides with Cart B. They stick together. What is the velocity of the combined cart afterward?

Without momentum conservation, this is impossible to solve from the given information — you'd need to know the force, the contact time, the deformation, and the friction. With momentum conservation, it's one line.

**Total momentum before:** $p_i = (1.0)(2.0) + (2.0)(0) = 2.0 \text{ kg·m/s}$.

**Total momentum after:** $p_f = (m_A + m_B) v_f = (3.0) v_f$.

**Conservation:** $p_i = p_f \implies v_f = 2.0 / 3.0 \approx 0.67 \text{ m/s}$.

The combined cart moves at $0.67 \text{ m/s}$ to the right after the collision. We didn't need any details of the collision — just the principle.

### The mechanism — when and why momentum is conserved

For an **isolated system** — one with no net external force — the total momentum is constant:

$$\mathbf{p}_{\text{total},i} = \mathbf{p}_{\text{total},f}.$$

The proof is short. By Newton's third law, internal forces in a system come in equal-and-opposite pairs (action and reaction). When you sum the impulses of all internal forces over the system, they cancel. Only external forces can change the system's total momentum. If there are no external forces, total momentum is constant.

The qualifier "isolated" matters. For a single cart on a track with no friction, momentum changes whenever your push acts. Once you let go and only internal forces (cart hitting another cart) act, total momentum of all carts together is conserved.

In practice, "isolated" often means: external forces are negligible compared to the internal forces during the brief collision. A car crash takes $0.1 \text{ s}$; gravity and friction during that interval impart very small impulses compared to the contact forces. The collision approximately conserves momentum, even though gravity is acting on the cars throughout.

### The trade-off

Conservation of momentum trades **detailed knowledge of the collision dynamics for a high-level conservation principle.** You don't have to know what the force-vs-time curve was during the impact; you only need the before and after states. The cost is that you can't predict, from momentum conservation alone, things like the deformation pattern or the contact time. You can predict the *outcome*.

### Worked example — recoil of a rifle

A $5.0 \text{ kg}$ rifle fires a $0.020 \text{ kg}$ bullet at $400 \text{ m/s}$. What is the recoil velocity of the rifle?

**Before firing.** Bullet at rest in chamber, rifle stationary. Total momentum $= 0$.

**After firing.** Bullet at $+400 \text{ m/s}$, rifle at velocity $v_r$ (to be found, expect negative).

**Conservation.** $0 = (0.020)(400) + (5.0) v_r$.

$$v_r = -\frac{(0.020)(400)}{5.0} = -1.6 \text{ m/s}.$$

The rifle recoils at $1.6 \text{ m/s}$ backward.

**Sanity check.** $1.6 \text{ m/s}$ is fast enough to feel ($\sim 5.8 \text{ km/h}$), and consistent with what shooters report. The rifle is far heavier than the bullet but much slower — they have equal and opposite momenta.

### Common misconceptions

- *"Momentum is always conserved."* Only in isolated systems. With external forces (gravity acting throughout, friction over a long time), momentum changes — and you must include the impulse from external forces explicitly.
- *"Conservation means nothing happens."* No — it means a specific quantity stays the same. Lots can happen (heat generated, sound emitted, deformation occurring) and momentum is still conserved if no external forces act.

↳ **Dig Deeper — Why momentum is conserved (Noether's theorem)**

*Why is momentum conserved? In 1918, the mathematician Emmy Noether proved a profound theorem: every continuous symmetry of the laws of physics implies a corresponding conservation law. Momentum conservation is a consequence of the fact that the laws of physics are the same here as they are over there — translational symmetry of space.*

**Prompt:**
> Explain Noether's theorem in one paragraph. Then describe how each of the three classical conservation laws corresponds to a symmetry: (a) momentum conservation ↔ translational symmetry of space, (b) energy conservation ↔ time-translation symmetry, (c) angular momentum conservation ↔ rotational symmetry of space. End with one sentence on what the implications are if a conservation law were ever experimentally violated (it would mean the corresponding symmetry is broken — a major discovery).

**What to do with the output:** Save it. Noether's theorem is the deepest result connecting symmetry to conservation in physics. It quietly underlies every chapter of the rest of the book.

---

## Concept 3 — Collisions: elastic and inelastic

### A cue ball striking a stationary ball squarely

A skilled pool player hits a cue ball squarely into a stationary target ball. After contact, the cue ball stops dead, and the target ball moves off with the speed the cue ball had. Same masses, head-on collision, very nearly elastic — and the velocity simply *transfers* from one ball to the other.

Why? Both momentum and kinetic energy are conserved in this collision. Two unknowns (the two final velocities), two equations. The unique solution is: cue ball stops, target ball takes off.

This special case is one of the most-photographed results of intro physics — the "Newton's cradle" sitting on countless desks shows it: drop one ball, only the far ball flies out, with the same speed.

### The mechanism — elastic and inelastic collisions

In an **elastic collision**, both momentum and kinetic energy are conserved:

$$m_1 v_{1i} + m_2 v_{2i} = m_1 v_{1f} + m_2 v_{2f},$$
$$\tfrac{1}{2} m_1 v_{1i}^2 + \tfrac{1}{2} m_2 v_{2i}^2 = \tfrac{1}{2} m_1 v_{1f}^2 + \tfrac{1}{2} m_2 v_{2f}^2.$$

Two equations, two unknowns ($v_{1f}$, $v_{2f}$). Closed-form solution.

For the special case of a 1D collision where mass 1 hits a stationary mass 2 elastically:

$$v_{1f} = \frac{m_1 - m_2}{m_1 + m_2} v_{1i}, \qquad v_{2f} = \frac{2 m_1}{m_1 + m_2} v_{1i}.$$

For equal masses ($m_1 = m_2$): $v_{1f} = 0$ and $v_{2f} = v_{1i}$. The cue ball stops; the target ball takes off. Exactly what we observed.

In an **inelastic collision**, momentum is conserved but kinetic energy is not (some converts to heat, sound, deformation). The energy equation no longer holds; you need another piece of information. The simplest case is the **perfectly inelastic** collision, where the objects stick together:

$$m_1 v_{1i} + m_2 v_{2i} = (m_1 + m_2) v_f.$$

One equation, one unknown.

For 2D collisions, momentum is conserved along each axis separately:

$$p_{x,i} = p_{x,f}, \qquad p_{y,i} = p_{y,f}.$$

Plus, if elastic, the kinetic-energy equation. Three equations, four unknowns (two final speeds, two final angles) — usually one more piece of information (one of the angles, often) closes it.

### The trade-off

Collision analysis trades **microscopic detail of the impact** (force-vs-time, deformation, sound, heat) **for macroscopic conservation laws** (momentum, energy if elastic). The cost is you don't know what happened during the collision; the benefit is you know what was true before and what is true after.

### Worked example — perfectly inelastic 2D collision

A $1{,}000 \text{ kg}$ car traveling east at $20 \text{ m/s}$ collides with a $1{,}500 \text{ kg}$ truck traveling north at $15 \text{ m/s}$. They stick together after the collision. What is their combined velocity?

**Set up axes.** $x$ east, $y$ north.

**Initial momenta.**
- Car: $p_{x,1} = (1000)(20) = 20{,}000 \text{ kg·m/s}$, $p_{y,1} = 0$.
- Truck: $p_{x,2} = 0$, $p_{y,2} = (1500)(15) = 22{,}500 \text{ kg·m/s}$.

**Total before.**
- $p_{x,\text{tot}} = 20{,}000$, $p_{y,\text{tot}} = 22{,}500$.

**After (combined mass $m = 2{,}500 \text{ kg}$).**
- $v_x = 20{,}000 / 2{,}500 = 8.0 \text{ m/s}$.
- $v_y = 22{,}500 / 2{,}500 = 9.0 \text{ m/s}$.

**Magnitude and direction.**
$$v = \sqrt{8.0^2 + 9.0^2} = \sqrt{64 + 81} = \sqrt{145} \approx 12.0 \text{ m/s}.$$
$$\theta = \tan^{-1}(9.0 / 8.0) = \tan^{-1}(1.125) \approx 48.4°.$$

The wreckage moves at $12.0 \text{ m/s}$, $48.4°$ north of east.

**Sanity check.** The combined velocity is between the two original speeds, which makes sense. The angle is between east (car's direction) and north (truck's direction), weighted by their respective momenta. The truck had slightly more momentum (because of higher mass × lower speed), so the angle leans slightly toward north.

**Energy check.** $KE_i = \tfrac{1}{2}(1000)(20)^2 + \tfrac{1}{2}(1500)(15)^2 = 200{,}000 + 168{,}750 = 368{,}750 \text{ J}$. $KE_f = \tfrac{1}{2}(2500)(12.0)^2 = 180{,}000 \text{ J}$. Energy lost: $368{,}750 - 180{,}000 = 188{,}750 \text{ J}$ — about half! Where did it go? Into deformation of the metal, into heat, into sound. Inelastic collisions always lose kinetic energy, often a substantial fraction.

### Common misconceptions

- *"Energy is always conserved in collisions."* Only in elastic collisions, which are rare in everyday life. Real collisions (cars, billiards, sports balls, even atomic-scale crashes) lose some energy to heat, sound, deformation. Momentum, however, is always conserved (in isolated systems).
- *"In a perfectly inelastic collision, the objects stop."* No — they move together at a velocity determined by momentum conservation. They only stop if the total initial momentum was zero.
- *"A heavy object hitting a light stationary one bounces back."* Almost — for a very heavy object hitting a very light one ($m_1 \gg m_2$), the heavy one barely slows ($v_{1f} \approx v_{1i}$) and the light one is launched at twice the original speed ($v_{2f} \approx 2 v_{1i}$). For the reverse case (light hits heavy stationary), the light one bounces back at nearly its original speed, and the heavy one barely moves.

↳ **Dig Deeper — Particle physics and the discovery of new particles via momentum conservation**

*Particle accelerators (the LHC, Fermilab) collide particles at near-light speed. The post-collision particles are tracked by detectors, and from the visible momenta of the products, momentum conservation lets physicists infer what was created — including particles that don't directly trigger the detector. The discovery of the neutrino, the Higgs boson, and many other particles relies on this.*

**Prompt:**
> Explain how conservation of momentum (and energy) is used in particle physics to infer the existence of unseen particles. Take one specific historical example: the discovery of the neutrino — Pauli proposed it in 1930 to "save" energy and momentum conservation in beta decay, when the observed electron's momentum did not balance. Walk through what was observed, what conservation predicted, and how the missing momentum pointed to a new particle. End with one sentence on what other particles have been discovered or characterized this way (Higgs boson, dark matter searches).

**What to do with the output:** Save it. The neutrino story is one of the cleanest examples of conservation laws driving the discovery of new physics.

---

## Synthesis — momentum, conservation, and the structure of mechanics

Step back. Two great conservation laws of mechanics: energy (Chapter 7) and momentum (this one).

**Energy conservation:** scalar, always exact, requires expanding ledger to include heat. Tells you about *speeds*.

**Momentum conservation:** vector, exact for isolated systems, no need to track heat. Tells you about *outcomes after collisions*.

The two together are the most powerful machinery in classical mechanics. For any 1D elastic collision, two unknowns and two equations — closed form. For any inelastic collision, momentum gives one equation and you need information about the inelasticity to close the system. For 2D collisions, momentum splits into two equations (one per axis), and you need either elasticity or geometric information to find the rest.

The **scale shift**: the same momentum-conservation principle covers a $0.057 \text{ kg}$ tennis ball at $55 \text{ m/s}$ ($p \sim 3 \text{ kg·m/s}$), a $1{,}500 \text{ kg}$ car at $30 \text{ m/s}$ ($p \sim 4.5 \times 10^4 \text{ kg·m/s}$), a $300{,}000 \text{ kg}$ Saturn V rocket on lift-off ($p \sim 10^9 \text{ kg·m/s}$ over the burn), and an electron in a particle collider ($p \sim 10^{-21} \text{ kg·m/s}$ at TeV energies). Across $30+$ orders of magnitude, $\mathbf{p}_{\text{total}}$ is conserved when no external forces act.

### A worked example using all three concepts — a rocket separation in space

A spacecraft of total mass $5{,}000 \text{ kg}$ is coasting at $1{,}000 \text{ m/s}$ in deep space (no significant external forces). It separates into two parts: a $3{,}000 \text{ kg}$ main body and a $2{,}000 \text{ kg}$ payload, with the payload propelled forward by a small spring-loaded ejector that imparts $50{,}000 \text{ J}$ of kinetic energy to the relative motion.

**Concept 1 (momentum):** Initial total momentum: $(5000)(1000) = 5 \times 10^6 \text{ kg·m/s}$.

**Concept 2 (conservation):** After separation: $3000 v_m + 2000 v_p = 5 \times 10^6$.

**Concept 3 (energy):** The spring imparted $50{,}000 \text{ J}$ to the *relative* motion. The kinetic energy of the system in its center-of-mass frame is what increased by $50{,}000 \text{ J}$. In the original frame:

$$\tfrac{1}{2}(3000) v_m^2 + \tfrac{1}{2}(2000) v_p^2 = \tfrac{1}{2}(5000)(1000)^2 + 50{,}000.$$

Right side: $2.5 \times 10^9 + 5 \times 10^4 = 2.50005 \times 10^9 \text{ J}$.

Two equations, two unknowns. Solving (algebra omitted): $v_p \approx 1{,}004.5 \text{ m/s}$, $v_m \approx 997 \text{ m/s}$.

The payload speeds up by $\sim 4.5 \text{ m/s}$; the main body slows by $\sim 3 \text{ m/s}$. The relative velocity is $\sim 7.5 \text{ m/s}$ — and this is exactly the kind of separation maneuver real spacecraft use to deploy payloads. The math is the same as for a rifle's recoil; only the scale changes.

---

## Exercises

### Warm-up

**8.1** *(LO 1)* A $2.0 \text{ kg}$ ball moves at $5.0 \text{ m/s}$. (a) What is its momentum? (b) What is its kinetic energy?

**8.2** *(LO 1)* A $0.15 \text{ kg}$ baseball is thrown at $40 \text{ m/s}$. The bat reverses its velocity, sending it back at $40 \text{ m/s}$. The contact lasts $1.5 \text{ ms}$. What is the average force on the ball during contact?

**8.3** *(LO 2)* A $50 \text{ kg}$ ice skater stands on frictionless ice and throws a $5.0 \text{ kg}$ ball horizontally at $10 \text{ m/s}$. What is the skater's recoil velocity?

**8.4** *(LO 4)* A $1{,}500 \text{ kg}$ car at $20 \text{ m/s}$ collides with and sticks to a stationary $1{,}500 \text{ kg}$ car. What is the combined post-collision velocity?

### Application

**8.5** *(LO 3)* A $0.50 \text{ kg}$ ball moving at $4.0 \text{ m/s}$ collides head-on elastically with a stationary $0.50 \text{ kg}$ ball. Find the velocities after.

**8.6** *(LO 3)* A $2.0 \text{ kg}$ ball at $3.0 \text{ m/s}$ collides head-on elastically with a stationary $1.0 \text{ kg}$ ball. Find the velocities after using $v_{1f} = \frac{m_1 - m_2}{m_1 + m_2} v_{1i}$ and $v_{2f} = \frac{2m_1}{m_1 + m_2} v_{1i}$.

**8.7** *(LO 5)* A $4 \text{ kg}$ object moving at $5 \text{ m/s}$ in the $+x$ direction collides with and sticks to a $3 \text{ kg}$ object moving at $4 \text{ m/s}$ in the $+y$ direction. Find the magnitude and direction of the combined velocity.

**8.8** *(LO 6)* A $0.005 \text{ kg}$ bullet is fired at $300 \text{ m/s}$ from a $4.0 \text{ kg}$ rifle. (a) What is the rifle's recoil velocity? (b) If the rifle is held against a $70 \text{ kg}$ shooter who absorbs the recoil over $0.10 \text{ s}$, what average force does the shooter feel?

### Synthesis

**8.9** *(LO 1, 4)* A $30 \text{ kg}$ child runs at $3.0 \text{ m/s}$ and jumps onto a stationary $5.0 \text{ kg}$ skateboard. (a) What is the post-jump velocity? (b) How much kinetic energy was lost? (c) Where did it go?

**8.10** *(LO 5)* In a billiards 2D collision, the cue ball (mass $0.165 \text{ kg}$) moving at $2.0 \text{ m/s}$ hits a stationary target ball of equal mass. The cue ball goes off at $30°$ above its original direction at $1.5 \text{ m/s}$. Find the velocity (magnitude and direction) of the target ball.

**8.11** *(LO 1, 6)* A $50 \text{ kg}$ astronaut is at rest in space, holding a $5 \text{ kg}$ wrench. She throws the wrench at $10 \text{ m/s}$ relative to herself (after release). (a) What is her velocity afterward (relative to the inertial frame)? (b) The astronaut needs to return to her ship $20 \text{ m}$ away — how long does that take after the throw?

### Challenge

**8.12** *(LO 6, beyond chapter)* A rocket with initial mass $10{,}000 \text{ kg}$ (including $8{,}000 \text{ kg}$ of fuel) ejects exhaust at $3{,}000 \text{ m/s}$ relative to itself. Use the Tsiolkovsky equation $\Delta v = v_e \ln(m_0 / m_f)$ to find the maximum velocity change the rocket can achieve (assume all fuel burns).

**8.13** *(beyond chapter)* In a particle physics experiment, a moving particle (mass $m$, velocity $v$) collides with a stationary particle (mass $M$). After the collision, two new particles emerge — one moving at angle $\theta_1$ above the original direction, the other at $\theta_2$ below. Using momentum conservation (no need to compute energy), set up the equations relating the four velocity magnitudes (initial $v$, final $v_1$, $v_2$, and effective masses) to the angles. State which quantities you'd need to measure to fully solve the system.

---

## LLM Exercise — Chapter 8: Momentum and Collisions in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A momentum-and-impulse analysis of a key collision or transfer event in your anchor phenomenon.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 8, I want to apply momentum conservation and impulse to one event in my phenomenon involving a transfer of motion or a collision. Please:

1. Identify ONE collision, impact, or momentum-transfer event. Examples:
   - Bike commute: pedaling — each pedal stroke transfers momentum from leg to chain to wheels. Or a sudden stop (brake = impulse).
   - Coffee maker: water hitting the puck (impulse on the grounds).
   - Basketball: ball bouncing off the floor (impulse with the floor); ball-rim collision.
   - Marathon: footstrike — each stride is an impulse from the ground.
   - Espresso: water hitting the puck at 9 bar; water exiting the basket as a stream.

2. Set up the momentum conservation. Identify all bodies in the "system." Are external forces negligible during the relevant time?

3. Compute the momentum change and the average force from impulse: $F = \Delta p / \Delta t$.

4. If the event is a collision, classify it: elastic, partially inelastic, or perfectly inelastic. Compute the energy lost.

5. Sanity check with one Fermi estimate.

6. Identify which simplification (negligible external forces, point masses, instantaneous transfer) is most likely to bite.

7. One sentence on how this connects to Chapter 9 (statics) — when momentum is constant at zero, you have static equilibrium.

Save the output as logbook/chapter-08-momentum.md.
```

### What this produces

An eighth Logbook entry: a momentum analysis of one event in your phenomenon, often revealing forces that are bigger than they look.

### How to adapt this prompt

- *For phenomena without obvious collisions* (a steady-state cup of coffee): focus on impulses (the impulse to lift it, the impulse from each sip).
- *For ChatGPT or Gemini:* identical with substitutions.
- *For Claude Code:* if you have force-time data (e.g., from a smart watch's accelerometer), import and integrate to get impulse.

### Connection to previous chapters

Builds on Chapter 4 (force) — impulse is force × time. Builds on Chapter 7 (energy) — collisions can lose energy but always conserve momentum. Vector decomposition from Chapter 3 returns for 2D collisions.

### Preview of next chapter

Chapter 9 introduces statics — the special case where total momentum is zero (nothing is moving) and total angular momentum is zero (nothing is rotating). The analysis that lets us solve dynamic collisions also lets us solve static structures.

---

## Chapter summary

Two conservation laws braided together. **Linear momentum** $\mathbf{p} = m\mathbf{v}$ is what changes when impulse is applied: $\mathbf{F} \Delta t = \Delta \mathbf{p}$. The **conservation of momentum** in isolated systems (no net external force) lets us predict the outcome of collisions, recoils, and rocket burns without knowing the internal dynamics in detail. **Elastic collisions** conserve both momentum and kinetic energy; **inelastic collisions** conserve only momentum. **2D collisions** are handled by applying momentum conservation along each axis separately.

The one idea that matters most: **internal forces don't change a system's total momentum.** Because of Newton's third law, every internal force-pair cancels in the system-wide sum. Only external forces can change $\mathbf{p}_{\text{total}}$. This is what makes "isolated system" a useful approximation: during a brief collision, external forces (gravity, friction) impart very small impulses compared to the contact forces, and momentum is approximately conserved.

The common mistake to watch for: **conflating elastic and inelastic.** Energy is conserved only in elastic collisions; momentum is conserved in both. Most everyday collisions (cars, sports balls, anything that makes a sound or warms up) are inelastic to some degree.

What you should now be able to teach someone else: how to compute momentum and impulse, how to apply conservation of momentum in 1D and 2D, how to distinguish elastic from inelastic collisions, and why airbags work (extending $\Delta t$ to reduce $F$ for the same $\Delta p$). Four skills, one underlying conservation principle.

---

## What would change my mind

The chapter argues that conservation of momentum is exact in isolated systems and a very good approximation in nearly-isolated systems (brief collisions where external forces' impulses are small). The argument would need revision if a measured collision in a well-isolated experimental setup ever showed a genuine non-conservation — historically, every apparent violation has been resolved by accounting for an unobserved particle or force, not by abandoning conservation.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **what does "isolation" even mean at the cosmological scale?** The total momentum of the universe — if the universe is finite — must be conserved. But the universe is expanding, and the cosmological reference frame is murky. Whether momentum conservation holds globally or only locally is a question general relativity addresses more carefully than Newton's framework can. We won't reach this until Chapter 33; until then, isolation is a useful local approximation.

---

## Connections forward

Chapter 9 (statics) treats the special case where momentum is zero everywhere. Chapter 10 (rotation) introduces *angular* momentum — the rotational analog, conserved separately. Chapter 31 (nuclear physics) is where momentum conservation does much of its modern work: every particle-physics calculation tracks momentum at every vertex. Chapter 28 (special relativity) modifies the definition of momentum to $\mathbf{p} = \gamma m \mathbf{v}$ at high speeds; conservation still holds, but the formula changes. The conservation principle is robust; only the specific expression evolves.

---

**Tags:** momentum, conservation, collisions, impulse, recoil

---

## AI Wayback Machine

**Christiaan Huygens** worked out the laws of elastic collisions in 1656 — establishing momentum conservation and the role of vector quantities decades before Newton's *Principia*. His work also produced the first pendulum clock.

**Run this:**

```
Who was Christiaan Huygens, and how does his work on collisions connect to momentum and collisions we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Christiaan Huygens"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Huygens's specific argument for momentum conservation in a two-ball elastic collision.
- Ask it about Huygens's wave theory of light — and the century-long contest with Newton's particle theory.

What changes? What gets better? What gets worse?
