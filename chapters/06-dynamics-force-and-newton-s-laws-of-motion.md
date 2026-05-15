# Chapter 6 — Dynamics: Force and Newton's Laws of Motion

**Suggested titles**

1. Dynamics: Force and Newton's Laws of Motion
2. Why Things Move (and Why They Stop)
3. The Three Lines That Replaced Aristotle

**TL;DR.** Kinematics described motion. Dynamics explains it. Newton's three laws — *change requires a net force*, *force equals mass times acceleration*, *every force has an equal and opposite partner* — are three sentences that, taken together, predict the motion of nearly everything in the everyday world. This chapter installs the laws, the bookkeeping (free-body diagrams, weight, normal force, tension), and the four fundamental forces of nature into which every push and pull eventually decomposes.

---

## A bat shattering on a Mariano Rivera cutter, summer 2013

Yankee Stadium, late innings, a one-run game. Mariano Rivera comes in from the bullpen — he is forty-three years old, in his last season, the most prolific closer in the history of the sport. The hitter sets up. Rivera throws his cutter — a fastball that, instead of rotating purely backward, spins slightly off-axis so that, in the last fifteen feet, it darts an inch or two toward the hitter's hands. The hitter swings. There is a *crack* that is not the usual *crack*. The bat splits at the handle, the top half spinning out toward the third-base line. The ball dribbles harmlessly to the pitcher.

A common reading: the bat hit the ball, transferring force into the ball, and the ball flew. A more honest reading: the bat hit the ball *and the ball hit the bat*, with exactly equal force in opposite directions. The bat was not the only thing exerting force during contact. The ball, moving at $40 \text{ m/s}$ into the hitting zone, pushed back on the bat with the same magnitude of force the bat applied to it. With a Rivera cutter, the contact point was usually a few inches from the bat's sweet spot — close enough to the handle that the wood couldn't take the load. The bat broke not because the hitter swung too hard, but because the ball pushed on the bat with the same force the bat pushed on the ball, in the wrong place along the lever.

This is one half of Newton's third law made visible: a force never exists alone. It always has a partner. To exert is also to receive. The bat is not in a privileged position; the ball is not in a privileged position; both are participating in the same interaction, viewed from two ends.

This chapter is about three sentences Isaac Newton wrote down, in Latin, in 1687, in a book called *Philosophiæ Naturalis Principia Mathematica*. The three sentences explain why things move, why they stop, why they don't move when they look like they should, and why a baseball can shatter a piece of seasoned ash. They also explain why a rocket goes up, why a car needs a road, and why, when you lean against a wall, the wall is — quietly, invisibly, exactly — pushing back on you.

**Learning objectives.** By the end of this chapter you should be able to:

1. State Newton's three laws of motion in your own words and identify when each applies.
2. Construct a free-body diagram of an object — identifying all external forces and ignoring internal ones.
3. Apply $F_{\text{net}} = m a$ to solve for an unknown force, mass, or acceleration in 1D and 2D problems.
4. Identify Newton's-third-law force pairs (action and reaction) in everyday situations and explain why they don't cancel each other.
5. Distinguish weight from mass, normal force from tension, and apply each correctly in a problem.
6. Name the four fundamental forces of nature and the rough domain of each.

**Prerequisites.** Chapter 1 (units, sig figs). Chapter 2 (acceleration). Chapter 3 (vectors and components). Trigonometry for resolving forces along chosen axes.

**Why this chapter matters.** Every later mechanics chapter — friction, drag, circular motion, gravity, work, energy, momentum, rotation, fluids, oscillation — applies Newton's laws to a specific case. Most engineering — buildings, vehicles, bridges, prosthetics — is the application of these laws to the static or dynamic equilibrium of structures. Get these three sentences wrong and the next twenty chapters become opaque. Get them right and most of mechanics is bookkeeping.

---

## Concept 1 — The first law: change requires a cause

### A puck on an air-hockey table, and the ghost of Aristotle

Aristotle, around 350 BC, had a theory of motion that everyone believed for the next two thousand years. The theory said: the natural state of a body is rest. Things at rest stay at rest. Things in motion slow down and stop because that is what they want to do. To keep something moving, you have to keep pushing.

The theory matches everyday experience. Push a book across a table; it slows and stops. Roll a ball across the carpet; it slows and stops. Throw a stick into a still pond; it floats to a stop. Aristotle's claim — *motion requires a sustained cause* — is what your kitchen and your living room teach you.

It is also wrong.

Galileo, around 1600, started undoing it with one observation. Push the book on a smooth wooden table; it slows quickly. Push it on glass; it slows less. Push it on a wet ice surface; it slows hardly at all. The slowing is not what the *book* wants to do. The slowing is what the *friction* does to the book. As the surface gets smoother, the slowing diminishes. *Extrapolate to perfect smoothness, and the slowing vanishes.* The book would slide forever.

Switch on the air-hockey table at any rec hall. The puck moves smoothly across the surface, riding on a thin film of air, and it does not appreciably slow. Switch the air off and the puck stops within an inch. The variable is not what the puck is doing — it's what the table is doing to the puck.

