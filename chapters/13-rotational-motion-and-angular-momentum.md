# Chapter 13 — Rotational Motion and Angular Momentum

**Suggested titles**

1. Rotational Motion and Angular Momentum
2. The Skater Pulls Her Arms In
3. Why Tornadoes Spin Up

**TL;DR.** This chapter generalizes everything in mechanics from translation to rotation. Position becomes angle, velocity becomes angular velocity, mass becomes moment of inertia, force becomes torque, momentum becomes angular momentum. The structure is exactly parallel — and so are the conservation laws. Angular momentum $L = I\omega$ is conserved when no external torque acts. That's why ice skaters spin faster when they pull their arms in, why tornadoes accelerate when air masses contract, and why a spinning top doesn't fall over.

---

## A figure skater at the World Championships, March 2010

Yu-Na Kim of South Korea is in the middle of her free skate at the 2010 Winter Olympics in Vancouver. She is in a high-speed combination spin. Arms outstretched, leg extended — slow, graceful rotation, maybe two revolutions per second. Then she pulls her arms tightly into her chest and brings her free leg in close to her body. She accelerates. Within a second she is rotating much faster — perhaps four or five revolutions per second — fast enough that her face becomes a blur on television.

She did not push against anything. No external torque acted on her (ice friction is small enough to ignore over the second of the maneuver). Yet her angular velocity changed dramatically. Where did the angular acceleration come from?

The answer is conservation of angular momentum, $L = I\omega$. By pulling her arms in, the skater reduced her **moment of inertia** $I$ — the rotational analog of mass, which measures how the mass of her body is distributed relative to her axis of rotation. Mass close to the axis contributes less to $I$ than mass far from the axis. Pulling her arms in moved mass closer; $I$ dropped. Because $L$ is conserved (no external torque), and $L = I\omega$, when $I$ shrinks, $\omega$ must grow proportionally. The product stays constant.

The same physics explains why a tornado spins up as it tightens — air mass moving inward toward a center reduces the rotating system's moment of inertia, increasing its angular velocity. The same physics explains why pulsars (collapsed neutron stars) rotate with periods of milliseconds: a star the size of the Sun (radius $\sim 10^9 \text{ m}$) collapsing to a neutron star (radius $\sim 10^4 \text{ m}$) reduces $I$ by a factor of $10^{10}$, and $\omega$ grows by the same factor. A star that rotates once a month becomes a neutron star that rotates a hundred times a second.

This chapter is about rotation. Linear motion was Chapters 2–8. Rotational motion is the same physics, with new symbols and one major new conservation law. By the end you will have a parallel vocabulary, a parallel set of equations, and the ability to apply them to anything that turns.

**Learning objectives.** By the end of this chapter you should be able to:

