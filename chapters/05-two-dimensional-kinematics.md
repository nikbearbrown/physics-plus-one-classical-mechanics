# Chapter 5 — Two-Dimensional Kinematics

**Suggested titles**

1. Two-Dimensional Kinematics
2. The Cannon, the Curve, and the Independence of Axes
3. Why Galileo's Two Coins Hit the Floor Together

**TL;DR.** Once motion stops being a straight line, you need vectors — quantities that carry both *how much* and *which way*. This chapter teaches the bookkeeping (components, addition, the Pythagorean reconstruction) and then unleashes the central result: horizontal and vertical motion are independent. From that single fact the entire arc of a thrown ball, a fired shell, a long jump, and the path of an airliner across a crosswind all fall out.

---

## A coin flicked off a desk, a coin nudged off the edge

A physics professor stands at the front of a lecture hall with two identical coins on the corner of her desk. She puts one finger on the first coin and a second finger on the second. With one quick motion, she flicks the first coin horizontally — it sails out in a graceful arc, lands a meter away with a clear *clink*. At the same instant, she nudges the second coin off the edge — it falls straight down and lands directly below the desk corner with its own *clink*.

Two clinks. One arrived a meter out. The other arrived directly below. They sounded at the same time.

Most students hear it but don't believe it. Surely the coin that travelled farther took longer? It went farther through the air; air is air; more air, more time. Try it yourself, with a coin and a ruler on the edge of a table: flick one coin, push the other off at the same moment. Listen.

The clinks are simultaneous because the horizontal motion does not affect the vertical motion. Each coin falls under gravity at the same rate, $g = 9.80 \text{ m/s}^2$, regardless of how fast it is also moving sideways. The flicked coin had a horizontal velocity. That changed *where* it landed, not *when*. Sideways speed and downward fall are independent. They do not negotiate with one another.

This is the most important fact in two-dimensional kinematics, and Galileo was the first to write it down clearly. Once you have it, every projectile problem in this book — a fireworks shell, an arrow loosed at a target, a basketball arcing toward the rim, a shell from a battleship cannon — collapses into two one-dimensional problems running in parallel. You already know how to solve those.

**Learning objectives.** By the end of this chapter you should be able to:

1. Resolve a two-dimensional vector into perpendicular components using $A_x = A\cos\theta$ and $A_y = A\sin\theta$, and reconstruct a vector from its components using the Pythagorean theorem.
2. Add vectors analytically: components along each axis add as ordinary numbers, and the resultant is recovered from those summed components.
3. Apply the principle that horizontal and vertical motions are independent — they share only time — and use it to set up projectile-motion problems.
4. Solve full projectile problems: range, peak height, flight time, and impact velocity for any launch angle and speed.
5. Add velocities using the same vector method to handle relative motion (a boat in a current, a plane in a crosswind).

**Prerequisites.** Chapter 1 (units, uncertainty, sig figs). Chapter 2 (kinematic equations, free fall). Right-triangle trigonometry: $\sin$, $\cos$, $\tan$, and $\tan^{-1}$. Comfort with the Pythagorean theorem.

**Why this chapter matters.** Real motion is not a straight line. A ball arcs. A car turns. A planet orbits. Every later chapter that involves motion in more than one direction — projectile problems, circular motion (Chapter 6), orbits, magnetic forces on charges (Chapter 22) — leans on the vector methods this chapter installs. If kinematics in 1D was the alphabet, kinematics in 2D is the first sentence.

---

## Concept 1 — Vectors: how a quantity gets a direction

### A pedestrian on a city grid

Imagine a person at the corner of 9th Street and Main. They want to reach a coffee shop at the corner of 18th Street and 5th Avenue. The streets run east-west; the avenues, north-south; every block is the same length. A helicopter could fly the diagonal — straight from start to coffee. A pedestrian cannot. They walk 9 blocks east on Main, then 5 blocks north on 18th. Total walked: 14 blocks. Straight-line distance from start to finish: less.

How much less? The two legs form the legs of a right triangle, and the diagonal is the hypotenuse:

$$d = \sqrt{(9)^2 + (5)^2} = \sqrt{81 + 25} = \sqrt{106} \approx 10.3 \text{ blocks}.$$

The pedestrian walked $14$ blocks; the helicopter would fly $10.3$. That difference — $3.7$ blocks of extra walking — is the price of being constrained to a grid.

This is the simplest case of two-dimensional motion. We did not just need a number ($14$ blocks); we needed two numbers (9 east, 5 north) to say where they ended up. A single number cannot capture motion that has direction in a plane. We need a richer object: a *vector*.