Newton wrote this insight down as a law. *A body at rest remains at rest, or, if in motion, remains in motion at constant velocity, unless acted on by a net external force.* The natural state of a body, in the absence of forces, is *constant velocity* — which includes zero velocity as a special case. Slowing down is not a default; slowing down requires a force, just as speeding up does.

### The mechanism — inertia, mass, and the meaning of "net external"

The first law introduces a property of matter that has not appeared in this book before: **inertia**. Inertia is the tendency of an object to resist changes in its motion. A heavy object is harder to start moving and harder to stop than a light one — that's its larger inertia. The quantitative measure of inertia is **mass**, in kilograms. (Mass and weight are different things; we'll separate them carefully in Concept 2.)

Two phrases in the law need unpacking. *Net external force* is one. *External* means "applied from outside the system you're analyzing." If you punch yourself in the arm, your fist exerts a force on your arm and your arm exerts a force on your fist (third law!), but neither is an external force on the system *you* — they're both internal. The whole-body system *you* doesn't accelerate from a self-punch. *Net* means "the vector sum of all external forces." If two equal forces push on opposite sides of an object, the net force is zero and the object's velocity doesn't change — even though there are forces acting.

This is what saves Newton's first law from looking trivially false in everyday life. The book on the table looks like Aristotle's example: pushed, it stops. But there are *two* forces on the moving book — your push (forward) and friction (backward). When you stop pushing, your push goes to zero but friction does not. The net external force is now backward; the book decelerates; the book stops. The first law was right all along; we were miscounting forces.

### The trade-off

The first law trades **everyday intuition for a cleaner conceptual structure.** It contradicts what your living-room experiments seem to teach. You have to be willing to imagine a frictionless world to feel the law. The reward is a single principle that scales from a hockey puck on ice to a satellite in orbit (still moving after the engines cut out, because no net force is changing its velocity).

### Worked example — does a constant-velocity car have a net force?

A car is cruising down a flat highway at a steady $30 \text{ m/s}$. The engine is running, the gas is engaged. Question: is the net external force on the car zero or nonzero?

