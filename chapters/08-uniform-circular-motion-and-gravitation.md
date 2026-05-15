# Chapter 8 — Uniform Circular Motion and Gravitation

**Suggested titles**

1. Uniform Circular Motion and Gravitation
2. The Continuous Fall: Why the Moon Doesn't Hit Us
3. Centripetal Acceleration and the Inverse-Square Law

**TL;DR.** An object moving in a circle at constant speed is accelerating — toward the center, with magnitude $v^2/r$. That single insight unlocks orbital mechanics: a satellite stays in orbit because gravity continuously bends its path into a closed curve, and gravity does this with a force that drops as $1/r^2$ between any two masses. This chapter installs centripetal acceleration, applies it to cars on curved roads and astronauts in centrifuges, and then reaches for Newton's universal law of gravitation to explain everything from why apples fall to why the Moon orbits at the distance and period it does.

---

## A grapefruit in low Earth orbit, October 4, 1957

At 7:28 PM Moscow time on October 4, 1957, a Soviet R-7 rocket launched from a remote site in Kazakhstan and put a polished aluminum sphere — about the size of a beach ball, with four whip antennas trailing behind — into orbit around the Earth. The sphere weighed $83.6 \text{ kg}$. It transmitted a simple beep on two short-wave frequencies. Its name was *Sputnik 1*. It was the first artificial object to orbit a planet.

Three weeks later, *Sputnik 1* was still up there, circling the Earth every $96$ minutes, traveling at about $8 \text{ km/s}$. Hundreds of millions of people, on every continent, looked up at the right angles in the right hours and saw a small bright dot moving steadily across the sky. It was visible to the naked eye in the right twilight conditions. It did not look like much. It changed everything.

The puzzle for a thoughtful person on the ground was simple. The grapefruit was at $250 \text{ km}$ altitude. Earth's gravity is plenty strong at that altitude (still about $93\%$ of surface gravity). So why didn't *Sputnik 1* fall? Why was it staying up?

The answer is that *it was* falling. Continuously. At every instant, gravity was pulling it toward the Earth — exactly as it pulls anything else. But *Sputnik 1* was also moving sideways, fast enough that as it fell, the Earth curved away beneath it at the same rate it fell. The satellite was always falling and never landing. Newton had imagined this exact scenario in 1687 — a cannonball fired horizontally fast enough that the Earth's surface drops away beneath it as fast as it falls — and predicted, correctly, what would happen. Three centuries later, the Soviets did it.

This chapter is the physics of that prediction. Two pieces. First: an object moving in a circle at constant speed is accelerating, toward the center, by $v^2/r$ — even though its speed isn't changing. Second: gravity is a force that scales as $G m_1 m_2 / r^2$ between any two masses, falling off with the square of distance. Put the two together and you get orbital mechanics, Kepler's laws of planetary motion, the design of GPS satellites, and the entire architecture of celestial mechanics.

**Learning objectives.** By the end of this chapter you should be able to:

1. Convert between angular and linear quantities ($s = r\theta$, $v = r\omega$, $a_t = r\alpha$) for motion along a circular path.
2. Compute centripetal acceleration ($a_c = v^2/r = r\omega^2$) and centripetal force ($F_c = m v^2/r$) for any object in uniform circular motion.
3. Apply Newton's laws to circular-motion problems: cars on flat and banked curves, riders in vertical loops, planets in (approximately circular) orbits.
4. State Newton's universal law of gravitation $F = G m_1 m_2 / r^2$ and use it to compute gravitational forces, surface gravities, and orbital parameters.
5. Apply Kepler's third law $T^2 \propto r^3$ to compare orbital periods at different radii, and explain how it follows from Newton's law of gravitation.