### The mechanism — what a vector is, what its components are

A **vector** is a quantity that has both a magnitude (a size, a number with units) and a direction. Position, displacement, velocity, acceleration, force, and momentum are all vectors. Mass, time, temperature, energy — those are *scalars*: they have a magnitude only.

We draw vectors as arrows. The length of the arrow is proportional to the magnitude. The direction of the arrow is the direction of the vector. If you draw a 5-cm arrow pointing northeast to represent a 5-meter displacement northeast, then a 10-meter displacement east would be a 10-cm arrow pointing east.

In writing, we mark vectors with boldface ($\mathbf{A}$) or sometimes an arrow on top ($\vec{A}$). The magnitude alone is written in italics ($A$). The direction is given by an angle $\theta$ from some chosen reference axis — usually east, or the positive $x$-axis.

Now the central trick. Any 2D vector $\mathbf{A}$ pointing in some general direction can be expressed as the sum of two perpendicular vectors — one along the $x$-axis ($\mathbf{A}_x$) and one along the $y$-axis ($\mathbf{A}_y$):

$$\mathbf{A} = \mathbf{A}_x + \mathbf{A}_y.$$

These are the **components** of $\mathbf{A}$. If $\mathbf{A}$ has magnitude $A$ and points at angle $\theta$ above the $x$-axis, the components are found from right-triangle trigonometry:

$$A_x = A \cos\theta, \qquad A_y = A \sin\theta.$$

Going the other way — from components back to magnitude and direction — is the Pythagorean theorem:

$$A = \sqrt{A_x^2 + A_y^2}, \qquad \theta = \tan^{-1}\!\left(\frac{A_y}{A_x}\right).$$

Notice what the components let you do. Adding two vectors $\mathbf{A}$ and $\mathbf{B}$ that point in different directions looks hard if you stay in arrow-and-protractor mode. But once you split each into components, the bookkeeping is trivial: components along the same axis add as ordinary numbers.

$$R_x = A_x + B_x, \qquad R_y = A_y + B_y.$$

Then reconstruct the resultant $\mathbf{R}$ with the Pythagorean theorem and arctangent. That's it. Every vector-addition problem in this book follows this recipe.

### The trade-off

The component method trades **geometric intuition for arithmetic discipline.** A protractor and a ruler will get you a vector sum to within a degree or two — which is fine for sketching, useless for engineering. The component method gives you the answer to whatever precision your inputs allow, but it requires you to trust the algebra and lose, for the moment, the visual sense of where the resultant points. Sketch the situation first to anchor your intuition, then compute.

### Worked example — adding two displacements analytically

A hiker walks $53.0 \text{ m}$ in a direction $20.0°$ north of east, then $34.0 \text{ m}$ in a direction $63.0°$ north of east. Where does she end up relative to her starting point?

**Choose axes.** Let $x$ be east, $y$ be north.

**Resolve each leg into components.**

$$A_x = (53.0)\cos(20.0°) = (53.0)(0.940) = 49.8 \text{ m},$$
$$A_y = (53.0)\sin(20.0°) = (53.0)(0.342) = 18.1 \text{ m}.$$

$$B_x = (34.0)\cos(63.0°) = (34.0)(0.454) = 15.4 \text{ m},$$
$$B_y = (34.0)\sin(63.0°) = (34.0)(0.891) = 30.3 \text{ m}.$$

**Add the components.**

$$R_x = 49.8 + 15.4 = 65.2 \text{ m},$$
$$R_y = 18.1 + 30.3 = 48.4 \text{ m}.$$

**Reconstruct the resultant.**

$$R = \sqrt{(65.2)^2 + (48.4)^2} = \sqrt{4251 + 2343} = \sqrt{6594} \approx 81.2 \text{ m}.$$

$$\theta = \tan^{-1}(48.4 / 65.2) = \tan^{-1}(0.742) \approx 36.6°.$$

She is $81.2 \text{ m}$ from her starting point, in a direction $36.6°$ north of east.

**Sanity check.** She walked a total of $87 \text{ m}$ along a path that bent slightly northward. The straight-line distance has to be less than that ($87$) and not too much less, because the two legs were close in direction. $81.2 \text{ m}$ fits. The angle ($36.6°$) sits between $20°$ and $63°$, weighted toward the longer first leg. Both checks pass.

### Common misconceptions