**Reasoning.** Constant velocity means zero acceleration. By the first law (and we'll see in Concept 2 that this is exactly $F_{\text{net}} = m a = 0$), the net external force is zero. *Even though the engine is producing forward thrust and the road is providing forward traction.*

The forces on the car are not zero. The engine-and-tires push the car forward. Air drag and rolling friction push it backward. At $30 \text{ m/s}$, those happen to be equal in magnitude. The net is zero. The car cruises.

If you took your foot off the gas, the forward push would drop, and the net force would become backward, and the car would decelerate. If you pressed harder, the forward push would exceed drag, and the car would accelerate.

**Sanity check.** This is consistent with what you actually feel. To maintain highway speed, you keep your foot on the gas — you don't press harder. The pressure required is what overcomes drag, not what produces speed.

**The general lesson.** Steady motion does not mean *no forces.* It means *no net force.* The two are different claims, and conflating them is the most common Aristotelian residue in beginner physics intuition.

### Common misconceptions

- *"A moving object has a force on it because it's moving."* No. A moving object can have zero net force (cruising car, sliding hockey puck on ice, satellite in orbit). Motion does not require force. *Change* in motion requires force.
- *"If there's no force, the object stops."* No. If there's no force, the object continues at whatever velocity it had — including a nonzero one. This is exactly Newton's first law.

↳ **Dig Deeper — Inertial frames and why the first law isn't trivially true**

*Newton's first law refers to "a body acted on by no net external force." But to say whether a body is moving at constant velocity, you have to specify a frame of reference. In an accelerating frame (a braking car, a spinning carousel), a body with no force on it appears to accelerate. The first law silently assumes you're observing from an *inertial* frame — and that assumption hides one of the deepest puzzles in classical mechanics.*

**Prompt:**
> Explain what an inertial frame is, why Newton's first law only holds in inertial frames, and how you would in principle test whether a frame is inertial. Walk through one example: an observer inside a car that brakes hard, watching a coffee cup slide forward — describe what's happening from inside the car (where the cup appears to accelerate forward without a force) versus from outside (where the cup is doing exactly what Newton's first law predicts). End with one sentence on why general relativity ultimately reframes "inertial frame" in terms of free-fall trajectories.

**What to do with the output:** Save it. The inertial-frame question returns in Chapter 6 (centripetal "force") and is foundational to Chapter 28 (special relativity).

---

## Concept 2 — The second law: $F = ma$ and what each symbol means

### A child pulling a wagon, two children pushing back

Imagine a child sitting in a wagon. Two friends push the wagon — one from behind, one from the side — at different angles. The wagon accelerates in some direction, at some rate. Newton's second law tells you how to predict that direction and that rate from the forces and the mass.

It is the equation every introductory physics student learns:

$$\mathbf{F}_{\text{net}} = m \mathbf{a}.$$

Three symbols. Each one is a vector or a scalar with a precise meaning. Half the work of using the equation is being careful about which symbol means what.

### The mechanism — the second law, term by term

**$\mathbf{F}_{\text{net}}$** is the *net external force on the system*. Sum, vectorially, every push and pull from outside the system. If three forces act, $\mathbf{F}_{\text{net}} = \mathbf{F}_1 + \mathbf{F}_2 + \mathbf{F}_3$. Internal forces — forces between parts of the system on each other — do not contribute, because they cancel in pairs (Newton's third law, foreshadowed).

**$m$** is the *inertial mass* of the system, in kilograms. It is a scalar, always positive. For a system made of multiple objects rigidly connected, $m$ is the sum of the masses.

**$\mathbf{a}$** is the *acceleration of the system's center of mass*. It is a vector — same direction as the net force, magnitude equal to $|\mathbf{F}_{\text{net}}| / m$.

The equation says: the net external force on a system *causes* an acceleration of the system's center of mass, in the direction of that net force, with a magnitude inversely proportional to the system's mass. Push hard on a heavy thing: small acceleration. Push hard on a light thing: large acceleration. Push gently on anything: small acceleration. The proportionality is exact.

In components, the second law splits into independent equations along each axis:

$$F_{\text{net},x} = m a_x, \qquad F_{\text{net},y} = m a_y, \qquad F_{\text{net},z} = m a_z.$$

This is what makes the chapter-3 vector machinery so important: every force problem in two or three dimensions is solved by resolving forces into components, then applying the second law along each axis separately.

### Weight and the difference between mass and weight

Consider an object near the surface of the Earth. The Earth pulls it downward with a gravitational force. Call that force $\mathbf{W}$, the **weight**:

$$\mathbf{W} = m \mathbf{g},$$

where $\mathbf{g}$ is the local gravitational acceleration (about $9.80 \text{ m/s}^2$ downward on Earth's surface). Weight is a *force*, measured in newtons. Mass is a *property*, measured in kilograms.

A $1 \text{ kg}$ object on Earth weighs $9.80 \text{ N}$. The same $1 \text{ kg}$ object on the Moon weighs $1.62 \text{ N}$ (the Moon's $g$ is about one-sixth of Earth's). The mass is the same in both places. The weight is not. Mass is what the object *is*; weight is what gravity *does* to it in a particular location.

Confusing the two is one of the most common errors in introductory physics. When a problem says "an object of weight $50 \text{ N}$," the mass is $50 / 9.80 \approx 5.10 \text{ kg}$, not $50 \text{ kg}$. When a problem says "a $5 \text{ kg}$ object," its weight is $5 \times 9.80 = 49 \text{ N}$, not $5 \text{ N}$. The factor of $g$ is constantly going one way or the other.

### Free-body diagrams — the bookkeeping that makes everything tractable

Before doing any second-law calculation, draw a **free-body diagram**. Reduce the object of interest to a point or simple shape. Draw an arrow for *every external force* acting on it — and *only* external forces. Label each arrow with what it represents (weight, normal force, friction, tension, your push, etc.).

Then choose axes. Then sum forces along each axis. Then apply $F_{\text{net},x} = m a_x$ and $F_{\text{net},y} = m a_y$.

This is the algorithm for every Newton's-laws problem. The hard part is identifying all the external forces and resisting the urge to draw imaginary ones (centrifugal force, "force of motion") or omit real ones (the normal force from the floor).

### The trade-off

The second law trades **conceptual purity for arithmetic generality.** The equation $F_{\text{net}} = ma$ doesn't tell you what *causes* gravity, what *causes* electromagnetism, or where forces come from in any deep sense. It tells you only what forces *do* once they exist. The cost is a missing piece (you have to look up the force law for each interaction). The benefit is a single equation that processes any force into a prediction of motion, regardless of the force's origin.

### Worked example — pushing a stalled car

You're pushing a stalled $1{,}500 \text{ kg}$ car along a level road. You apply a horizontal force of $400 \text{ N}$. The car experiences rolling friction of $200 \text{ N}$ opposing the motion. What is the car's acceleration?

**Free-body diagram.** Forces on the car: your push ($+400 \text{ N}$ in the direction of motion); friction ($-200 \text{ N}$ opposing motion); weight ($mg = 1{,}500 \times 9.80 = 14{,}700 \text{ N}$ downward); normal force from the road ($+14{,}700 \text{ N}$ upward).

**Choose axes.** $x$ along the direction of motion, $y$ vertical.

**Vertical:** $F_{\text{net},y} = N - W = 14{,}700 - 14{,}700 = 0$. The car is not accelerating vertically. Good. (If the answer here had been nonzero, the car would be falling through the road or jumping off it — a sanity-check failure.)

**Horizontal:** $F_{\text{net},x} = 400 - 200 = 200 \text{ N}$. So:

$$a_x = \frac{F_{\text{net},x}}{m} = \frac{200 \text{ N}}{1{,}500 \text{ kg}} \approx 0.13 \text{ m/s}^2.$$

The car accelerates at about $0.13 \text{ m/s}^2$ in the direction you're pushing.

**Sanity check.** Pushing a real car requires real effort and produces a slow acceleration — your $400 \text{ N}$ is about 90 pounds of force, a hard but plausible push. Getting an acceleration of $0.13 \text{ m/s}^2$ means the car gains about $1.3 \text{ m/s}$ (3 mph) over ten seconds. That feels right for shoving a stalled car. The numbers check.

**The general lesson.** Always draw the free-body diagram. Always check both axes — even when one is "obviously" balanced. The vertical-axis check confirmed the normal force (which we'll need for friction in Chapter 5). Half the value of free-body diagrams is in the forces you check off as balanced; you only get to ignore them once you've confirmed they are.

### Common misconceptions

- *"Mass and weight are the same thing."* Mass is a scalar in kilograms; weight is a force in newtons. The relationship $W = mg$ converts one to the other, but they are different quantities.
- *"A bigger force always means a bigger velocity."* No. A bigger force means a bigger *acceleration* (rate of change of velocity). An object can have a very small velocity at the moment a very large force is applied (think of a rocket lifting off — for the first millisecond, velocity is nearly zero, but acceleration is enormous).
- *"$F = ma$ describes how the force depends on the motion."* It doesn't. It describes how the motion depends on the force. The force comes from somewhere else (gravity, contact, electromagnetism); $F = ma$ then tells you the resulting acceleration.

↳ **Dig Deeper — Why $F = ma$ specifically? The momentum form of the second law**

*Newton actually wrote his second law in terms of momentum: $\mathbf{F} = d\mathbf{p}/dt$, where $\mathbf{p} = m\mathbf{v}$ is the momentum. For constant mass, this reduces to $\mathbf{F} = m\mathbf{a}$. The momentum form is more general — it handles cases like a rocket that loses mass as it burns fuel, where the constant-mass version fails.*

**Prompt:**
> Walk me through the momentum form of Newton's second law: $\mathbf{F} = d\mathbf{p}/dt$. Show that for constant mass, this reduces to $\mathbf{F} = m\mathbf{a}$. Then work through one example where mass is not constant — a rocket burning fuel — and show how the momentum form gives the right answer (the rocket equation, $\Delta v = v_e \ln(m_0/m_f)$) while the constant-mass second law fails. End with one sentence on what other physical scenarios involve changing mass.

**What to do with the output:** Save it. The momentum form is the foundation of Chapter 8 (linear momentum and collisions) and the conceptual basis of how rockets work.

---

## Concept 3 — The third law: forces come in pairs

### A swimmer pushing off the wall

A competitive swimmer at the start of a race waits at the wall. The starting buzzer sounds. She pushes hard against the wall with her feet — and shoots forward into the pool. The wall did not move; her body did. From her perspective, she pushed off the wall and accelerated forward. But what was the *force on her* that accelerated her body?

Her muscles pushed against the wall. The wall, in response, pushed her body forward with exactly the same magnitude of force, in exactly the opposite direction. The force *on her* (which is what determines her acceleration by the second law) came from the wall pushing on her. Without the wall pushing back, she would have nothing to accelerate against.

This is Newton's third law in action. The swimmer pushes the wall; the wall pushes the swimmer. Forces always come in pairs — and the two forces in a pair act on *different objects*. They never cancel, because they're not on the same object.

### The mechanism — action-reaction pairs

Newton's third law: *Whenever one body exerts a force on a second body, the first body experiences a force that is equal in magnitude and opposite in direction to the force it exerts.*

Symbolically: if object A exerts force $\mathbf{F}_{A \to B}$ on object B, then object B exerts force $\mathbf{F}_{B \to A}$ on object A, with

$$\mathbf{F}_{B \to A} = -\mathbf{F}_{A \to B}.$$

The two forces are equal in magnitude, opposite in direction, and act on *different objects*. That last part is critical.

A common confusion: "If every action has an equal and opposite reaction, how does anything ever accelerate? Don't the forces cancel?"

They don't, because they're on different objects. When the swimmer's feet push the wall with $500 \text{ N}$ forward (into the wall), the wall pushes her with $500 \text{ N}$ backward (out of the wall). The $500 \text{ N}$ on the wall is what would accelerate the wall — except the wall is bolted to the pool, which is bolted to the Earth, so the effective mass it would have to accelerate is gigantic and the resulting acceleration is negligible. The $500 \text{ N}$ on the swimmer is what accelerates her — and her mass is small, so her acceleration is large. Same force pair, vastly different consequences, because the two forces are on objects with vastly different effective masses.

### Identifying action-reaction pairs

The trick to spotting third-law pairs: replace "X exerts force on Y" with "Y exerts force on X." If both sentences are true and the forces are equal-magnitude opposite-direction, you have a pair.

- The Earth pulls down on you (gravity, $\sim 700 \text{ N}$ for a $70 \text{ kg}$ person). You pull up on the Earth (gravity, also $700 \text{ N}$). Pair. The Earth doesn't visibly accelerate because its mass is $\sim 6 \times 10^{24}$ kg.
- The road pushes up on the car's tires (normal force). The tires push down on the road (normal force, equal and opposite). Pair.
- A book sits on a table. The table pushes up on the book (normal force, $50 \text{ N}$ if the book weighs $50 \text{ N}$). The book pushes down on the table (normal force, $50 \text{ N}$). Pair.

A non-pair, for contrast: gravity (Earth on book) and normal force (table on book) are *not* a third-law pair, even though they cancel in the book's free-body diagram. They're both forces on the book; a third-law pair would have one force on the book and another on something else. The third-law partner of "gravity Earth-on-book" is "gravity book-on-Earth." The third-law partner of "normal table-on-book" is "normal book-on-table." Both pairs exist; neither pair has the two forces on the same object.

### The trade-off

The third law trades **single-object focus for relational thinking.** A naive view of mechanics treats one object at a time. Newton's third law forces you to remember that every interaction is mutual; whenever you write down a force, the partner force exists and acts on something else. This is what makes systems analysis tractable: choose your "system" carefully, and the internal force pairs cancel automatically, leaving only external forces on the system as a whole.

### Worked example — the bat and the ball revisited

A baseball bat strikes a ball. During the brief contact, the bat exerts an average force of $5{,}000 \text{ N}$ on the ball (forward). The ball has mass $0.145 \text{ kg}$; the bat has mass $0.95 \text{ kg}$.

**(a) What force does the ball exert on the bat?**

By the third law, $5{,}000 \text{ N}$ in the opposite direction (backward, into the bat).

**(b) What is the ball's acceleration during contact?**

$$a_{\text{ball}} = \frac{F}{m_{\text{ball}}} = \frac{5{,}000}{0.145} \approx 34{,}500 \text{ m/s}^2.$$

That's about $3{,}500$ g's. Brief and ferocious.

**(c) What is the bat's acceleration during contact (assuming the hitter's hands aren't holding it)?**

If the bat were free, the same magnitude of force ($5{,}000 \text{ N}$) acting on its smaller-relative-to-the-ball mass would give:

$$a_{\text{bat,free}} = \frac{F}{m_{\text{bat}}} = \frac{5{,}000}{0.95} \approx 5{,}300 \text{ m/s}^2.$$

About $540$ g's.

**(d) Why doesn't the bat fly backward in real games?**

The hitter's hands. The hitter, gripping the bat, exerts an additional forward force on the bat that prevents most of the recoil. The hitter's body — and ultimately the ground under his feet — absorbs the reaction. (This is also why hits sting the hands. The momentary force on the bat from the ball is not zero, and the hitter feels it at the grip.)

The bat shattering in our opening anecdote is the bat failing to transmit the ball's reaction force from contact point to grip without exceeding the wood's structural limits. Off the sweet spot, the lever-arm geometry concentrates stress at the handle. The wood breaks before the force makes it to the hands.

**Sanity check.** $5{,}000 \text{ N}$ for ball-on-bat is in the right range — published measurements of MLB-level bat-ball collisions place peak forces in the $5{,}000$–$15{,}000 \text{ N}$ range, with contact times around a millisecond. The ball changes velocity from about $-40 \text{ m/s}$ to about $+40 \text{ m/s}$ (a $\Delta v$ of $80 \text{ m/s}$) in roughly $10^{-3}$ s, giving $a \approx 80{,}000 \text{ m/s}^2$ if it were uniform — our number is in the right ballpark, lower because $5{,}000 \text{ N}$ was the *average*, not the peak.

### Common misconceptions

- *"Action and reaction cancel, so nothing should accelerate."* They act on different objects. They don't cancel in any single free-body diagram.
- *"The bigger object exerts a bigger force in a collision."* No. The forces are exactly equal. What differs is the resulting acceleration: bigger mass, smaller acceleration. A truck and a car colliding feel the same magnitude of force on each, but the car's much smaller mass means its acceleration is much larger — which is why occupants of small cars suffer more in collisions with trucks.
- *"The Earth doesn't pull on me as hard as I pull on the Earth, because I'm so much smaller."* The forces are exactly equal. Both you and the Earth exert about $700 \text{ N}$ on each other (for a $70 \text{ kg}$ person). The Earth's resulting acceleration is so small ($a \approx 700 / 6 \times 10^{24} \approx 10^{-22} \text{ m/s}^2$) that it's unmeasurable, but it's not zero.

↳ **Dig Deeper — The four fundamental forces**

*Every push, pull, contact force, friction, normal force, tension, and electrostatic attraction in this book ultimately reduces to combinations of just four fundamental interactions: gravity, electromagnetism, the strong nuclear force, and the weak nuclear force. Knowing which fundamental force underlies a given everyday force changes how you think about it.*

**Prompt:**
> Briefly explain the four fundamental forces of nature (gravitational, electromagnetic, weak nuclear, strong nuclear). For each, name (a) the relative strength compared to the others, (b) the range over which it acts, and (c) one example of an everyday phenomenon it produces or governs. Then explain why nearly every contact force you experience in daily life — friction, normal force, tension, the rigidity of a chair — is fundamentally electromagnetic in origin, despite not feeling like an "electric" force.

**What to do with the output:** Save it. The four-forces framework returns in Chapter 22 (electromagnetism), Chapter 31 (nuclear physics), and as the conceptual horizon for any later study of particle physics or cosmology.

---

## Synthesis — three laws, one machinery for everything mechanical

Step back. Three laws.

**First:** an object's velocity does not change unless a net external force acts on it. Constant velocity is the natural state, including zero velocity as a special case.

**Second:** the net external force on a system equals the system's mass times the acceleration of its center of mass. $\mathbf{F}_{\text{net}} = m\mathbf{a}$. This is the predictive equation; once you know the forces, you know the motion.

**Third:** every force is half of a pair. If A pushes B with force $\mathbf{F}$, then B pushes A with force $-\mathbf{F}$. The two forces act on different objects.

Together, these three sentences explain pulleys and rockets, falling apples and orbiting moons, the gait of a horse and the design of a suspension bridge. They do not explain *why* gravity exists or *why* the Earth's surface is rigid — those questions point to gravity (Chapter 6), atomic structure (Chapter 30), and ultimately the four fundamental forces. But within those forces, the laws describe what happens completely.

The **scale shift** I want you to feel here: the same three laws govern a baseball bat shattering at $5{,}000 \text{ N}$ over a millisecond, a person walking across a room at a few newtons of net force over seconds, a car cruising the highway with zero net force over hours, and a planet orbiting the Sun under a $3.5 \times 10^{22} \text{ N}$ gravitational pull continuously for billions of years. The law $\mathbf{F} = m\mathbf{a}$ scales without modification across more than 30 orders of magnitude in mass and at least as many in time. That kind of universality is what justifies treating Newton's laws as foundational.

### A worked example using all three concepts — a tugboat-towed barge

Two tugboats push a $5.0 \times 10^6 \text{ kg}$ barge. Tugboat 1 pushes with $2.7 \times 10^5 \text{ N}$ in the $+x$ direction. Tugboat 2 pushes with $3.6 \times 10^5 \text{ N}$ in the $+y$ direction. The barge is observed to accelerate at $7.5 \times 10^{-2} \text{ m/s}^2$ in the direction of the combined applied force. Water drag opposes this motion. Find the magnitude of the drag force.

**Concept 1 (first law).** Constant acceleration means nonzero net force; the drag must be less than the applied force, leaving a residual that produces the acceleration.

**Concept 2 (second law).** Combine the two tugboat forces vectorially:

$$F_{\text{app}} = \sqrt{(2.7 \times 10^5)^2 + (3.6 \times 10^5)^2} = \sqrt{7.29 \times 10^{10} + 1.30 \times 10^{11}} \approx 4.5 \times 10^5 \text{ N}.$$

The applied force vector points at angle $\theta = \tan^{-1}(3.6/2.7) \approx 53°$ above the $+x$-axis.

The required net force to produce the observed acceleration:

$$F_{\text{net}} = m a = (5.0 \times 10^6)(7.5 \times 10^{-2}) = 3.75 \times 10^5 \text{ N}.$$

So drag (along the same line as the applied force, but opposite) is:

$$F_{\text{drag}} = F_{\text{app}} - F_{\text{net}} = 4.5 \times 10^5 - 3.75 \times 10^5 = 7.5 \times 10^4 \text{ N}.$$

**Concept 3 (third law).** The barge pushes back on each tugboat with forces equal and opposite to what each tugboat applies. The barge also pushes water backward (action), and water pushes the barge backward via drag (reaction). Drag is one half of the third-law pair "barge pushes water" — barge displaces water, water resists.

**Sanity check.** Drag is about $17\%$ of the applied force. For a flat-bottomed barge moving slowly through water, that's plausible — slow motion through a fluid is dominated by viscous drag, and the quoted acceleration is indeed slow ($7.5 \text{ cm/s}^2$ — over a minute, that's a velocity change of about $4.5 \text{ m/s}$, or about $9$ knots in a minute, which is fast for a barge but not absurd as a peak).

The example exercises all three laws: the first frames the question (a net force is required because acceleration is nonzero); the second computes the magnitude; the third interprets the drag as the water's reaction to being pushed.

---

## Exercises

### Warm-up

**4.1** *(LO 1)* A puck slides across a perfectly frictionless ice rink at constant velocity. (a) What is the net force on it? (b) Are there any forces on it at all? List them.

**4.2** *(LO 3)* A $2.0 \text{ kg}$ object experiences a net force of $10 \text{ N}$. What is its acceleration?

**4.3** *(LO 5)* What is the weight (in newtons) of a $65 \text{ kg}$ student on Earth? On the Moon ($g_{\text{Moon}} = 1.62 \text{ m/s}^2$)? What is her mass in each location?

**4.4** *(LO 4)* Identify the third-law partner of each force: (a) Earth's gravity pulling down on you. (b) Your hand pushing on a door. (c) A horse pulling a cart forward.

### Application

**4.5** *(LO 2, 3)* A $1{,}200 \text{ kg}$ car accelerates from rest to $25 \text{ m/s}$ in $8.0 \text{ s}$. (a) What is its acceleration? (b) What is the net force on it during the acceleration? (c) If air drag and rolling friction sum to $400 \text{ N}$, what forward force must the engine-and-tires produce?

**4.6** *(LO 2, 3)* A $50 \text{ kg}$ skydiver falls at terminal velocity. (a) What is her acceleration? (b) What is the net force on her? (c) What is the magnitude of the air drag opposing her fall?

**4.7** *(LO 5)* A $20 \text{ kg}$ box hangs from two ropes attached to the ceiling, each rope making a $30°$ angle with the vertical. Find the tension in each rope. (Assume symmetric loading.)

**4.8** *(LO 2, 3)* A horizontal force of $30 \text{ N}$ is applied to a $5.0 \text{ kg}$ block on a frictionless horizontal surface. (a) What is the block's acceleration? (b) What normal force does the surface exert on the block?

### Synthesis

**4.9** *(LO 2, 3, 4)* Two ice skaters of masses $50 \text{ kg}$ and $80 \text{ kg}$ push off from each other on a frictionless rink. The push lasts $0.50 \text{ s}$, during which the lighter skater experiences a force of $200 \text{ N}$. (a) What force does the heavier skater experience during the push? (b) What are their respective accelerations? (c) After the push, what are their respective velocities?

**4.10** *(LO 3, 5)* A $100 \text{ kg}$ crate sits on a $30°$ ramp. There is no friction. (a) What is the component of gravity along the ramp (down the slope)? (b) What is the normal force from the ramp on the crate? (c) What is the crate's acceleration down the ramp?

**4.11** *(LO 2, 4)* A $1{,}500 \text{ kg}$ truck tows a $500 \text{ kg}$ trailer along a level road. The system accelerates at $1.0 \text{ m/s}^2$. (a) What is the net force on the system? (b) If rolling friction on the trailer is $50 \text{ N}$, what is the tension in the tow hitch? (c) Identify three Newton's-third-law force pairs in this scenario.

### Challenge

**4.12** *(beyond chapter)* A $0.145 \text{ kg}$ baseball is in contact with a bat for $1.5 \text{ ms}$. The ball changes velocity from $-40 \text{ m/s}$ (incoming) to $+45 \text{ m/s}$ (outgoing). (a) Compute the ball's average acceleration during contact. (b) Compute the average force on the ball. (c) Compute the average force on the bat. (d) Estimate the peak force, given that real force-vs-time curves typically peak at about twice the average.

**4.13** *(beyond chapter)* A rocket of initial mass $1{,}000 \text{ kg}$ (including $800 \text{ kg}$ of fuel) burns fuel at $4 \text{ kg/s}$, expelling exhaust at $2{,}500 \text{ m/s}$ relative to the rocket. (a) What is the thrust force? (b) What is the rocket's initial acceleration (immediately after launch)? (c) What is its acceleration just before all fuel is used? (d) Why does the second answer matter for designing real rockets?

---

## LLM Exercise — Chapter 4: Forces in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A free-body diagram of a key element of your anchor phenomenon, with all forces identified, $F = ma$ applied, and at least one Newton's-third-law pair named explicitly.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 4, I want to apply Newton's three laws to my phenomenon. Please:

1. Pick ONE moment in my phenomenon where forces are interesting. Examples:
   - Bike commute: the moment of pushing off from a stop sign — what forces accelerate me?
   - Coffee maker: the moment when water column weight pushes down through the basket and grounds resist — what's the force balance during brewing?
   - Basketball shot: the moment of release — what forces does the player exert and feel?
   - Marathon: a steady-state stride at race pace — what forces are balanced, and what produces forward motion?
   - Espresso: the puck during extraction at 9 bar — what forces act on the coffee, and what balances them?

2. Draw (in ASCII or describe in text) the free-body diagram for the chosen object. List every external force with magnitude (estimated or computed) and direction.

3. Apply F = ma along each axis. Solve for any unknown (the acceleration, an unknown force, or a needed coefficient).

4. Identify at least one Newton's-third-law action-reaction pair in the scene. Name both forces, both objects, and explain why the pair doesn't "cancel."

5. Sanity check the result with one Fermi-style estimate.

6. Identify which fundamental force (gravity, electromagnetic, etc.) ultimately underlies each contact force you listed.

7. One sentence on how friction (Chapter 5) will modify this analysis.

Save the output as logbook/chapter-04-newtons-laws.md.
```

### What this produces

A fourth Logbook entry: a force analysis of your phenomenon with the action-reaction structure made explicit. By Chapter 4 you have foundation + 1D kinematics + 2D kinematics + force analysis — most of "Newtonian mechanics" in skeleton form for your phenomenon.

### How to adapt this prompt

- *For phenomena where motion is mostly steady-state* (a coffee maker reaching equilibrium, a marathon at constant pace): emphasize the balanced-force analysis (first law) rather than the accelerating analysis. Both are exercises of Newton's laws.
- *For ChatGPT or Gemini:* identical with interface substitutions.
- *For Claude Code:* if you have force data (e.g., a pressure curve from an espresso machine, a wattmeter reading from a stationary bike), paste it and ask for a force-vs-time fit.

### Connection to previous chapters

Builds directly on Chapter 3's vector decomposition (forces are vectors; we resolve them along axes the same way we resolved velocities). The kinematics from Chapter 2 returns: once you have $a$ from Newton's second law, you can predict velocity and position from the kinematic equations.

### Preview of next chapter

Chapter 5 specializes Newton's laws to friction, drag, and elasticity — three force laws that fill in the "where do contact forces come from?" gap. The Chapter 5 LLM Exercise will ask you to compute friction or drag explicitly for your phenomenon.

---

## Chapter summary

Newton's three laws of motion are the foundation of mechanics. **First law:** an object's velocity changes only when a net external force acts. **Second law:** the net external force equals mass times the acceleration of the center of mass, $\mathbf{F}_{\text{net}} = m\mathbf{a}$. **Third law:** every force has an equal-magnitude, opposite-direction partner force on a different object.

The one idea that matters most: **forces cause changes in motion, not motion itself.** This single insight inverts two thousand years of Aristotelian physics. Once internalized, it organizes every later mechanics problem: identify the object, identify the external forces, sum them as vectors, divide by mass to get acceleration, integrate to get velocity and position.

The common mistake to watch for: **ignoring forces that are obviously there.** Beginning physicists often forget the normal force from the floor, the tension in the rope, the weight of an object, or — most insidiously — the third-law partner force on the object outside their system. Free-body diagrams are the discipline that prevents this. Draw them. Always.

What you should now be able to teach someone else: how to draw a free-body diagram (every external force, no internal ones, vectors with proper directions); how to apply $F = ma$ along chosen axes; how to identify a Newton's-third-law pair (replace "X exerts force on Y" with "Y exerts force on X" and the magnitudes match); and how mass differs from weight ($m$ in kilograms, $W = mg$ in newtons). Four skills, one underlying framework.

---

## What would change my mind

The chapter argues that Newton's three laws, with the corrections supplied by relativity and quantum mechanics for extreme conditions, are sufficient to describe the mechanical behavior of nearly every system humans engineer or encounter. The argument would need revision if everyday-scale macroscopic phenomena turned out to require corrections beyond the relativistic and quantum regimes already known — which would mean a new branch of physics has been discovered. None has been, despite vigorous searching for over a century.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is inertial mass equal to gravitational mass?** Newton's second law uses *inertial mass* (the $m$ in $F = ma$) — what an object resists acceleration with. Newton's law of gravity uses *gravitational mass* (the source of gravitational pull). These are conceptually distinct quantities. Experimentally, to a precision now better than one part in $10^{13}$, they are equal. Why? Newton's framework offers no answer; it is a coincidence in his system. Einstein's general relativity rewrites the question: in general relativity, gravity is not a force at all but the curvature of spacetime, and the equivalence of inertial and gravitational mass becomes structural, not coincidental. We will not see this until Chapter 33. Until then, the equality is a free gift from nature.

---

## Connections forward

Chapter 5 specializes Newton's second law to specific contact forces: friction, drag, the elastic restoring force of springs and other deformable bodies. Chapter 6 applies $\mathbf{F} = m\mathbf{a}$ to circular motion (centripetal acceleration) and gravitation (the inverse-square law). Chapter 7 reformulates dynamics in terms of *energy* — a different, often more powerful, accounting of the same physics. Chapter 8 reformulates it again in terms of *momentum* — the form of Newton's second law that handles collisions and rocket-like systems. Chapter 9 specializes to statics (when $\mathbf{F}_{\text{net}} = 0$ everywhere). Chapter 10 generalizes everything in this chapter to rotation (force becomes torque, mass becomes moment of inertia, $\mathbf{F} = m\mathbf{a}$ becomes $\boldsymbol{\tau} = I\boldsymbol{\alpha}$). The three laws you just met are the trunk; everything else in mechanics is a branch.

---

**Tags:** Newtons-laws, force, free-body-diagram, third-law, inertia

---

## AI Wayback Machine

**Émilie du Châtelet** translated Newton's *Principia* into French and added a commentary that introduced the concept of kinetic energy as mv² — refining Newton's framework for working physicists. Her version was the standard text on Newtonian mechanics in France for a century.

**Run this:**

```
Who was Émilie du Châtelet, and how does her translation of Newton connect to the dynamics we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about her career or ideas.
```

→ Search **"Émilie du Châtelet"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through du Châtelet's mv² argument and contrast it with Newton's momentum-based framing.
- Ask it about her partnership with Voltaire — and her death in childbirth at 42.

What changes? What gets better? What gets worse?