1. Convert between linear and angular kinematics: $s = r\theta$, $v = r\omega$, $a_t = r\alpha$.
2. Apply the rotational kinematic equations (parallel to Chapter 2's translational ones) for constant angular acceleration.
3. Compute moment of inertia $I$ for simple shapes and apply $\tau = I\alpha$ (rotational Newton's second law).
4. Compute rotational kinetic energy $KE_{\text{rot}} = \tfrac{1}{2} I \omega^2$ and apply energy conservation including rotation.
5. Compute angular momentum $L = I\omega$ and apply conservation of angular momentum to spinning systems.

**Prerequisites.** Chapter 6 (uniform circular motion, $\omega$, $a_c$). Chapter 7 (kinetic energy). Chapter 8 (linear momentum, conservation). Chapter 9 (torque, $\tau = rF\sin\theta$).

**Why this chapter matters.** Anything that rotates uses this physics: tires, fans, gyroscopes, planets, stars, galaxies, electrons in atoms (in the quantum-mechanical analog). Engines and motors are rotational systems. The conservation of angular momentum is one of the three foundational conservation laws of mechanics (alongside energy and linear momentum). It explains pulsars, ice skaters, and the stability of spinning tops. It is also why bicycles balance — a moving wheel has angular momentum that resists tipping.

---

## Concept 1 — Rotational kinematics: the parallel language

### A motorcycle wheel from rest to highway speed

A motorcycle accelerates from rest. The rear wheel, of radius $0.30 \text{ m}$, spins up from $0$ to $30 \text{ m/s}$ at the rim — the bike's road speed — in $5 \text{ seconds}$. What is happening rotationally?

The wheel's angular velocity $\omega$ at any instant is related to the linear speed of a point on the rim by $v = r\omega$. So at the start: $\omega = 0$. At $t = 5 \text{ s}$: $\omega = v/r = 30/0.30 = 100 \text{ rad/s}$ (about 16 revolutions per second).

The angular acceleration: $\alpha = \Delta \omega / \Delta t = 100/5 = 20 \text{ rad/s}^2$.

The angle the wheel turned through during the acceleration: using rotational kinematics, $\theta = \tfrac{1}{2} \alpha t^2 = \tfrac{1}{2}(20)(25) = 250 \text{ rad} \approx 40 \text{ revolutions}$.

If you've worked the kinematics chapter (Chapter 2) carefully, every step here looks familiar. The equations are identical to translational kinematics with $\theta$ in place of $x$, $\omega$ in place of $v$, $\alpha$ in place of $a$.

### The mechanism — rotational kinematic equations

For a rotating body with constant angular acceleration $\alpha$:

$$\omega = \omega_0 + \alpha t,$$
$$\theta = \theta_0 + \omega_0 t + \tfrac{1}{2} \alpha t^2,$$
$$\omega^2 = \omega_0^2 + 2\alpha (\theta - \theta_0).$$

Linear-rotational analogies:
- Position $x \leftrightarrow$ angle $\theta$
- Velocity $v \leftrightarrow$ angular velocity $\omega$
- Acceleration $a \leftrightarrow$ angular acceleration $\alpha$

For a point at distance $r$ from the rotation axis:
- $s = r\theta$ (arc length)
- $v = r\omega$ (tangential speed)
- $a_t = r\alpha$ (tangential acceleration)
- $a_c = v^2/r = r\omega^2$ (centripetal acceleration, from Chapter 6)

The total acceleration of a point on a rotating body has two components: tangential (changing speed along the circle) and centripetal (changing direction). They're perpendicular, so $a_{\text{total}} = \sqrt{a_t^2 + a_c^2}$.

### The trade-off

Rotational kinematics trades **a separate set of formulas to memorize** for **the same mathematical structure as translational kinematics, just with new symbols**. Once you've internalized the analogy, no new memorization is needed — solve any rotational kinematics problem with the corresponding translational equation, swapping the symbols. The cost is the moment of mental translation; the benefit is recognizing that rotation is structurally the same as translation.

### Worked example — a CD spinning down

A CD spinning at $200 \text{ rpm}$ (revolutions per minute) is unplugged and slows uniformly to a stop in $30 \text{ s}$. (a) What is the initial angular velocity in rad/s? (b) What is the angular deceleration? (c) How many revolutions does the CD make before stopping?

**Convert.** $200 \text{ rpm} = 200 \times (2\pi / 60) \text{ rad/s} \approx 20.9 \text{ rad/s}$.

**Angular deceleration.** $\alpha = (\omega_f - \omega_i)/t = (0 - 20.9)/30 = -0.70 \text{ rad/s}^2$.

**Total angle.** $\theta = \tfrac{1}{2}(\omega_i + \omega_f) t = \tfrac{1}{2}(20.9 + 0)(30) = 314 \text{ rad}$. Convert: $314/(2\pi) = 50$ revolutions.

The CD makes about $50$ more revolutions before stopping.

**Sanity check.** It started at $200/60 \approx 3.3$ rev/s and slowed to zero over $30 \text{ s}$ — average rate $\sim 1.7$ rev/s, times $30 \text{ s}$ = $50$ revolutions. Consistent.

### Common misconceptions

- *"Angular velocity is just RPM."* RPM is one unit; rad/s is another. The SI unit is rad/s. $1 \text{ rev/s} = 2\pi \text{ rad/s}$. Always check units before applying equations.
- *"Tangential and centripetal are the same."* They aren't. Tangential acceleration changes the *speed* of motion around the circle; centripetal acceleration changes the *direction* (always toward the center). Both can be nonzero simultaneously when something is speeding up while turning.

↳ **Dig Deeper — Why "radian" is the right unit**

*The radian is defined as the angle subtended by an arc length equal to the radius. This makes $s = r\theta$ exact (no conversion factor). Other angle units — degrees, revolutions — require conversion factors and obscure the connection. The radian's mathematical naturalness is why physicists default to it.*

**Prompt:**
> Explain why the radian is the "natural" unit for angles in physics, by walking through how using degrees would force conversion factors into every linear-rotational relationship ($s = r\theta$, $v = r\omega$, $a_t = r\alpha$). Show one specific example: compute the linear speed at the rim of a 0.5 m wheel rotating at 60 RPM, doing the calculation (a) with $\omega$ in rad/s, (b) with $\omega$ in degrees/s, (c) with $\omega$ in rev/s. End with one sentence on what this means for the small-angle approximation $\sin\theta \approx \theta$ (which only works for $\theta$ in radians).

**What to do with the output:** Save it. The "radians as natural" insight returns in oscillations (Ch. 16) and in any chapter using small-angle approximations.

---

## Concept 2 — Rotational dynamics: $\tau = I\alpha$

### Pushing a merry-go-round close to vs. far from the center

You're standing at a playground merry-go-round. Push the rim — even a gentle push — and it spins up. Push the same hard at the center hub — it barely moves. Same force; very different rotational effect.

This is what Chapter 9 introduced as torque: $\tau = rF\sin\theta$. Force times perpendicular distance from the pivot. Now we ask the dynamic question: given a torque, *how much* angular acceleration results?

The answer parallels Newton's second law, with appropriate analog symbols. Where translational dynamics has $F = ma$ — net force equals mass times acceleration — rotational dynamics has:

$$\tau_{\text{net}} = I \alpha,$$

where $I$ is the **moment of inertia** (rotational analog of mass) and $\alpha$ is angular acceleration. The harder you push (larger torque), the faster the angular acceleration. The more massive and spread-out the object (larger $I$), the slower it accelerates.

### The mechanism — moment of inertia

Mass tells you how hard it is to translate something. Moment of inertia tells you how hard it is to rotate something — and crucially, it depends on *where the mass is* relative to the rotation axis.

For a point mass $m$ at distance $r$ from the axis:

$$I = m r^2.$$

For an extended body, sum (or integrate) over all the mass:

$$I = \sum m_i r_i^2.$$

For continuous bodies, this becomes an integral. Common shapes have tabulated results:

- Solid disk or cylinder, axis through center: $I = \tfrac{1}{2} M R^2$.
- Hoop or cylinder shell, axis through center: $I = M R^2$.
- Solid sphere: $I = \tfrac{2}{5} M R^2$.
- Thin rod, axis through center: $I = \tfrac{1}{12} M L^2$.
- Thin rod, axis through end: $I = \tfrac{1}{3} M L^2$.

Notice: same mass and size, different shapes, different $I$. A solid disk has half the moment of inertia of a hoop of the same mass and radius — the disk's mass is distributed throughout the interior, while the hoop's is concentrated at the rim.

This is why rolling races between objects of the same mass and radius have a winner: the one with smaller $I$ converts more of its potential energy into translational motion (less into rotational). A solid disk beats a hoop down a ramp, every time.

### The trade-off

The rotational dynamics framework trades **a single quantity (mass)** for **a quantity that depends on geometry and rotation axis (moment of inertia).** $I$ is harder to compute; you need to know how the mass is distributed. The benefit: with $I$ in hand, every rotational problem reduces to the same machinery as Chapter 4's translational dynamics.

### Worked example — torque needed to spin up a merry-go-round

A playground merry-go-round is approximately a solid disk of mass $M = 200 \text{ kg}$ and radius $R = 1.5 \text{ m}$. A child pushes it tangentially at the rim with a force of $50 \text{ N}$. What is the angular acceleration?

**Moment of inertia.** $I = \tfrac{1}{2} M R^2 = \tfrac{1}{2}(200)(1.5)^2 = 225 \text{ kg·m}^2$.

**Torque.** Push tangentially at the rim, $\theta = 90°$, $\tau = R F = (1.5)(50) = 75 \text{ N·m}$.

**Angular acceleration.** $\alpha = \tau / I = 75 / 225 \approx 0.33 \text{ rad/s}^2$.

In one second, the merry-go-round gains $0.33 \text{ rad/s} \approx 0.05 \text{ rev/s}$ of angular velocity. After $30 \text{ s}$ of pushing, it's spinning at $\sim 1.6 \text{ rev/s}$ — about 96 RPM. Realistic for a merry-go-round being pushed steadily.

**Sanity check.** A $50 \text{ N}$ push (about 11 lbf) is light — a child's effort. The acceleration is small. But over time, even small angular accelerations add up to substantial spin.

### Common misconceptions

- *"Moment of inertia depends only on mass."* It depends on mass *and* on how mass is distributed. Two objects of equal mass but different shapes have different $I$.
- *"$I$ is the same regardless of axis."* No. The moment of inertia of a rod about an axis through its end is $\tfrac{1}{3} M L^2$; about an axis through its center, $\tfrac{1}{12} M L^2$. The axis matters.

↳ **Dig Deeper — Rolling vs. sliding: kinetic energy partition**

*An object rolling without slipping has both translational kinetic energy ($\tfrac{1}{2} M v^2$) and rotational kinetic energy ($\tfrac{1}{2} I \omega^2$). For a given total energy (e.g., from a height $h$), how that energy partitions between the two depends on the object's shape — and that determines whether it wins a rolling race.*

**Prompt:**
> Compare the speeds at the bottom of an incline of height $h$ for: (a) a sliding block (no friction, no rotation), (b) a solid disk rolling without slipping, (c) a hoop rolling without slipping. Use energy conservation $mgh = KE_{\text{trans}} + KE_{\text{rot}}$ with the rolling constraint $v = R\omega$ for the rolling cases. Show that the sliding block wins, the disk comes second, and the hoop comes last. End with one sentence on why this is independent of mass and radius (only the *fraction* $I/(MR^2)$ matters).

**What to do with the output:** Save it. The rolling-race physics is one of the cleanest demonstrations that moment-of-inertia geometry matters as much as mass.

---

## Concept 3 — Angular momentum and its conservation

### The pulsar in the Crab Nebula

In 1054 AD, Chinese and Arab astronomers recorded a sudden bright "guest star" in the constellation Taurus. It was visible in daylight for $23$ days and remained visible at night for nearly two years. Today, in the same location, we see the **Crab Nebula** — an expanding cloud of gas, the remnants of a supernova explosion. At its center is a tiny, dense object: a **neutron star**, the collapsed core of the original star, with mass roughly $1.4$ solar masses packed into a radius of about $10 \text{ km}$.

The neutron star is rotating. Fast. It rotates about $30$ times per second. We know because it sends pulses of radiation toward Earth that we detect with each rotation — it is a *pulsar*. Its angular velocity is about $190 \text{ rad/s}$.

How did it spin so fast? The original star, before collapse, was rotating much more slowly — perhaps once per month. But the original star was also much larger, with radius $\sim 7 \times 10^8 \text{ m}$ (typical for a Sun-like star). When the star's core collapsed, its radius shrank to $\sim 10^4 \text{ m}$ — a factor of $7 \times 10^4$ smaller. Moment of inertia, scaling as $R^2$, shrank by a factor of $\sim 5 \times 10^9$.

If angular momentum was conserved during the collapse (and to first approximation, it was — no external torque acts on a collapsing star), then the angular velocity must have grown by the same factor. A rotation period of one month becomes a rotation period of $\sim$ one month / $5 \times 10^9 \approx 5 \times 10^{-7}$ seconds, or $0.5 \text{ μs}$ — actually faster than the observed $30 \text{ ms}$, which is consistent with some loss of mass and outer-shell fly-off during the collapse.

This is conservation of angular momentum at its most dramatic. The same principle that lets the ice skater speed up by pulling her arms in lets a star speed up by collapsing.

### The mechanism — angular momentum and conservation

**Angular momentum** of a rotating body:

$$L = I \omega.$$

Units: $\text{kg·m}^2/\text{s}$. Vector quantity; direction along the rotation axis (right-hand rule).

For a point particle in motion (not a rotating extended body), the angular momentum about a chosen pivot is:

$$L = m v r_\perp,$$

where $r_\perp$ is the perpendicular distance from the pivot to the line of motion.

**Conservation of angular momentum:** in the absence of external torques, the total angular momentum of a system is constant.

$$L_i = L_f \quad \implies \quad I_i \omega_i = I_f \omega_f.$$

This is the rotational analog of conservation of linear momentum. The proof parallels: $\tau = dL/dt$ (analogous to $F = dp/dt$); if $\tau_{\text{net}} = 0$, $L$ is constant.

For a system that changes shape (skater pulling arms in, star collapsing): $I$ changes, $\omega$ adjusts so $I\omega$ stays the same. If $I$ halves, $\omega$ doubles. If $I$ shrinks by $10^{10}$, $\omega$ grows by $10^{10}$.

### The trade-off

Angular momentum conservation trades **the need to track every torque during a complicated process** for **a single conserved quantity at the start and end.** The cost: $L$ is sometimes counterintuitive (it's a vector along the axis, perpendicular to the rotation plane). The benefit: powerful predictions about systems in transition (skaters, collapsing stars, gyroscopes, planets being perturbed).

### Worked example — the spinning skater

A figure skater spinning at $1.5 \text{ rev/s}$ has her arms extended ($I = 4.0 \text{ kg·m}^2$). She pulls them in tight ($I = 1.0 \text{ kg·m}^2$). Assuming no external torque, what is her new angular velocity?

**Conservation of angular momentum.** $I_i \omega_i = I_f \omega_f$.

$$(4.0)(1.5 \text{ rev/s}) = (1.0) \omega_f \implies \omega_f = 6.0 \text{ rev/s}.$$

She quadruples her spin rate when she pulls her arms in (because $I$ shrank by a factor of $4$).

**Energy check.** $KE_i = \tfrac{1}{2}(4.0)(2\pi \times 1.5)^2 = \tfrac{1}{2}(4.0)(88.8) = 178 \text{ J}$. $KE_f = \tfrac{1}{2}(1.0)(2\pi \times 6.0)^2 = \tfrac{1}{2}(1.0)(1421) = 711 \text{ J}$. Kinetic energy *increased* by a factor of $4$.

Where did the energy come from? Her muscles did work pulling her arms in against the (apparent) outward push of rotation. In her rotating reference frame, she's pulling against centrifugal force; in the inertial frame, she's doing work to bring mass inward against angular-momentum-conserving dynamics. Either way, work was done — and that work appears as additional kinetic energy.

**Sanity check.** Yu-Na Kim's spin acceleration in our chapter opener was about a factor of $2$–$3$ — reasonable for partial arm-pulling. Champion spinners (like the legendary Lucinda Ruh, who held the world record for spin speed) exceed factors of $4$ by extreme body compaction.

### Common misconceptions

- *"Angular momentum is conserved automatically, regardless of forces."* No — it's conserved only if no *external torque* acts. Internal forces (the skater pulling her own arms) don't change it; gravity (vertical, no torque about the vertical spin axis) doesn't change it; ice friction (small but real) eventually does.
- *"Angular momentum and linear momentum are the same."* No — different conservation laws. A car driving in a straight line has linear momentum but no angular momentum about any point on its line of motion. A spinning top in place has angular momentum but zero linear momentum.

↳ **Dig Deeper — Why a bicycle stays up: gyroscopic effects and angular momentum**

*A moving bicycle wheel is essentially a spinning gyroscope. The angular momentum of the wheel resists changes in its orientation — including the kind of toppling that would cause a stationary bike to fall. The bicycle's stability has surprising layers: the gyroscopic effect contributes, but so do trail (the steering geometry) and the rider's active control.*

**Prompt:**
> Explain how gyroscopic effects contribute to the stability of a moving bicycle. Walk through (a) the angular momentum of a spinning wheel pointing along its axle (right-hand rule), (b) the effect of trying to tilt the bike — the gyroscopic precession redirects the angular momentum, making the front wheel turn in a way that helps the bike stay upright. Then mention recent research (e.g., Schwab et al., 2007, who built a bike with no gyroscopic stability that still stayed up) that suggests gyroscopic effects are real but not the only or even main source of bicycle stability. End with one sentence on why physics-of-bicycles is still an open research area.

**What to do with the output:** Save it. The bicycle-stability question is a great example where the textbook answer ("gyroscopic precession") is partly true but not the whole story.

---

## Synthesis — rotation as the parallel pillar of mechanics

Step back. Everything in linear mechanics has a rotational analog:

| Linear | Rotational |
|---|---|
| Position $x$ | Angle $\theta$ |
| Velocity $v$ | Angular velocity $\omega$ |
| Acceleration $a$ | Angular acceleration $\alpha$ |
| Mass $m$ | Moment of inertia $I$ |
| Force $F$ | Torque $\tau$ |
| $F = ma$ | $\tau = I\alpha$ |
| Momentum $p = mv$ | Angular momentum $L = I\omega$ |
| KE $= \tfrac{1}{2}mv^2$ | $KE_{\text{rot}} = \tfrac{1}{2}I\omega^2$ |
| Conservation of $\mathbf{p}$ (no $\mathbf{F}_{\text{ext}}$) | Conservation of $\mathbf{L}$ (no $\boldsymbol{\tau}_{\text{ext}}$) |

This is not coincidence. The rotational quantities are derived from the linear quantities applied to point masses on a rotating body, with $r$ playing a key role. Once you have the linear framework, the rotational one is structural.

The **scale shift** I want you to feel: angular momentum conservation works for a child on a playground merry-go-round ($L \sim 100 \text{ kg·m}^2/\text{s}$), an ice skater spinning ($L \sim 10 \text{ kg·m}^2/\text{s}$), a freely spinning satellite ($L \sim 10^3 \text{ kg·m}^2/\text{s}$), Earth's rotation ($L \sim 7 \times 10^{33} \text{ kg·m}^2/\text{s}$), and a neutron star (much greater per unit mass). The same principle. The same algebra. Across $30+$ orders of magnitude.

### A worked example using all three concepts — a bowling ball striking pins

A $7.0 \text{ kg}$ bowling ball moving at $7.0 \text{ m/s}$ strikes a $1.5 \text{ kg}$ pin standing $0.40 \text{ m}$ tall. The pin can be treated as a uniform rod, with the impact at the top. Find the pin's angular velocity immediately after the collision (treat as inelastic, ball loses negligible speed).

**Concept 1 — kinematics of pin.** Rod length $L = 0.40 \text{ m}$. After collision, the pin pivots at its bottom (held by friction with the floor for the instant).

**Concept 2 — moment of inertia of pin.** As a uniform rod about its end: $I = \tfrac{1}{3} M L^2 = \tfrac{1}{3}(1.5)(0.40)^2 = 0.080 \text{ kg·m}^2$.

**Concept 3 — angular momentum balance.** Before: ball has angular momentum about the pin's pivot $L_i = m_b v_b L = (7.0)(7.0)(0.40) = 19.6 \text{ kg·m}^2/\text{s}$. The pin is at rest. After: ball still moving (negligible speed change), pin spinning. To estimate the pin's $\omega$, treat the impact as imparting $\Delta L \approx$ small fraction of $L_i$ to the pin (in a real bowling collision, much of the ball's linear momentum is transferred — but for a pure angular-momentum analysis assume some fraction $f$ is transferred):

If $\sim 30\%$ of the ball's angular momentum about the pivot transfers (a typical value for a glancing strike): $L_{\text{pin}} = 0.3 \times 19.6 = 5.9 \text{ kg·m}^2/\text{s}$.

Then $\omega_{\text{pin}} = L_{\text{pin}} / I = 5.9 / 0.080 \approx 74 \text{ rad/s}$, or about $12 \text{ rev/s}$. The pin will tip over very quickly (ground friction stops the spin within a fraction of a second, but it tips first).

**Sanity check.** This is a rough estimate — bowling-pin physics is much more complex than a clean angular-momentum transfer (collisions are partially elastic, the pin doesn't rotate cleanly about its base). But the order-of-magnitude says: small pin moment of inertia + nontrivial angular momentum transfer → very fast spin → quick tip-over. Exactly what bowling pins do.

The synthesis exercises all three concepts: kinematics relates $v$ at the rim to $\omega$ of the rotation; moment of inertia tells you how the pin resists rotation; angular momentum (combined with conservation as much as friction allows) tells you how fast it ends up spinning.

---

## Exercises

### Warm-up

**10.1** *(LO 1)* A wheel of radius $0.40 \text{ m}$ rotates at $20 \text{ rad/s}$. (a) What is the linear speed of a point on the rim? (b) What is its angular velocity in RPM?

**10.2** *(LO 1, 2)* A flywheel accelerates from $10 \text{ rad/s}$ to $30 \text{ rad/s}$ in $5.0 \text{ s}$. (a) Angular acceleration? (b) Angle turned through in those 5 seconds?

**10.3** *(LO 3)* A solid disk of mass $5.0 \text{ kg}$ and radius $0.30 \text{ m}$ is rotated by a torque of $10 \text{ N·m}$ applied at the rim. What is its angular acceleration?

**10.4** *(LO 5)* A spinning ice skater has $I = 5.0 \text{ kg·m}^2$ and $\omega = 4.0 \text{ rad/s}$. What is her angular momentum?

### Application

**10.5** *(LO 4)* A solid sphere of mass $2.0 \text{ kg}$ and radius $0.10 \text{ m}$ rolls without slipping at $5.0 \text{ m/s}$. Compute (a) its translational KE, (b) its rotational KE, (c) the total KE, (d) the fraction in rotation.

**10.6** *(LO 3, 4)* A solid disk of mass $3.0 \text{ kg}$ and radius $0.50 \text{ m}$ rolls without slipping down a $30°$ incline of height $2.0 \text{ m}$. (a) Use energy conservation to find the speed at the bottom. (b) Compare to a frictionless slide of the same height.

**10.7** *(LO 5)* A merry-go-round (solid disk, $200 \text{ kg}$, $1.5 \text{ m}$ radius) is spinning at $1.0 \text{ rad/s}$. A $40 \text{ kg}$ child jumps on at the rim. (a) New angular velocity? (b) How much KE was lost? (c) Where did it go?

**10.8** *(LO 5)* An astronaut floating in space holds a spinning bicycle wheel ($I = 0.50 \text{ kg·m}^2$, $\omega = 30 \text{ rad/s}$). She inverts it (flips its axis $180°$). The astronaut + wheel system has $I_{\text{astronaut}} = 4.0 \text{ kg·m}^2$ about the same axis. What angular velocity does the astronaut acquire?

### Synthesis

**10.9** *(LO 1, 2, 3, 4)* A car wheel of mass $20 \text{ kg}$ and radius $0.30 \text{ m}$ spins up from rest as the car accelerates from $0$ to $25 \text{ m/s}$ in $8 \text{ s}$ (no slipping). Compute: (a) the angular acceleration, (b) the angular displacement during the acceleration, (c) the moment of inertia of the wheel (treat as a solid disk), (d) the torque applied to the wheel.

**10.10** *(LO 2, 4, 5)* A solid disk of mass $0.50 \text{ kg}$ and radius $0.20 \text{ m}$ falls down from a string wound around its rim (Maxwell's wheel). (a) What is the linear acceleration of its center as it falls? (b) After falling $1.0 \text{ m}$, what is its translational KE? Rotational KE?

**10.11** *(LO 5)* A neutron star with mass $1.4$ solar masses and radius $10 \text{ km}$ spins at $30 \text{ Hz}$. (a) Compute its angular momentum (treat as a uniform sphere, $I = \tfrac{2}{5} MR^2$). (b) The original progenitor star had radius $7 \times 10^8 \text{ m}$; what was its rotation period before collapse, assuming angular momentum was conserved?

### Challenge

**10.12** *(beyond chapter)* A figure skater holds her arms out, $I = 5 \text{ kg·m}^2$, spinning at $2 \text{ rev/s}$. She pulls her arms in to $I = 1 \text{ kg·m}^2$. Compute (a) her new angular velocity, (b) the kinetic energy before and after, (c) the work she did pulling her arms in. (d) Show that the work equals the increase in rotational KE.

**10.13** *(beyond chapter)* A gyroscope wheel of $I = 0.10 \text{ kg·m}^2$ spinning at $200 \text{ rad/s}$ is mounted on a horizontal axle that is supported only at one end (free at the other). The wheel weighs $2.0 \text{ kg}$ and the axle from support to wheel center is $0.20 \text{ m}$. Compute the precession rate $\Omega = MgL/(I\omega)$. (Express in rad/s and in revolutions per minute.)

---

## LLM Exercise — Chapter 10: Rotational Motion in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A rotational analysis of one rotating element of your anchor phenomenon, with $I$, $\omega$, $L$, and $KE_{\text{rot}}$ computed.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 10, I want to apply rotational dynamics — moment of inertia, angular acceleration, angular momentum — to one rotating element of my phenomenon. Please:

1. Identify ONE rotating component in my phenomenon. Examples:
   - Bike commute: the wheel rotation, which has moment of inertia and angular momentum.
   - Coffee maker: a centrifugal pump impeller; a rotating burr grinder.
   - Basketball: the ball's spin during the shot (back-spin or side-spin).
   - Marathon: a runner's swinging arms (modeled as rotating rods).
   - Espresso: a rotating tamper or a spinning piston in the pump.

2. Compute the moment of inertia $I$ using the appropriate formula for the shape (disk, hoop, sphere, rod). State the formula.

3. Compute the angular velocity $\omega$ from the linear velocity (using $v = r\omega$) or from RPM data.

4. Compute the angular momentum $L = I\omega$ and the rotational kinetic energy $KE_{\text{rot}} = \tfrac{1}{2} I\omega^2$.

5. If a torque is involved (acceleration), compute it from $\tau = I\alpha$.

6. Sanity-check with one Fermi estimate.

7. Identify which assumption (rigid body, no slip, axis through center) is most likely to bite.

8. One sentence on how this connects to Chapter 11 (fluid statics) — fluids don't rotate as rigid bodies, so the moment-of-inertia framework needs modification.

Save the output as logbook/chapter-10-rotation.md.
```

### What this produces

A tenth Logbook entry: a rotational-dynamics analysis applied to your phenomenon, often surprising in how much energy is "locked up" in rotation.

### How to adapt this prompt

- *For phenomena with no obvious rotation* (a vertical pour): treat the curl/vortex of any flowing fluid as quasi-rotational; or examine an oscillating system as rotational about its pivot.
- *For ChatGPT or Gemini:* identical with substitutions.
- *For Claude Code:* if you have video of a spinning object, paste frame-time data and let Claude compute angular velocity from frame analysis.

### Connection to previous chapters

Builds directly on Chapter 6 (uniform circular motion). Adds angular acceleration and dynamics. Generalizes Chapters 4 (force), 7 (KE), 8 (momentum) to rotational form.

### Preview of next chapter

Chapter 11 begins fluids — both static and flowing. Fluids don't rotate as rigid bodies (different parts can have different angular velocities); the rotational framework needs to be extended into vorticity. But the energy and momentum frameworks carry over.

---

## Chapter summary

Rotational motion is structurally identical to translational motion, with new symbols. **Position** becomes angle; **velocity** becomes angular velocity; **mass** becomes moment of inertia; **force** becomes torque; **momentum** becomes angular momentum; the equations are exactly parallel. The new conservation law — **conservation of angular momentum** — is independent of linear momentum conservation and explains a wide range of phenomena from ice skater spins to neutron star formation.

The one idea that matters most: **moment of inertia depends on how mass is distributed relative to the rotation axis, not just total mass.** This is what makes a hoop and a disk of the same mass rotate differently, and what lets a skater control her spin rate by changing her body shape.

The common mistake to watch for: **forgetting to specify the rotation axis when computing $I$.** Without the axis, the moment of inertia is undefined. The same object has different $I$ about different axes — a rod about its center has $\tfrac{1}{12} M L^2$, about its end $\tfrac{1}{3} M L^2$.

What you should now be able to teach someone else: how to translate between linear and angular kinematic quantities, how to apply $\tau = I\alpha$ for rotational dynamics, how to compute rotational kinetic energy and angular momentum, and how angular momentum conservation explains spin-up phenomena from skaters to pulsars. Five skills, one organizing principle: every linear quantity has an angular analog, and the conservation laws survive intact.

---

## What would change my mind

The chapter argues that classical rotational mechanics, applied via the moment-of-inertia / angular-momentum framework, is sufficient for nearly all engineering and astronomical-scale problems. The argument would need revision if a class of common rotational problems systematically required corrections beyond rigid-body dynamics — they often need corrections (deformable bodies, coupled rotations, gyroscopic precession in detail), but those layer on the framework, not replace it.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why are angular momentum and linear momentum independent conservation laws?** Both come from Noether's theorem (linear from spatial-translation symmetry, angular from rotational symmetry). They are independent because translations and rotations are independent symmetries of space. Yet at the deepest physical level, this independence is itself surprising — why does space have both kinds of symmetry? General relativity weaves them together more deeply (curvature can mix translations and rotations), but classical mechanics treats them as separate. The answer to *why* is structural; the answer to *how to use them* is the content of this chapter.

---

## Connections forward

Chapter 11 introduces fluid statics — fluids at rest. Fluids can't be treated as rigid bodies; they deform under any shear. But pressure as a scalar quantity playing the role of "force per unit area" gives us a clean framework. Chapter 12 extends to flowing fluids — and any flow can be decomposed into translation, rotation, and deformation, each handled by extensions of the rigid-body machinery here. Chapter 16 (oscillations) uses the rotational framework for the motion of pendulums and torsional oscillators. Chapter 33 (general relativity) returns to rotation in the context of frame-dragging by rotating black holes — angular momentum at extreme scales.

---

**Tags:** rotation, angular-momentum, moment-of-inertia, conservation, torque

---

## AI Wayback Machine

**Emmy Noether** proved in 1915 that every continuous symmetry of a physical system corresponds to a conservation law — including the connection between rotational symmetry and angular momentum conservation. The theorem is a foundation of modern physics; she was a Jewish woman who could not hold a salaried university position in Germany.

**Run this:**

```
Who was Emmy Noether, and how does Noether's theorem connect to the angular momentum we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about her career or ideas.
```

→ Search **"Emmy Noether"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through what Noether's theorem says about three specific symmetries — time, space, rotation — and the conservation laws each implies.
- Ask it about the institutional barriers Noether navigated as a Jewish woman at Göttingen and Bryn Mawr.

What changes? What gets better? What gets worse?