- *"The magnitudes of components add to the magnitude of the vector."* No. $A_x + A_y \neq A$. The components add as *vectors* to give $\mathbf{A}$, but the Pythagorean reconstruction is what gives the magnitude. For a vector with $A_x = 3$ and $A_y = 4$, $A = 5$ — not $7$.
- *"You always use $\cos$ for $x$ and $\sin$ for $y$."* True only when $\theta$ is measured from the $x$-axis. If you measure $\theta$ from the $y$-axis instead, the trig functions swap. Always draw the triangle and label which side is opposite, which is adjacent, before reaching for $\sin$ or $\cos$.

↳ **Dig Deeper — Why is the component decomposition unique?**

*The chapter asserts that any 2D vector can be split into two perpendicular components in exactly one way (once you've fixed the axes). This is not obvious, and the argument has consequences for every later use of vectors — including how forces decompose along inclined planes.*

**Prompt:**
> Explain why the decomposition of a 2D vector into perpendicular components along a chosen pair of axes is unique. What changes if the axes are not perpendicular (oblique components)? Walk through one worked example showing that a vector decomposed along non-perpendicular axes also has a unique decomposition, but the formulas $A_x = A\cos\theta$, $A_y = A\sin\theta$ no longer apply. End with one sentence on why physicists almost always choose perpendicular axes.

**What to do with the output:** Save it. The same uniqueness argument supports writing forces as sums of components on inclined planes (Chapter 5) and decomposing electric fields along arbitrary axes (Chapter 18).

---

## Concept 2 — Independence of perpendicular motions

### The strobe-lit pair: dropped vs. thrown

In 1948 Harold Edgerton, the MIT engineer who made strobe photography famous, captured two billiard balls falling side by side. One was simply released from rest. The other was thrown horizontally at the same instant from the same height. The strobe flashed every $1/30$ of a second; the camera recorded a track of dots showing each ball's position at each flash.

The dropped ball appeared as a vertical column of dots, getting farther apart toward the bottom (because it accelerated). The thrown ball appeared as a parabolic curve of dots, also getting farther apart toward the bottom.

Here is the part that catches you: at every flash, the two balls were at the same *height*. The horizontal positions differed — the thrown ball had moved sideways. But vertically, every flash showed them level with each other. The thrown ball was falling at exactly the same rate as the dropped ball, despite having sideways speed.

The strobe photograph is a one-frame proof of what Galileo argued by reasoning alone four centuries earlier: **horizontal velocity does not affect vertical fall**. Gravity pulls only downward. There is no horizontal component of gravity to change horizontal motion, and there is no horizontal component of motion to change vertical fall.

### The mechanism — solving a 2D problem as two 1D problems

Take any object moving in two dimensions under gravity alone. Resolve its initial velocity into components: $v_{0x}$ horizontal, $v_{0y}$ vertical. Then write the kinematic equations *separately* for each axis.

**Horizontal motion** — gravity has no horizontal component, so $a_x = 0$. The horizontal motion is uniform:

$$x = x_0 + v_{0x} t,$$
$$v_x = v_{0x} = \text{constant}.$$

**Vertical motion** — gravity acts downward. Taking up as positive, $a_y = -g$. The vertical motion is constant-acceleration kinematics from Chapter 2:

$$y = y_0 + v_{0y} t - \tfrac{1}{2} g t^2,$$
$$v_y = v_{0y} - g t,$$
$$v_y^2 = v_{0y}^2 - 2 g (y - y_0).$$

The two systems of equations share only one variable: $t$. Time ticks at the same rate in both directions. This is what couples them; this is also what lets you solve them separately. Find $t$ from one (usually vertical, since gravity sets the timeline), substitute into the other.

That is the entire algorithm for projectile motion. Resolve into components. Apply 1D kinematics to each. Recombine if needed.

### The trade-off

This treatment of projectiles trades **realism for tractability.** We've assumed no air resistance. In real life, a thrown ball loses speed to drag — more for light objects, more for high speeds, more for non-streamlined shapes. A baseball pitched at $40 \text{ m/s}$ loses meaningful speed before reaching home plate; an artillery shell on a long arc spends much of its energy fighting air. The vacuum-projectile equations are excellent for short flights of dense objects (a thrown rock, a long jumper, a basketball over the rim) and progressively worse otherwise. We use them where they're good and reach for computer simulation when they aren't.

### Worked example — the fireworks shell

A fireworks shell is launched at $v_0 = 70.0 \text{ m/s}$ at an angle of $75.0°$ above horizontal. Its fuse is timed to ignite at the peak of its trajectory. (a) How high does it explode? (b) When does it explode? (c) How far horizontally has it traveled by then?

**Resolve the initial velocity into components.**

$$v_{0x} = (70.0)\cos(75.0°) = (70.0)(0.259) = 18.1 \text{ m/s},$$
$$v_{0y} = (70.0)\sin(75.0°) = (70.0)(0.966) = 67.6 \text{ m/s}.$$

**Find the peak height.** At the peak, $v_y = 0$. Using $v_y^2 = v_{0y}^2 - 2g(y - y_0)$ with $y_0 = 0$:

$$0 = (67.6)^2 - 2(9.80)\, y,$$
$$y = \frac{(67.6)^2}{2(9.80)} = \frac{4570}{19.6} \approx 233 \text{ m}.$$

**Find the time to peak.** From $v_y = v_{0y} - g t$ with $v_y = 0$:

$$t_{\text{peak}} = \frac{v_{0y}}{g} = \frac{67.6}{9.80} \approx 6.90 \text{ s}.$$

**Find the horizontal distance at that time.** Horizontal motion is uniform at $v_{0x} = 18.1 \text{ m/s}$:

$$x = v_{0x}\, t_{\text{peak}} = (18.1)(6.90) \approx 125 \text{ m}.$$

So the shell explodes about $233 \text{ m}$ up, $6.90 \text{ s}$ after launch, and $125 \text{ m}$ downrange. (Once it explodes, drag dominates; the fragments do not follow projectile equations any further.)

**Sanity check.** $233 \text{ m}$ is a reasonable height for large professional fireworks (commercial display shells often peak between $200$ and $400$ meters). The flight time of about seven seconds matches what you observe at any fireworks show — count between launch *thump* and the burst. The numbers make sense.

**The general lesson.** Once you've resolved the initial velocity into components, gravity only touches the vertical equations. The horizontal answer is always just $x = v_{0x}\, t$. Find $t$ from the vertical condition you care about (peak when $v_y = 0$; landing when $y$ returns to its initial value; etc.), then substitute.

### Common misconceptions

- *"The horizontal velocity changes during flight."* Only because of air resistance. In the no-air idealization we're using, horizontal velocity is *constant* throughout the entire flight, even at the peak. The shell at its apex still has $v_x = 18.1 \text{ m/s}$.
- *"At the peak, gravity has stopped acting."* No. Velocity is zero in the vertical direction; acceleration is still $-9.80 \text{ m/s}^2$ downward. That's exactly *why* the shell starts to descend — gravity has been pulling all along, and at the peak it has just finished cancelling the upward velocity and is about to make it negative.

↳ **Dig Deeper — The range equation and why $45°$ wins**

*From the kinematic equations you can derive a closed-form expression for projectile range on level ground: $R = v_0^2 \sin(2\theta_0) / g$. The result is famous, the derivation short, and the consequence — that $45°$ launch maximizes range — is so widely repeated it deserves a careful look at when it actually holds.*

**Prompt:**
> Derive the projectile range equation $R = v_0^2 \sin(2\theta_0) / g$ from the kinematic equations for level-ground launch and landing. Then explain (a) why $\theta_0 = 45°$ gives the maximum range, (b) why the maximum-range angle drops to about $38°$ when air resistance is included, and (c) why a shotputter releasing from above ground level (about 2 m) optimizes at an angle below $45°$ even with no air. End with one sentence on what kinds of athletic events the $45°$ result actually predicts well.

**What to do with the output:** Save it. The pattern — a clean theoretical answer, modified by realistic conditions — recurs whenever physics meets engineering. The same shape of correction shows up for orbital launch angles in aerospace.

---

## Concept 3 — Adding velocities: motion relative to motion

### A canoe pointing across a river

You launch a canoe from the east bank of a river. You point the bow due west and paddle steadily, keeping the bow aimed straight across. You expect to arrive directly opposite your launch point. You don't. You arrive somewhere downstream — the current carried you while you were paddling.

This isn't a failure of paddling; it's a failure of intuition. The canoe's velocity *relative to the water* points west. The water's velocity *relative to the ground* points downstream. The canoe's velocity *relative to the ground* — which is what determines where you end up — is the vector sum of those two. There is no way to point the bow that changes the *sum* unless you also change one of its parts, which means paddling against the current.

The same machinery applies to airplanes in crosswinds, to swimmers in currents, to a satellite released from a moving spacecraft. Whenever an object moves *through a medium* that is itself moving *relative to a third frame*, the object's velocity in the third frame is the vector sum of its velocity in the medium plus the medium's velocity in the frame.

### The mechanism — vector addition of velocities

Velocity is a vector. The same component-addition rules apply. If you're tracking three reference frames — call them ground (G), medium (M), object (O) — the relationship is:

$$\mathbf{v}_{\text{O,G}} = \mathbf{v}_{\text{O,M}} + \mathbf{v}_{\text{M,G}}.$$

Read it: the object's velocity relative to the ground equals its velocity relative to the medium, plus the medium's velocity relative to the ground. The subscripts cancel diagonally, which is a useful mnemonic for setting up the right combination.

In components: write each velocity in $x$-$y$ form on a common set of axes, add component by component, then reconstruct the resultant.

### The trade-off

Vector addition of velocities trades **a single intuitive answer for a discipline of tracking frames.** Most everyday motion problems hide which frame you're standing in. ("How fast is the boat going?" — relative to the water? to the shore? to a fish swimming alongside?) Once you commit to writing every velocity with two subscripts (object-relative-to-frame), the algebra is forced to be honest. The cost is a temporary explosion of subscripts. The benefit is no more frame confusion.

### Worked example — the boat across a river

A boat is pointed perpendicular to the bank of a river. Its speed relative to the water is $0.750 \text{ m/s}$, in the $+y$ direction. The river flows at $1.20 \text{ m/s}$ in the $+x$ direction (downstream). What is the boat's velocity relative to the shore?

**Set up axes.** $x$ along the river (downstream positive), $y$ across the river (the direction the bow points).

**Identify components.**
- Boat relative to water: $v_x = 0$, $v_y = 0.750 \text{ m/s}$.
- Water relative to shore: $v_x = 1.20 \text{ m/s}$, $v_y = 0$.

**Add.**
$$v_{\text{tot},x} = 0 + 1.20 = 1.20 \text{ m/s},$$
$$v_{\text{tot},y} = 0.750 + 0 = 0.750 \text{ m/s}.$$

**Reconstruct.**
$$v_{\text{tot}} = \sqrt{(1.20)^2 + (0.750)^2} = \sqrt{1.44 + 0.5625} = \sqrt{2.00} \approx 1.42 \text{ m/s}.$$

$$\theta = \tan^{-1}(0.750 / 1.20) = \tan^{-1}(0.625) \approx 32.0°.$$

The boat moves at $1.42 \text{ m/s}$ relative to shore, $32°$ from the downstream direction (or, equivalently, $58°$ off the perpendicular line you intended to follow). Aim straight across, drift downstream — that's what the answer means.

**Sanity check.** The river flows faster than the boat can paddle relative to the water ($1.20 > 0.750$). So the boat should end up going more downstream than across. The angle ($32°$ from downstream) confirms this — less than $45°$ means the downstream component dominates.

### Common misconceptions

- *"I just add the speeds."* No. You add the *vectors*. Speeds are magnitudes. Adding a $1.20 \text{ m/s}$ downstream speed to a $0.750 \text{ m/s}$ cross-stream speed does not give $1.95 \text{ m/s}$ in any direction — it gives $1.42 \text{ m/s}$ at an angle, because the velocities are perpendicular.
- *"To go straight across, just paddle harder."* True only up to a point — paddling harder increases your speed relative to the water, which can let you angle the bow upstream and have your across-water velocity component plus the downstream current's $x$-component sum to zero. If your top boat-relative-to-water speed is less than the river's speed, no amount of effort gets you across in a straight line.

↳ **Dig Deeper — Galilean relativity and the limits of velocity addition**

*The velocity-addition rule used in this chapter is exact at everyday speeds and a very good approximation across the entire scale of human engineering. At speeds approaching the speed of light, it stops working — and the correct rule, from special relativity, is one of the foundations of modern physics.*

**Prompt:**
> Explain the classical (Galilean) velocity addition rule used in this chapter, then state the relativistic velocity addition formula from special relativity: $u' = (u + v) / (1 + uv/c^2)$. Compute one specific example: an object moving at $0.5c$ relative to a frame that itself moves at $0.5c$ relative to a third frame. The classical rule says $1.0c$; what does the relativistic rule say, and why is the difference important? End with one sentence on at what speeds the classical rule starts to fail measurably.

**What to do with the output:** Save it. Special relativity (Chapter 28) revisits this question in depth. The velocity-addition rule is one of the cleanest places to feel the difference between classical and relativistic kinematics.

---

## Synthesis — vectors, independence, and the cleanup of motion

Step back. Three concepts: vectors and components; the independence of perpendicular motions; addition of velocities. They are not three different ideas — they are three faces of one idea. Two-dimensional motion is just one-dimensional motion happening in two directions at once, and the only thing that links the two directions is shared time.

This is the **scale shift** I want you to feel. The same machinery describes:

- A coin flicked off a desk (a few cm of fall, a meter of horizontal travel).
- A long jump (about 8 meters of horizontal travel, half a meter of rise and fall).
- An artillery shell (kilometers in each direction).
- An ICBM on a ballistic trajectory (thousands of kilometers, with the curvature of the Earth and variation of $g$ becoming significant).
- A satellite in orbit (the same equations, but with $g$ pointing toward Earth's center and varying with altitude — at this scale, "orbit" is what happens when the projectile keeps missing the ground).

The change as you scale up is not the math; it's which approximations break. At small scales, ignore air. At medium scales, include drag but treat $g$ as constant. At planetary scales, treat $g$ as varying with altitude and direction. At galactic scales, switch to general relativity. The vector decomposition into components stays.

### A worked example using all three concepts — the falcon hunt

A peregrine falcon is in a steady horizontal glide at $15.0 \text{ m/s}$ at an altitude of $80.0 \text{ m}$. Below her, a wind is blowing east at $5.00 \text{ m/s}$ — but the falcon is in still air at altitude, gliding due south. She spots prey on the ground directly below where she will be in a few seconds, and folds into a stoop (a steep dive) by tucking her wings. For the next portion of flight, treat her as a projectile launched horizontally at $15.0 \text{ m/s}$ due south from $80.0 \text{ m}$ altitude (we'll keep ignoring air drag and the wind on her body for the calculation, but flag the gap).

**Concept 1 — vectors.** Set $x$ as east, $y$ as north, $z$ as up. The falcon's initial velocity has $v_x = 0$, $v_y = -15.0 \text{ m/s}$ (southward), $v_z = 0$. Her initial position: $(0, 0, 80.0)$. Vertically, she is in free fall with $a_z = -9.80 \text{ m/s}^2$.

**Concept 2 — independence.** Vertical motion: $z = 80.0 - \tfrac{1}{2}(9.80) t^2$. She hits the ground when $z = 0$:

$$0 = 80.0 - 4.90 t^2 \implies t = \sqrt{80.0 / 4.90} = \sqrt{16.3} \approx 4.04 \text{ s}.$$

Horizontal motion (south): $y = -15.0 \cdot 4.04 \approx -60.6 \text{ m}$. She lands $60.6 \text{ m}$ south of where she started.

**Concept 3 — relative velocity.** Now suppose she actually has to deal with the ground-level east wind. If the wind extends to her flight altitude (it usually doesn't extend uniformly, but assume it does for the exercise), then her velocity relative to the ground is her velocity through the air plus the air's velocity relative to the ground:

$$v_{\text{ground},x} = 0 + 5.00 = 5.00 \text{ m/s east},$$
$$v_{\text{ground},y} = -15.0 + 0 = -15.0 \text{ m/s south}.$$

Now her ground track has an eastward component. After the same $4.04 \text{ s}$ of fall, her displacement is $(20.2, -60.6, -80.0)$ — about $20$ meters east of the no-wind landing point. That's the difference between a successful strike and a missed prey.

**Scale shift.** Same equations, applied to a different problem: an aerial bomb dropped from a plane traveling at $250 \text{ m/s}$ at $10{,}000 \text{ m}$ altitude. The bomb is a projectile launched horizontally; you find time of fall from the vertical equation ($t \approx 45 \text{ s}$); you compute horizontal distance from $x = v_x t \approx 11 \text{ km}$. The numbers are bigger; the recipe is identical. From a falcon's stoop to a bombsight, the kinematic structure does not change.

---

## Exercises

### Warm-up

**3.1** *(LO 1)* A hiker walks $4.0 \text{ km}$ east, then $3.0 \text{ km}$ north. (a) What is her total walked distance? (b) What is her displacement (magnitude and direction from start)?

**3.2** *(LO 1)* A vector has magnitude $25.0 \text{ m}$ and points $40°$ north of east. Compute its $x$ (east) and $y$ (north) components.

**3.3** *(LO 1)* A vector has $A_x = -3.0 \text{ m}$ and $A_y = +4.0 \text{ m}$. What is its magnitude and direction (angle from the $+x$-axis)?

**3.4** *(LO 3)* A ball is thrown horizontally at $8.0 \text{ m/s}$ from a height of $1.5 \text{ m}$. Ignoring air resistance, how long until it hits the ground, and how far does it travel horizontally?

### Application

**3.5** *(LO 2)* A boat heads east at $6.00 \text{ m/s}$ relative to the water. The water flows north at $2.00 \text{ m/s}$. (a) What is the boat's velocity relative to the shore (magnitude and direction)? (b) If the river is $300 \text{ m}$ wide (east–west), how long does it take the boat to cross?

**3.6** *(LO 4)* A projectile is launched at $50.0 \text{ m/s}$ at an angle of $30.0°$ above horizontal on level ground. (a) What are the components of the initial velocity? (b) What is the time of flight? (c) What is the range? (d) What is the maximum height?

**3.7** *(LO 4)* A ball is thrown horizontally from the top of a $60.0 \text{ m}$ building and lands $100 \text{ m}$ from the base. Find: (a) the time in the air, (b) the initial horizontal velocity, (c) the velocity (magnitude and direction) just before impact.

**3.8** *(LO 5)* An airplane is heading due north at $200 \text{ km/h}$ relative to the air. A wind blows from the west at $50 \text{ km/h}$. What is the plane's velocity relative to the ground (magnitude and direction)?

### Synthesis

**3.9** *(LO 1, 2, 4)* A daredevil drives a motorcycle off a $32°$ ramp at $40.0 \text{ m/s}$. The takeoff and landing are at the same height. (a) How far does he travel horizontally? (b) If buses parked end-to-end below are $20.0 \text{ m}$ each, how many can he clear?

**3.10** *(LO 4)* The free-throw line in basketball is $4.57 \text{ m}$ from the basket; the rim is $3.05 \text{ m}$ above the floor. A player releases the ball at $2.44 \text{ m}$ above the floor with an initial speed of $8.15 \text{ m/s}$. At what release angle does the ball pass through the rim?

**3.11** *(LO 3, 4)* Drop one coin off a desk while flicking another horizontally at $2.0 \text{ m/s}$. The desk is $0.80 \text{ m}$ tall. (a) Compute when each coin hits the floor. (b) Compute where each coin lands relative to the edge. (c) Comment on whether the two clinks should be simultaneous.

### Challenge

**3.12** *(LO 4, beyond chapter)* A cannon fires a shell with muzzle velocity $560 \text{ m/s}$ at the maximum-range angle. (a) Compute the range, ignoring air drag and Earth's curvature. (b) Compute the peak altitude. (c) Look up Earth's radius and estimate by how much the curvature of the Earth changes the answer in (a). (d) Comment qualitatively on whether air resistance makes the actual range bigger or smaller than the calculated value.

**3.13** *(LO 2, beyond chapter)* Derive the range equation $R = v_0^2 \sin(2\theta_0) / g$ from the kinematic equations. Show your work step by step: write the vertical equation for landing, solve for $t$, substitute into the horizontal equation. State explicitly the assumption that launch and landing are at the same height.

---

## LLM Exercise — Chapter 3: 2D Motion in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A 2D-motion analysis of one element of your anchor phenomenon — a curving path, an angled trajectory, a relative-velocity calculation — using vector decomposition.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste the 1-sentence description from earlier chapters].

For Chapter 3, I want to apply two-dimensional kinematics — vectors, components, projectile motion, and relative velocity — to one element of my phenomenon that involves motion in more than one direction.

Please:

1. Identify ONE 2D-motion question in my phenomenon. Examples:
   - Bike commute: what's my velocity relative to the road when there's a crosswind, and how does it change my heading?
   - Coffee maker: what is the trajectory of a drip falling from the showerhead onto the grounds, given the showerhead spacing?
   - Basketball shot: what release angle maximizes my chance of making a free throw given my release height and speed?
   - Marathon: how does a 10 km/h crosswind change effective pace if I'm running due north at 4 m/s?
   - Espresso: what arc does a stream of water make exiting the portafilter at a typical extraction velocity?

2. Set up the problem with explicit axes (x and y), state the components of every vector involved, and identify which 1D kinematic equation applies to each axis.

3. Walk through the calculation. Report the answer with proper units, sig figs, and an uncertainty estimate (using percent-addition from Chapter 1).

4. Sanity-check the result using a Fermi estimate.

5. Identify which assumption (no air drag, constant g, level launch/land, etc.) is most likely to bite this calculation, and estimate by what fraction the real answer probably differs.

6. One sentence on how this connects to Chapter 4 (forces) when we meet it.

Save the output as logbook/chapter-03-two-dimensional-kinematics.md.
```

### What this produces

A third Logbook entry: a worked 2D motion problem applied to your anchor phenomenon, with an honest accounting of which idealizations are doing the heavy lifting.

### How to adapt this prompt

- *For phenomena that are mostly 1D* (a vertical pour, a straight-line commute on a windless day): introduce a hypothetical 2D element (what would happen with a crosswind, or with a curved component) so you still exercise the chapter's machinery.
- *For ChatGPT or Gemini:* identical, with the usual interface substitutions.
- *For Claude Code:* if you have GPS data from your bike commute, video frames of a basketball shot, or any time-series, paste it and ask Claude to fit a parabola or compute angles directly.

### Connection to previous chapters

Builds on Chapter 2's 1D kinematics by adding a perpendicular axis. The uncertainty propagation rule from Chapter 1 still applies — and in 2D problems, where you may multiply trig functions by speeds and times, the percent-addition rule has more terms to track.

### Preview of next chapter

Chapter 4 introduces Newton's three laws — finally answering *why* the projectile follows the path it does. The Chapter 4 LLM Exercise will ask you to identify the forces at work in your phenomenon and apply $F = ma$ to compute one of them.

---

## Chapter summary

Two-dimensional kinematics is a story told three times. Vectors give you a way to talk about quantities that have direction in a plane — splitting them into perpendicular components is the bookkeeping move that makes addition and subtraction tractable. The independence of perpendicular motions is the physics fact that splits any 2D motion under gravity into two 1D problems sharing only time. Velocity addition extends the same vector logic to motion relative to a moving medium.

The one idea that matters most: **horizontal and vertical motion under gravity are independent**, sharing only the clock. Once you internalize that, every projectile problem reduces to "find $t$ from the vertical equation; substitute into the horizontal." The Edgerton strobe photograph is the proof; Galileo's reasoning is the explanation; the kinematic equations from Chapter 2 are the tool.

The common mistake to watch for: **adding magnitudes instead of vectors.** A boat going $0.75 \text{ m/s}$ across a river that flows $1.20 \text{ m/s}$ does not move at $1.95 \text{ m/s}$ in any direction. It moves at $\sqrt{0.75^2 + 1.20^2} = 1.42 \text{ m/s}$ at an angle, because the velocities are perpendicular and add as vectors. The Pythagorean theorem and the arctangent are the discipline that prevents this error.

What you should now be able to teach someone else: how to split a vector into components, how to add two vectors by components, how to set up a projectile problem (resolve initial velocity, treat horizontal and vertical separately, find $t$ from one and use it in the other), and how to add two velocities to find motion relative to a third frame. Three skills, one underlying idea.

---

## What would change my mind

The chapter argues that the no-air-resistance treatment of projectile motion is a clean idealization that captures the essential physics for short, dense projectiles. The argument would need revision if introductory mechanics courses found that students using the no-air model systematically misjudged real ball trajectories in ways that hurt their later physics — they don't, with the standard caveats taught and the realistic-correction problems offered in later chapters.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is the universe so kind as to allow motion to decompose along perpendicular axes at all?** Vector decomposition works because space, at least at human scales, behaves as a flat Euclidean plane in which perpendicular directions are genuinely independent. In curved spacetimes (general relativity), this stops being exactly true. We will not encounter curvature until Chapter 33; until then, the flatness of space is a convenience we will not interrogate.

---

## Connections forward

Chapter 4 introduces Newton's laws of motion — finally telling us *why* objects accelerate the way they do. Force is a vector; force decomposition uses exactly the component machinery installed here. Chapter 5 applies this to motion on inclined planes (where the natural axes are not horizontal/vertical but parallel/perpendicular to the slope). Chapter 6 takes the projectile-motion logic and curls it into a circle: uniform circular motion is what happens when a projectile keeps falling toward a center. Chapter 8 (momentum) uses vector addition for collisions in 2D; Chapter 22 (magnetic forces) uses it for charged particles in fields. Vectors are the spine of the rest of the book.

---

**Tags:** vectors, projectile-motion, components, relative-velocity, independence-of-axes

---

## AI Wayback Machine

**Niccolò Tartaglia** worked out projectile motion in the 1530s — the first systematic mathematical treatment of how a cannonball travels through the air. He developed the theory while consulting for Italian artillery commanders and later regretted helping make war more deadly.

**Run this:**

```
Who was Niccolò Tartaglia, and how does his projectile motion work connect to the two-dimensional kinematics we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Niccolò Fontana Tartaglia"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Tartaglia's account of projectile motion — what was right, what was wrong, what Galileo later corrected.
- Ask it about Tartaglia's famous mathematical contest with Cardano over solving cubic equations.

What changes? What gets better? What gets worse?