**Prerequisites.** Chapter 4 (Newton's laws). Chapter 5 (friction provides the centripetal force on a flat curve). Vector decomposition from Chapter 3 (banked-curve forces). Comfort with the idea of acceleration as a *vector* — change in velocity, not just change in speed.

**Why this chapter matters.** Circular motion appears in every rotating system — planets, electrons in atoms (in the Bohr model), tires on cars, blades on turbines, stars in galaxies. Gravitation explains the structure of the solar system, the orbits of communication satellites, the trajectory of every spacecraft humans have launched, and (with relativistic corrections) the precession of Mercury and the bending of starlight. This chapter is the bridge between Newton's laws as a local rule and the planetary-scale physics that the rest of the universe runs on.

---

## Concept 1 — Angular quantities and centripetal acceleration

### A merry-go-round at the playground

Stand at the edge of a playground merry-go-round. A friend pushes it slowly. You feel yourself moving. Your feet trace a circle; your head traces a circle (slightly smaller, because it's closer to the axis); the rim of the platform you're standing on traces the largest circle of all. Each part of you moves at a different *linear* speed, but every part of you sweeps the same *angle* per second. The whole platform rotates as a rigid body. Some piece of vocabulary makes the situation describable: the angular vocabulary.

Once you have the angular vocabulary, an unexpected thing emerges from the geometry alone. Even though every point on the merry-go-round is moving at constant speed (assuming the rotation rate is constant), every point is also *accelerating* — toward the center. Acceleration is a vector; it measures change in velocity, and *direction is part of velocity*. A point on the platform whose direction of motion keeps changing (because it's tracing a circle) has a continuously changing velocity vector. The rate of change of that vector is the centripetal acceleration.

### The mechanism — angular and centripetal quantities

For an object moving along a circular path of radius $r$:

**Arc length** $\Delta s$: the distance traveled along the curve. Related to the angle swept ($\Delta\theta$, in radians):

$$\Delta s = r \, \Delta\theta.$$

(This is what a *radian* means: the angle that subtends an arc length equal to the radius.)

**Angular velocity** $\omega$: how fast the angle is changing.

$$\omega = \frac{\Delta\theta}{\Delta t}, \qquad \text{units: rad/s.}$$

**Linear (tangential) speed** $v$: how fast a point on the rotating object moves along its circular path.

$$v = r\omega.$$

So a point twice as far from the axis moves twice as fast at the same $\omega$.

**Period** $T$: the time for one full revolution. Since one revolution sweeps $2\pi$ radians:

$$T = \frac{2\pi}{\omega}.$$

**Centripetal acceleration** $a_c$: the inward-pointing acceleration of an object moving in a circle at constant speed.

$$a_c = \frac{v^2}{r} = r\omega^2.$$

The two forms are equivalent (substitute $v = r\omega$). Use whichever is more convenient.

The derivation is geometric. As the object moves through a small angle $\Delta\theta$, its velocity vector also rotates through that angle. The change in velocity vector $\Delta\mathbf{v}$ has magnitude $v \cdot \Delta\theta$ (for small $\Delta\theta$) and points toward the center of the circle. Divide by the time elapsed $\Delta t = \Delta\theta / \omega$ and you get $a = v\omega = v^2/r$. The direction is *toward* the center — that's why it's called "centripetal" (Latin for "center-seeking").

### The trade-off

The angular framework trades **familiar Cartesian intuition for rotational symmetry.** You give up some intuitive directionality (no fixed "x-axis" — every point on the wheel is treated as moving along its own arc) and pick up an enormous simplification: every point on a rigid rotating body shares the same $\omega$ and $\alpha$. Once you have those, the linear quantities at any radius follow from $r$.

### Worked example — centripetal acceleration of a car on a curve

A car drives around a curve of radius $r = 500 \text{ m}$ at a constant speed of $v = 25.0 \text{ m/s}$ (about $90 \text{ km/h}$). What is its centripetal acceleration?

$$a_c = \frac{v^2}{r} = \frac{(25.0)^2}{500} = \frac{625}{500} = 1.25 \text{ m/s}^2.$$

In units of $g$:

$$a_c / g = 1.25 / 9.80 \approx 0.13.$$

Your body, going around that curve, is being accelerated sideways at about $0.13 g$.

**Sanity check.** You can feel a $0.13 g$ sideways force, but it's not extreme — equivalent to leaning at about $7°$ from vertical. Driving fast on a freeway entrance ramp is a common everyday experience of a few tenths of $g$ centripetal acceleration. Tighter turns or higher speeds push it higher. Race cars routinely experience $2$–$5 g$ in turns; high-performance jets in tight maneuvers reach $8$–$9 g$, near the limit of human tolerance.

**The general lesson.** Centripetal acceleration scales linearly with radius (at constant $\omega$) but quadratically with speed (at constant $r$). Doubling your speed quadruples the centripetal acceleration — which is why slowing down helps you keep traction on a slippery curve so much more than tightening the turn would.

### Common misconceptions

- *"Constant speed means no acceleration."* Speed is the *magnitude* of velocity. Velocity is a vector. Direction is part of it. Constant speed with changing direction means changing velocity, which means nonzero acceleration. Uniform circular motion is the canonical case.
- *"Centripetal force is a new kind of force."* It isn't. *Centripetal* describes the *direction* of a net force in a circular-motion situation, not its physical origin. Whatever force happens to be pointing toward the center — friction, gravity, tension, normal force — is acting as the centripetal force.
- *"There's a centrifugal force pushing you outward in a turning car."* No. Inside the car (a non-inertial, accelerating frame), it *feels* like there's an outward push because your body is trying to continue in a straight line while the car turns under you. From the ground's frame, there is no outward force on you — just your own inertia carrying you straight, plus the inward force from the seat pushing you into the curve.

↳ **Dig Deeper — Why Earth's rotation flattens it (and the centrifugal effect on $g$)**

*Earth rotates once a day. That's slow, but at the equator it gives every object a tangential speed of about $465 \text{ m/s}$ and centripetal acceleration toward Earth's axis of about $0.034 \text{ m/s}^2$. This is one of the reasons measured surface $g$ is slightly smaller at the equator than at the poles — and it also explains why Earth is slightly flattened at the poles.*

**Prompt:**
> Compute the centripetal acceleration on an object at the equator due to Earth's daily rotation, given Earth's equatorial radius $\approx 6.378 \times 10^6 \text{ m}$ and rotation period $\approx 86{,}164 \text{ s}$ (the sidereal day). Then explain (a) why this means the apparent weight of an object at the equator is slightly less than at the poles, (b) by approximately what fraction (in parts per thousand), and (c) how this rotational effect contributes to Earth's equatorial bulge (oblateness). End with one sentence on what would happen to Earth's shape if its rotation rate doubled.

**What to do with the output:** Save it. The Earth-rotation effect is a beautiful place where centripetal-acceleration arithmetic meets geophysics. The Coriolis force (which produces hurricanes' rotation direction) follows the same logic and is worth a follow-up.

---

## Concept 2 — Centripetal force: what bends the path

### A car rounding a wet corner

Imagine a $1{,}500 \text{ kg}$ car on a flat road, taking a curve of radius $50 \text{ m}$ at $20 \text{ m/s}$ (about $72 \text{ km/h}$). What force is keeping the car on the curve? Specifically: what physical mechanism is producing the centripetal acceleration we just learned how to compute?

For a car on a flat road, the answer is *static friction* between the tires and the road surface. The tires exert a sideways friction force on the road; the road exerts an equal and opposite friction force on the tires (Newton's third law, again); that friction is the only horizontal force on the car; therefore that friction must be exactly the centripetal force that bends the car's path.

If the friction available isn't enough — wet road, icy patch, oily spot — the car can't bend its path tightly enough. The car slides outward, leaving the curve. *That* is what skidding off a corner physically means: the required centripetal force exceeded the maximum available friction, and the road could no longer redirect the car.

### The mechanism — Newton's second law for circular motion

Centripetal force is just $\mathbf{F}_{\text{net}} = m\mathbf{a}$ with $\mathbf{a} = a_c$ pointing toward the center of the circle:

$$F_c = m a_c = \frac{m v^2}{r} = m r \omega^2.$$

The *physical source* of $F_c$ varies with the situation. Some examples:

- **Car on flat curve:** $F_c$ provided by static friction between tires and road. Maximum: $\mu_s mg$.
- **Car on banked curve:** $F_c$ provided by the horizontal component of the normal force, optionally supplemented by friction.
- **Object on a string twirled in a horizontal circle:** $F_c$ provided by string tension.
- **Roller coaster at the top of a vertical loop:** $F_c$ provided by gravity (and possibly normal force from the track, depending on speed).
- **Moon orbiting Earth:** $F_c$ provided by gravity.
- **Electron orbiting a proton (in the Bohr model):** $F_c$ provided by electrostatic attraction.

The recipe is always the same: identify what physical force is pointing toward the center; equate it to $m v^2/r$; solve for whatever you don't know.

### The trade-off

The centripetal-force framework trades **a unified accounting** (one quantity, $F_c$) **for the work of identifying the physical mechanism in each case.** You can't just say "centripetal force does it" — you have to say *what* is supplying it. Friction? Gravity? Tension? The label "centripetal" describes the role; the physics tells you the actor.

### Worked example — minimum coefficient of friction for a curve

A $900 \text{ kg}$ car negotiates a flat curve of radius $500 \text{ m}$ at $25.0 \text{ m/s}$. What minimum coefficient of static friction is required between the tires and the road?

**Identify the centripetal force.** $F_c = \mu_s N = \mu_s mg$ (since on a flat road, $N = mg$).

**Set equal to required centripetal force.**

$$\mu_s mg = \frac{m v^2}{r}.$$

Mass cancels. Solve for $\mu_s$:

$$\mu_s = \frac{v^2}{rg} = \frac{(25.0)^2}{(500)(9.80)} = \frac{625}{4900} \approx 0.13.$$

A coefficient of $0.13$ is required.

**Sanity check.** From Chapter 5's table, dry concrete on rubber has $\mu_s \approx 1.0$ — far above the required $0.13$. Dry pavement: no problem. But wet concrete might drop $\mu_s$ to $\sim 0.7$, still fine. Ice with $\mu_s \approx 0.1$ is below the required value — and that's where the car slides. The threshold tells you which conditions are safe at this speed.

**The general lesson.** Mass cancels. The required friction coefficient depends only on speed, radius, and $g$. A truck and a Mini Cooper have the same skid threshold on the same curve. (In practice, tires, suspension, weight distribution, and load all matter — but the basic centripetal calculation gives you the leading-order answer.)

### Common misconceptions

- *"Heavier cars need more friction to go around the same curve."* No. Mass cancels. Required $\mu_s$ depends on $v$, $r$, $g$ — not $m$. (Loading does affect things in detail, but not in the simple model.)
- *"Banked curves use centripetal force; flat curves use friction."* Both use whatever force points toward the center. Banked curves redirect the normal force; flat curves use friction. Real curves often combine both for safety margin.
- *"Centripetal force pulls outward."* No, inward. The misnomer "centrifugal" (center-fleeing) refers to a fictitious force in non-inertial frames, not a real outward force.

↳ **Dig Deeper — Why banked curves work, and the ideal banking angle**

*A banked curve uses the geometry of the surface to make the normal force point partially toward the center of the curve, providing centripetal force without relying on friction. There's an "ideal banking angle" at which a car can navigate the curve at a specific speed even with zero friction — pure geometry.*

**Prompt:**
> Derive the ideal banking angle $\theta$ for a curve of radius $r$ taken at speed $v$, assuming no friction. Show by free-body analysis that the required angle satisfies $\tan\theta = v^2/(rg)$. Then compute the ideal banking angle for a freeway off-ramp of $r = 100 \text{ m}$ designed for $25 \text{ m/s}$ ($90 \text{ km/h}$). Finally, explain why real engineered curves are typically banked at less than the ideal angle for the design speed (hint: friction provides safety margin in both directions — slower vehicles also need to not slide *down* the bank).

**What to do with the output:** Save it. Banked-curve geometry is a beautiful merger of Newton's laws with practical engineering, and the same analysis applies to circular tracks for racing, the design of high-speed highway interchanges, and the inclined paths of cyclists in velodromes.

---

## Concept 3 — Newton's law of gravitation

### An apple, a moon, and a missing connection

The mythology says Newton sat under an apple tree and watched an apple fall. The reality is more interesting. Newton, around 1666, was thinking about why the Moon orbits the Earth instead of flying off in a straight line (Newton's first law) or crashing into the Earth. He had Kepler's three laws of planetary motion in front of him — empirical patterns Kepler had derived from Tycho Brahe's careful observations decades earlier. Newton wanted to *explain* Kepler's laws from a force.

His insight: the same force that pulls an apple to the ground might be what holds the Moon in its orbit. If gravity is a force between any two masses — not just between the Earth and stuff on its surface — then maybe it operates on the Moon too. And if gravity falls off with distance in the right way, it would produce exactly the orbital motion Kepler had described.

The "right way," it turned out, was the inverse square: $F \propto 1/r^2$. Newton showed mathematically that an inverse-square gravitational force, combined with his three laws of motion, produces orbits that are conic sections (ellipses, parabolas, hyperbolas — Kepler's first law), and that orbital periods scale as $T^2 \propto r^3$ (Kepler's third law). The math worked out exactly. The same force that ripens apples explains planetary motion.

### The mechanism — the universal law

**Newton's law of universal gravitation:** between any two point masses $m_1$ and $m_2$, separated by distance $r$, there is an attractive force along the line connecting them, with magnitude

$$F = G \frac{m_1 m_2}{r^2},$$

where $G$ is the **universal gravitational constant**:

$$G = 6.674 \times 10^{-11} \text{ N} \cdot \text{m}^2 / \text{kg}^2.$$

The smallness of $G$ tells you why gravity, despite being universal, is normally negligible between everyday objects. The gravitational force between two $1 \text{ kg}$ masses one meter apart is $G \approx 6.7 \times 10^{-11} \text{ N}$ — far less than your scale could ever measure. Gravity matters when at least one of the masses is huge: a planet, a star, a galaxy.

**For an extended body (like a planet),** the gravitational force on an external object behaves *as if* all of the body's mass were concentrated at its center. (This is a non-trivial result — Newton himself struggled with it for years before proving it with calculus.) For the Earth on an object near its surface:

$$F = G \frac{M_{\oplus} m}{R_{\oplus}^2} = m \cdot \left(\frac{G M_{\oplus}}{R_{\oplus}^2}\right) = mg,$$

where the bracketed quantity is exactly $g$. Plugging in $M_{\oplus} = 5.97 \times 10^{24} \text{ kg}$ and $R_{\oplus} = 6.378 \times 10^6 \text{ m}$:

$$g = \frac{(6.674 \times 10^{-11})(5.97 \times 10^{24})}{(6.378 \times 10^6)^2} \approx 9.80 \text{ m/s}^2.$$

Which is, of course, the value we've been using since Chapter 2.

### Orbits and Kepler's third law

For a satellite of mass $m$ in a circular orbit of radius $r$ around a much larger mass $M$, gravity provides the centripetal force:

$$G \frac{M m}{r^2} = \frac{m v^2}{r}.$$

Solve for $v$:

$$v = \sqrt{\frac{GM}{r}}.$$

The orbital speed depends only on the central mass and the orbital radius — not on the satellite's mass.

Period: $T = 2\pi r / v = 2\pi r / \sqrt{GM/r} = 2\pi \sqrt{r^3 / GM}$, so:

$$T^2 = \frac{4\pi^2}{GM} r^3.$$

This is **Kepler's third law**: $T^2 \propto r^3$. The proportionality constant ($4\pi^2 / GM$) depends on what you're orbiting, but the scaling holds for any system.

### The trade-off

Newton's law of gravitation trades **microscopic explanation for macroscopic predictive power.** The law tells you *what* gravity does between two masses — but not *why* mass attracts mass, or *how* the attraction is transmitted across empty space (action at a distance was a problem Newton himself didn't fully accept). The cost is a foundational mystery; the benefit is exact prediction of orbits, tides, falling objects, and the structure of the solar system. Three centuries later, general relativity replaced "force at a distance" with "curvature of spacetime" — but Newton's law remains an excellent approximation under almost all circumstances humans care about.

### Worked example — Moon's orbital period from Earth's mass

Given $M_{\oplus} = 5.97 \times 10^{24} \text{ kg}$ and the Moon's orbital radius $r_{\text{Moon}} = 3.84 \times 10^8 \text{ m}$, compute the Moon's orbital period.

$$T^2 = \frac{4\pi^2}{G M_{\oplus}} r^3 = \frac{4\pi^2}{(6.674 \times 10^{-11})(5.97 \times 10^{24})} \times (3.84 \times 10^8)^3.$$

Numerator: $4\pi^2 \approx 39.48$.

Denominator: $G M_{\oplus} \approx 3.986 \times 10^{14} \text{ m}^3/\text{s}^2$.

$r^3 = (3.84 \times 10^8)^3 \approx 5.66 \times 10^{25} \text{ m}^3$.

$$T^2 = \frac{39.48 \times 5.66 \times 10^{25}}{3.986 \times 10^{14}} = \frac{2.234 \times 10^{27}}{3.986 \times 10^{14}} \approx 5.61 \times 10^{12} \text{ s}^2.$$

$$T = \sqrt{5.61 \times 10^{12}} \approx 2.37 \times 10^6 \text{ s}.$$

Convert to days: $T \approx 2.37 \times 10^6 / 86{,}400 \approx 27.4$ days.

**Sanity check.** The Moon's actual orbital period (sidereal month) is $27.32$ days. We got $27.4$ — agreement to better than $0.3\%$. Newton's law, applied with one input (Earth's mass) and one geometric measurement (orbital radius), reproduces the Moon's period to three significant figures. That kind of agreement — across a factor of $10^8$ from Earth's surface to the Moon — is what made Newton's gravity overwhelming evidence for centuries.

**The general lesson.** The same equation that predicts a stone's fall predicts the Moon's orbit. The unification — terrestrial physics matching celestial physics — is what made Newton's *Principia* (1687) one of the most consequential books ever written.

### Common misconceptions

- *"Astronauts in orbit are weightless because there's no gravity."* No. At the ISS altitude ($\sim 400 \text{ km}$), Earth's gravitational acceleration is still about $89\%$ of its surface value. Astronauts are weightless because *they and the station are both in free fall* — falling toward Earth at the same rate, so they have no relative weight. They feel weightless the way you feel weightless during the brief fall on a roller coaster.
- *"Gravity propagates instantaneously."* Newton's law treats it that way, but in general relativity, gravity propagates at the speed of light. For most calculations, the difference is negligible.
- *"Heavier objects feel a stronger gravitational pull, so they should fall faster."* They do feel a stronger pull — but their inertia (also proportional to mass) is also larger, and the two cancel exactly, giving the same acceleration. This is the equivalence principle in disguise.

↳ **Dig Deeper — Geosynchronous orbit and the genius of Arthur C. Clarke**

*In 1945, science fiction writer Arthur C. Clarke proposed in a letter to Wireless World magazine that a satellite in a circular orbit at exactly the right altitude — about $36{,}000 \text{ km}$ — would have an orbital period of $24$ hours, and thus appear stationary above a fixed point on Earth's equator. This is geosynchronous orbit, and almost every weather and TV-broadcast satellite uses it. The altitude follows directly from Kepler's third law applied to Earth.*

**Prompt:**
> Use Kepler's third law $T^2 = (4\pi^2 / GM_{\oplus}) r^3$ to compute the orbital radius required for a $24$-hour orbital period around Earth (this is geosynchronous orbit). Convert to altitude above Earth's surface (subtract Earth's radius $\sim 6{,}378 \text{ km}$). Then explain (a) why the orbit must lie in Earth's equatorial plane to be truly "geostationary," (b) what specific applications require this orbit, and (c) what the orbital speed of a geostationary satellite is.

**What to do with the output:** Save it. The geosynchronous-orbit calculation is one of the most directly consequential applications of Kepler's third law. Clarke's 1945 paper is a beautiful piece of intellectual history.

---

## Synthesis — circles, gravity, and the prediction of orbits

Step back. Two pieces of physics:

**Centripetal acceleration** is the kinematic fact that anything moving in a circle at constant speed is accelerating toward the center, by $v^2/r$. The acceleration must come from a real force; what force depends on the situation. For a car on a flat curve, friction. For a satellite, gravity. For an electron in the Bohr-model atom, electrostatic attraction. Same algebraic structure, different physical actor.

**Gravity** is a universal force between any two masses, $F = G m_1 m_2 / r^2$, attractive, falling off with the square of distance. Combined with $F = m a_c$ for orbital motion, it produces Kepler's three laws — all of celestial mechanics emerges from this combination.

The **scale shift** I want you to feel: the same equations describe the centripetal acceleration of a child on a merry-go-round (radius $\sim 1 \text{ m}$, speed $\sim 1 \text{ m/s}$, $a_c \sim 1 \text{ m/s}^2$), a car on a freeway curve ($r \sim 500 \text{ m}$, $v \sim 25 \text{ m/s}$, $a_c \sim 1 \text{ m/s}^2$), the Moon orbiting Earth ($r \sim 4 \times 10^8 \text{ m}$, $v \sim 1{,}000 \text{ m/s}$, $a_c \sim 0.0027 \text{ m/s}^2$), and Earth orbiting the Sun ($r \sim 1.5 \times 10^{11} \text{ m}$, $v \sim 30{,}000 \text{ m/s}$, $a_c \sim 0.006 \text{ m/s}^2$). The vocabulary — radius, speed, period, central force — describes them all. The physics is invariant across $11$ orders of magnitude.

### A worked example using all three concepts — the speed of *Sputnik 1*

*Sputnik 1* orbited Earth at an altitude of about $250 \text{ km}$ above sea level. What was its orbital speed and period?

**Centripetal-gravitational balance.** At orbital altitude, the only significant force is gravity. It provides the centripetal acceleration. Setting $G M_{\oplus} m / r^2 = m v^2 / r$:

$$v = \sqrt{\frac{G M_{\oplus}}{r}}.$$

**Orbital radius.** Earth's radius is $R_{\oplus} \approx 6.378 \times 10^6 \text{ m}$, so:

$$r = R_{\oplus} + 250 \text{ km} = 6.378 \times 10^6 + 2.5 \times 10^5 \approx 6.628 \times 10^6 \text{ m}.$$

**Orbital speed.**

$$v = \sqrt{\frac{(6.674 \times 10^{-11})(5.97 \times 10^{24})}{6.628 \times 10^6}} = \sqrt{\frac{3.986 \times 10^{14}}{6.628 \times 10^6}} = \sqrt{6.014 \times 10^7} \approx 7{,}754 \text{ m/s}.$$

About $7.8 \text{ km/s}$ — consistent with what *Sputnik 1* actually traveled.

**Orbital period.**

$$T = \frac{2\pi r}{v} = \frac{2\pi \times 6.628 \times 10^6}{7{,}754} \approx 5{,}370 \text{ s} \approx 89.5 \text{ min}.$$

About $90$ minutes — close to the published $96$ minutes (the discrepancy is from Sputnik's actual orbit being elliptical, not circular, with apogee around $940 \text{ km}$ rather than the $250 \text{ km}$ perigee we used).

**Concept-by-concept.** Concept 1 (angular vocabulary, $v = r\omega$) lets us compute orbital period from speed and radius. Concept 2 (centripetal force = $mv^2/r$) tells us the force needed to bend the path. Concept 3 (Newton's law of gravitation) tells us what force is actually providing it. Together, they reduce a beach-ball-sized aluminum sphere in low Earth orbit to a closed-form calculation.

The same logic, different inputs, gives you: the speed of a GPS satellite (orbiting at $20{,}200 \text{ km}$ altitude), the orbital period of Mars (using the Sun's mass and Mars's distance), the rotation period of a binary star system. The framework is the same. Only the numbers change.

---

## Exercises

### Warm-up

**6.1** *(LO 1)* A bicycle wheel of radius $0.35 \text{ m}$ rotates at $10$ revolutions per second. (a) What is its angular velocity in rad/s? (b) What is the linear speed of a point on the rim?

**6.2** *(LO 2)* A $0.50 \text{ kg}$ stone tied to a string is whirled in a horizontal circle of radius $1.0 \text{ m}$ at $4.0 \text{ m/s}$. What is the tension in the string?

**6.3** *(LO 3)* A car rounds a flat curve of radius $40 \text{ m}$ at $20 \text{ m/s}$. What is the minimum coefficient of static friction required between tires and road?

**6.4** *(LO 4)* Compute the gravitational force between you ($70 \text{ kg}$) and a friend ($60 \text{ kg}$) sitting $1.0 \text{ m}$ apart. Compare to your weight on Earth.

### Application

**6.5** *(LO 2, 3)* A $1{,}000 \text{ kg}$ car drives over a hill of radius of curvature $50 \text{ m}$ at $15 \text{ m/s}$. (a) What is the centripetal acceleration at the top? (b) What is the normal force from the road at the top? (c) What is the maximum speed at which the car can crest the hill while still in contact with the road?

**6.6** *(LO 4)* Compute Earth's surface gravity from $g = G M_{\oplus} / R_{\oplus}^2$. Use $M_{\oplus} = 5.97 \times 10^{24} \text{ kg}$ and $R_{\oplus} = 6.378 \times 10^6 \text{ m}$. Compare to $9.80 \text{ m/s}^2$.

**6.7** *(LO 4, 5)* (a) Using $G$, $M_{\oplus}$, and the orbital radius of the ISS ($r \approx 6{,}778 \text{ km}$), compute its orbital speed. (b) Compute its orbital period. (c) The ISS appears to circle the Earth in about 90 minutes — does your answer match?

**6.8** *(LO 5)* Mars orbits the Sun at $r = 1.52$ AU with period $T_{\text{Mars}}$. Earth orbits at $r = 1.00$ AU with $T_{\text{Earth}} = 1$ year. Use Kepler's third law to compute $T_{\text{Mars}}$.

### Synthesis

**6.9** *(LO 1, 2, 3)* A $60 \text{ kg}$ pilot in a fighter jet pulls a tight banked turn of radius $200 \text{ m}$ at $150 \text{ m/s}$. (a) Compute the centripetal acceleration in m/s² and in $g$'s. (b) What is the centripetal force on the pilot? (c) What is the apparent weight she feels (the force from the seat)?

**6.10** *(LO 4, 5)* The Hubble Space Telescope orbits at $r \approx 6{,}918 \text{ km}$ from Earth's center. (a) Compute its orbital speed. (b) Compute its orbital period in minutes. (c) Per orbit, how far does it travel in km?

**6.11** *(LO 4, 5)* If you were on a planet with twice Earth's mass and the same radius as Earth, what would $g$ be? What would your weight be (you weigh $700 \text{ N}$ on Earth)? What if the planet had Earth's mass but half Earth's radius?

### Challenge

**6.12** *(LO 5, beyond chapter)* Compute the radius required for a geosynchronous orbit (period exactly $24 \text{ h}$) around Earth using Kepler's third law. Convert to altitude above sea level. Compare to the published $35{,}786 \text{ km}$ altitude.

**6.13** *(beyond chapter)* The Sun has mass $M_{\odot} = 1.989 \times 10^{30} \text{ kg}$. Pluto orbits at average $r = 5.91 \times 10^{12} \text{ m}$. (a) Compute Pluto's orbital period. (b) Compute its orbital speed. (c) Compare both to Earth's orbital values. (d) Comment on why Pluto orbits much more slowly: which scaling in Kepler's third law dominates?

---

## LLM Exercise — Chapter 6: Circular Motion in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A circular-motion or gravitational analysis of one element of your anchor phenomenon.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 6, I want to apply uniform circular motion (centripetal acceleration, $a_c = v^2/r$) and/or Newton's gravitation to my phenomenon. Please:

1. Identify ONE circular or rotational element in my phenomenon. Examples:
   - Bike commute: cornering on the bike — what's the centripetal acceleration on a typical curve, and what minimum friction does it require?
   - Coffee maker: a centrifugal pump or a spinning grinder — what centripetal force on a coffee particle?
   - Basketball: spin on the ball during the shot — what's the centripetal acceleration of a point on the surface?
   - Marathon: running on a curved track section — what centripetal force on the runner?
   - Espresso: the orbit of a coffee particle in the puck during 9-bar extraction (any vortex flow). Or the rotation of a milk frother.

2. Compute the relevant quantities ($v$ or $\omega$, $r$, $a_c$, $F_c$). Identify what physical force provides $F_c$.

3. Express $a_c$ in units of $g$ as a sanity check.

4. Identify any gravitational effects in your phenomenon (the most common: weight as the dominant downward force, but also potentially tidal effects, gravity assist, orbital motion if your phenomenon involves space).

5. One Fermi-style sanity check.

6. Identify which assumption (uniform circular motion, neglected gravity, neglected drag) is most likely to bite.

7. One sentence on how this connects to Chapter 7 (work and energy) — circular motion at constant speed does no net work; why?

Save the output as logbook/chapter-06-circular-and-gravitation.md.
```

### What this produces

A sixth Logbook entry: a circular-motion analysis applied to your phenomenon, often surprising in magnitude (small radii at moderate speeds give large $a_c$).

### How to adapt this prompt

- *For phenomena with no obvious circular component* (a straight-line marathon, a vertical pour): bring in Earth's rotation or the Earth-Sun gravitational force as the gravitational element.
- *For ChatGPT or Gemini:* identical with interface substitutions.
- *For Claude Code:* if you have angular-velocity or RPM data, paste it; ask for centripetal force and required friction.

### Connection to previous chapters

Builds directly on Chapter 4 (force, $F = ma$) and Chapter 5 (friction often provides centripetal force). Newton's law of gravitation is a specific application of force from Chapter 4.

### Preview of next chapter

Chapter 7 introduces work and energy as alternative bookkeeping for mechanical systems. Circular motion is interesting for energy: at constant speed, no net work is done (force is perpendicular to motion), even though force is applied continuously. Gravity, in contrast, does substantial work when objects fall.

---

## Chapter summary

Two pieces of physics, one tightly braided pair. **Centripetal acceleration** $a_c = v^2/r$, directed toward the center of a circular path, is what an object in uniform circular motion experiences — a kinematic fact, derivable from the geometry of changing direction at constant speed. **Newton's law of universal gravitation** $F = G m_1 m_2 / r^2$, an attractive inverse-square force between any two masses, is the physical law that supplies that centripetal force in the case of orbital motion. Combined, they predict Kepler's three laws of planetary motion and the orbits of every satellite humans have launched.

The one idea that matters most: **circular motion at constant speed is accelerated motion.** Acceleration is a vector; constant speed is not the same as constant velocity. The centripetal acceleration $v^2/r$ requires a real force to supply it — and identifying *what* supplies that force (friction, tension, gravity, normal force, electromagnetic) is the work of any specific problem.

The common mistake to watch for: **invoking centrifugal force as if it were a real outward force.** In an accelerating reference frame (a turning car, a rotating platform), it *feels* like an outward push — but from any inertial frame, the force is inward (centripetal), and the apparent outward push is your body's inertia trying to continue in a straight line.

What you should now be able to teach someone else: how to compute centripetal acceleration from speed and radius, how to identify what physical force is supplying the centripetal force in any given scenario, how to apply Newton's law of gravitation to compute either a force or an orbital parameter, and how to use Kepler's third law to compare two orbits. Four skills, one underlying idea: gravity does the work of bending paths into closed curves, and centripetal acceleration is the geometric description of what those curves require.

---

## What would change my mind

The chapter argues that Newton's law of gravitation is exact within the regime of weak fields and slow motion that includes essentially all engineering and most astronomy. The argument would need revision if anomalies in solar-system-scale gravitational predictions (e.g., the Pioneer anomaly, dark-matter substructure puzzles) turned out to require modifications to Newton's $1/r^2$ law itself, rather than to the assumptions that go into applying it.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is the gravitational force exactly proportional to mass?** Inertial mass (the $m$ in $F = ma$) and gravitational mass (the $m$ in $F = GMm/r^2$) are conceptually distinct quantities. Their equality is what makes all objects fall at the same rate (the masses cancel in $a = F/m$). Newton noted the equality but had no explanation. Einstein's general relativity makes their equality a foundational principle (the equivalence principle) — and reframes gravity itself as not a force at all but the curvature of spacetime. We will not get there until Chapter 33, but the gift of mass-independent acceleration is sitting under the surface of every result in this chapter.

---

## Connections forward

Chapter 7 introduces work and energy. A surprising fact emerges: the gravitational force does *no* net work on a satellite in a perfectly circular orbit (the force is always perpendicular to the motion), but it does substantial work on objects in elliptical orbits or falling toward the central mass. Chapter 8 (momentum) treats two-body problems where Newton's third law makes both the central mass and the satellite move (a star and planet both orbit their common center of mass). Chapter 10 (rotational motion) generalizes the angular-velocity vocabulary of this chapter to extended rotating bodies and introduces angular momentum — a conserved quantity that explains why Kepler's second law holds (areas swept in equal times). Chapter 33 returns to gravity at the deepest level: Einstein's general relativity replaces Newton's force with curved spacetime, refining (not overturning) the predictions used in this chapter.

---

**Tags:** circular-motion, gravitation, Keplers-laws, centripetal-acceleration, orbits

---

## AI Wayback Machine

**Johannes Kepler** worked out the three laws of planetary motion between 1609 and 1619 — elliptical orbits, equal areas in equal times, and the period-radius relation. He did the work using Tycho Brahe's painstaking observational records and roughly 40 years before Newton supplied the gravitational explanation.

**Run this:**

```
Who was Johannes Kepler, and how do his laws of planetary motion connect to uniform circular motion and gravitation we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Johannes Kepler"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how Newton's universal gravitation actually derives Kepler's three laws.
- Ask it about Kepler's day job casting horoscopes — and how he reconciled that with empirical astronomy.

What changes? What gets better? What gets worse?
