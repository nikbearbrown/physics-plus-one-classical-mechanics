# Chapter 7 — Further Applications of Newton's Laws: Friction, Drag, and Elasticity

**Suggested titles**

1. Friction, Drag, and Elasticity: The Forces That Resist
2. Why a Crate Suddenly Slides, Why a Skydiver Stops Accelerating, Why a Bridge Doesn't
3. Three Force Laws That Build the Real World

**TL;DR.** Chapter 4 said *force causes acceleration*. This chapter fills in the question Chapter 4 left hanging: *where do contact forces come from, and how big are they?* Three answers: friction (proportional to normal force, with a coefficient), drag (proportional to speed squared at human scales), and elasticity (proportional to deformation, Hooke's law). Each is an empirical law — fitted to measurement, not derived from first principles — and each has a domain where it holds and a domain where it breaks down. Together, they describe nearly every contact interaction that engineers care about.

---

## A skier in the Karakoram, January 2018

Andrzej Bargiel, 30 years old, Polish, stands at $8{,}611 \text{ m}$ on the summit of K2 — the world's second-highest mountain, often called the most lethal of the eight-thousanders. He clicks into his skis. He is the first person ever to attempt to ski K2 from the summit to base camp without removing his skis. The slope angle in the upper sections is around $50°$, ice and snow in alternating bands, exposed to a fall of more than two vertical kilometers if he misses an edge.

He skis it. Six hours of mostly steady descent through the Bottleneck, the Black Pyramid, around the séracs of the Shoulder. He arrives at base camp on his own legs, on his own skis, alive.

What kept him on the mountain instead of accelerating off it? Friction. Specifically, the friction of his ski edges against compacted snow and ice. Without friction, a body on a $50°$ slope accelerates at $g \sin 50° \approx 7.5 \text{ m/s}^2$ down the fall line — roughly $25 \text{ km/h}$ added to your speed every second. With friction, the acceleration becomes $g(\sin\theta - \mu_k \cos\theta)$. For waxed steel ski edges on packed snow, $\mu_k$ is something like $0.05$. The acceleration drops from $7.5$ to about $7.2 \text{ m/s}^2$ — barely changed by friction alone. But Bargiel isn't sliding straight down. He's making turns: each turn rotates his ski edges so the friction is doing useful work along his direction of motion, and the geometry can hold him near a steady velocity rather than a runaway acceleration.

Friction is what makes mountains skiable. It is also what makes them climbable, and what determines whether a moving car can stop before the cliff. It is by far the most quantitatively important force on the engineering scale of human activity.

This chapter is about three contact-force laws — friction, drag, and elastic deformation — that fill in the practical content of Newton's framework. Each one is a fit to measurement, not a derivation from microscopic physics. Each one has a story about where it came from and where it stops working. By the end of the chapter you should be able to compute how hard you need to push a stuck crate, how fast a skydiver falls before drag stops her acceleration, and how much a steel beam stretches under load.

**Learning objectives.** By the end of this chapter you should be able to:

1. Distinguish static and kinetic friction; compute each from $f_s \leq \mu_s N$ and $f_k = \mu_k N$, given the relevant coefficient and normal force.
2. Apply the friction laws to objects on level surfaces and on inclined planes, including the limiting angle at which sliding begins.
3. Compute drag force from $F_D = \tfrac{1}{2} C \rho A v^2$ for objects moving through air or water at intermediate speeds, and identify where this expression breaks down (very small or very fast).
4. Compute terminal velocity by setting drag equal to weight, and explain why it depends on mass, area, and the medium's density.
5. Apply Hooke's law $F = k \Delta L$ to predict the deformation of springs and elastic materials under known loads, and identify the elastic limit beyond which Hooke's law fails.

**Prerequisites.** Chapter 4 (Newton's laws, free-body diagrams, $F = ma$). Chapter 3 (vector decomposition for inclined-plane problems). Comfort with trigonometry.

**Why this chapter matters.** Friction is what makes cars accelerate, brakes work, walking possible, and bolts stay tight. Drag determines fuel economy, terminal velocity, the design of airplanes and parachutes, and the speed limit of every projectile through air. Elasticity is what makes structural engineering possible — every beam, every spring, every musical instrument string, every tendon and bone in your body deforms under load according to Hooke's law (within limits). These are the three contact forces real engineering touches.

---

## Concept 1 — Friction: the force that opposes (and enables) motion

### A heavy crate on a concrete floor

A laboratory technician needs to move a $100 \text{ kg}$ wooden crate across a concrete floor. She leans into it and pushes — gently at first, then harder. The crate doesn't move. She pushes harder still. Nothing. Then suddenly, at some threshold of effort, the crate slides. Once it's sliding, she finds she doesn't have to push nearly as hard to keep it moving. If she stops pushing, the crate slides a short distance and stops.

Almost everything quantitative about friction is in that anecdote. Three observations:

1. *Friction can exactly balance an applied force, up to a maximum.* Below that maximum, the crate doesn't move — friction adjusts itself to whatever force is applied.
2. *The maximum static friction is greater than the kinetic friction.* The crate is harder to start than to keep moving.
3. *Friction depends on what's pressing the surfaces together*, not on the area of contact. Add a heavy box on top of the crate and the threshold force to start it moving rises. Switch from concrete to ice and it falls.

These observations, formalized, become the friction laws.

### The mechanism — static and kinetic friction

When two surfaces are in contact and not moving relative to each other, **static friction** $f_s$ acts to prevent relative sliding. It can take any value from zero up to a maximum:

$$f_s \leq \mu_s N,$$

where $N$ is the magnitude of the normal force pressing the surfaces together and $\mu_s$ is the **coefficient of static friction** — a dimensionless number that depends on the two materials in contact. As you push harder, $f_s$ rises to match. Once your push exceeds $\mu_s N$, the surfaces start sliding.

When two surfaces are sliding relative to each other, **kinetic friction** $f_k$ acts to oppose the motion:

$$f_k = \mu_k N,$$

where $\mu_k$ is the **coefficient of kinetic friction**. This is an equality, not an inequality — once sliding begins, kinetic friction has a definite value (under our simplifying assumption that "friction behaves simply"). Crucially, $\mu_k < \mu_s$ for almost every pair of materials. That's why the crate sticks until it suddenly slides, and why you slide a bit further than you intended after stopping the push.

Coefficients of friction are tabulated, but their values are notoriously variable — affected by temperature, humidity, surface preparation, contamination, and how recently the surfaces were last in motion. Here are typical values:

| Surfaces | $\mu_s$ | $\mu_k$ |
|---|---|---|
| Rubber on dry concrete | 1.0 | 0.7 |
| Rubber on wet concrete | 0.7 | 0.5 |
| Wood on wood | 0.5 | 0.3 |
| Steel on steel (dry) | 0.6 | 0.3 |
| Waxed wood on wet snow | 0.14 | 0.1 |
| Teflon on steel | 0.04 | 0.04 |
| Synovial joints in humans | 0.01 | 0.003 |

Notice the human joint at the bottom — biology has engineered nearly frictionless bearings inside your knees and hips with synovial fluid. Ball-bearing assemblies in machinery achieve similar values with metal parts.

A microscopic note: friction at the surface comes from two effects. *Adhesion* — molecular attractions between the two surfaces wherever they touch — and *interlocking* — when the asperities (microscopic bumps) on each surface catch on each other. Both depend on how hard the surfaces are pressed together (determining how many contact points actually touch and how flat they go), which is why both static and kinetic friction scale with $N$.

### The trade-off

The friction laws trade **microscopic accuracy for macroscopic predictive power.** They do not derive from first principles. They are empirical fits — measured for various material pairs, tabulated, used. The values can be off by a factor of two depending on conditions. The reward is that the simple laws ($f_s \leq \mu_s N$, $f_k = \mu_k N$) work well enough to design brakes, predict skidding distances, and engineer climbing ropes. For higher-precision needs (machining tolerances, micromechanics), more sophisticated tribological models exist.

### Worked example — a skier on a slope

A skier with mass $m = 62 \text{ kg}$ glides down a $25°$ slope at constant velocity. What is the coefficient of kinetic friction between her skis and the snow?

**Set up.** The skier moves at constant velocity, so $\mathbf{F}_{\text{net}} = 0$. Free-body diagram: weight $\mathbf{W} = m\mathbf{g}$ straight down; normal force $\mathbf{N}$ perpendicular to the slope, pointing away from the surface; kinetic friction $\mathbf{f}_k$ pointing up the slope (opposing motion).

**Choose axes.** $x$ along the slope (down-slope positive), $y$ perpendicular to the slope (away from surface positive).

**Decompose weight.** Component along the slope: $W \sin\theta = mg \sin 25°$. Component perpendicular to the slope (into the slope): $W \cos\theta = mg \cos 25°$.

**Vertical (perpendicular-to-slope) balance.** $N - mg\cos\theta = 0$, so:

$$N = mg\cos\theta.$$

**Horizontal (along-slope) balance.** Constant velocity means net force along-slope is zero:

$$mg \sin\theta - f_k = 0, \quad \text{so} \quad f_k = mg \sin\theta.$$

**Apply the friction law.** $f_k = \mu_k N$:

$$\mu_k N = mg \sin\theta,$$
$$\mu_k (mg \cos\theta) = mg \sin\theta,$$
$$\mu_k = \tan\theta = \tan 25° \approx 0.466.$$

The coefficient of kinetic friction is about $0.47$.

**Sanity check.** This is higher than the table's value for waxed wood on wet snow ($\sim 0.10$), which suggests her skis are not optimally waxed, or the snow is unusually grippy (cold, sticky), or both. A real ski on real snow with $\mu_k \approx 0.47$ would feel slow — consistent with a beginner on warm spring snow, or any skier on un-waxed equipment. The table value applies under ideal conditions; real ones often differ.

**The general lesson.** Two beautiful results fall out of the slope analysis. First, the mass cancels — the coefficient of friction at constant velocity equals $\tan\theta$, regardless of how heavy the skier is. Second, this gives you a measurement technique: tilt a slope until an object barely slides at constant velocity, then $\mu_k = \tan\theta$. (For static friction: tilt the slope until the object first starts to slide, and $\mu_s = \tan\theta_{\text{just barely}}$.) Geometry plus equilibrium gives you a coefficient.

### Common misconceptions

- *"Friction is proportional to area of contact."* It isn't, in the simple model. A wide tire and a narrow tire on the same car will produce, all else equal, the same friction force from the road — because $f = \mu N$ depends on the total normal force, not how that force is distributed across area. (Real tires have additional effects beyond the simple model.)
- *"Static friction is always equal to $\mu_s N$."* No. Static friction is whatever it has to be to prevent motion, *up to a maximum* of $\mu_s N$. If you push a crate with $50 \text{ N}$ and the maximum static friction is $200 \text{ N}$, static friction is $50 \text{ N}$ — exactly what's needed to hold the crate still.
- *"Friction always opposes motion."* It opposes *relative motion of surfaces.* For a car accelerating from rest, friction from the road on the tires acts *forward* — because the tire's surface is trying to slide *backward* relative to the road, and friction opposes that attempted sliding. The forward force on the car from the road is friction.

↳ **Dig Deeper — Why does $\mu$ depend so much on conditions?**

*The simple $f = \mu N$ model treats $\mu$ as a property of two materials. In reality, it depends on temperature, humidity, surface roughness, contamination, sliding speed, and how recently the surfaces were brought into contact. Modern tribology — the science of friction and wear — explains why, and the answers reach into surface chemistry and statistical mechanics.*

**Prompt:**
> Explain the three main mechanisms that contribute to friction between dry surfaces (adhesion, plowing/asperity interlocking, and elastic/plastic deformation). For each mechanism, name one variable (temperature, humidity, surface preparation, sliding speed) that affects it and how. Then explain why the simple law $f = \mu N$ is independent of contact area in the basic model, and under what real-world circumstances area-independence breaks down (hint: when the deformation under load becomes nonlinear). End with one sentence on how lubricants change the picture.

**What to do with the output:** Save it. Tribology returns implicitly in any mechanical engineering context — bearings, brakes, tire design, prosthetics. The friction laws in this chapter are the entry-level approximation; everything else is correction terms.

---

## Concept 2 — Drag and terminal velocity

### A skydiver leaving the door of a Twin Otter

You jump out of a small aircraft at $4{,}000 \text{ m}$ altitude in a stable face-down body position. Your fall begins like any other fall: you accelerate at $g = 9.80 \text{ m/s}^2$ downward. After about a second, you're falling at $9.80 \text{ m/s}$. The acceleration is still $g$, because air drag at low speeds is small.

Two seconds in, you're at about $19 \text{ m/s}$, still accelerating but a little less. Five seconds in, $40 \text{ m/s}$, and the air pressure on your chest is becoming noticeable. Ten seconds in, $50 \text{ m/s}$ — and you're no longer accelerating. The drag force from the air has caught up with your weight. You've reached **terminal velocity**.

This is the central phenomenon of drag: a falling object does not, in air, keep accelerating forever. It accelerates until the resistive force from the air equals its weight, then continues at constant velocity. For a typical skydiver in a stable face-down position, terminal velocity is around $55 \text{ m/s}$ ($200 \text{ km/h}$). For a skydiver in a streamlined head-down dive, it can exceed $90 \text{ m/s}$. For a skydiver under an open parachute, it drops to about $5 \text{ m/s}$. Same person, vastly different terminal velocities, set by how much surface area is presented to the airflow.

### The mechanism — the drag-force equation

For an object moving through a fluid (gas or liquid) at intermediate speeds — fast enough that the flow becomes turbulent, slow enough that the speed is well below the speed of sound — the drag force is well-approximated by:

$$F_D = \tfrac{1}{2} C \rho A v^2,$$

where:

- $C$ is the dimensionless **drag coefficient**, which depends on the object's shape (typical values: $0.04$ for a streamlined airfoil, $0.5$ for a sphere, $0.7$ for a typical skydiver, $1.0$–$1.3$ for a parachute, $2$ or so for a flat plate face-on).
- $\rho$ is the density of the fluid ($\rho_{\text{air}} \approx 1.21 \text{ kg/m}^3$ at sea level; $\rho_{\text{water}} \approx 1{,}000 \text{ kg/m}^3$).
- $A$ is the cross-sectional area of the object presented to the flow.
- $v$ is the object's speed relative to the fluid.

The $v^2$ scaling is the key feature. Drag at $40 \text{ m/s}$ is $16$ times larger than drag at $10 \text{ m/s}$, not $4$ times. This is why doubling your speed roughly doubles your fuel consumption per kilometer (drag-power scales as $v^3$ — drag force times velocity), and why streamlined cars matter so much more at highway speeds than at city speeds.

The $v^2$ form holds when the flow around the object is turbulent — when fluid is being shoved out of the way faster than the fluid's viscosity can equilibrate it. At very low speeds (or for very small objects, like bacteria swimming or aerosol particles falling), the regime changes: drag becomes proportional to $v$, not $v^2$, and the formula is $F_D = 6\pi \eta r v$ (Stokes drag, for a sphere of radius $r$ in a fluid of viscosity $\eta$). The boundary between the two regimes is set by the Reynolds number, which we'll meet in Chapter 12.

### Terminal velocity

Set drag equal to weight:

$$\tfrac{1}{2} C \rho A v_t^2 = mg,$$

solve for $v_t$:

$$v_t = \sqrt{\frac{2 mg}{\rho C A}}.$$

Note what scales how. Heavier objects fall faster (terminal velocity scales as $\sqrt{m}$). Larger surface area means slower terminal velocity (scales as $1/\sqrt{A}$). Denser fluid (water vs. air) means slower fall (scales as $1/\sqrt{\rho}$). A leaf falls slowly because $A/m$ is large; a stone falls fast because $A/m$ is small.

### The trade-off

The drag equation trades **a clean closed form for a hidden empirical coefficient.** $C$ is not derivable from first principles; it's measured in wind tunnels for each shape. But once you have $C$, the equation predicts force across a wide range of speeds and geometries with one formula. The cost is the coefficient look-up; the benefit is generality.

### Worked example — terminal velocity of a 75 kg skydiver

A $75 \text{ kg}$ skydiver in a stable horizontal position has cross-sectional area $A = 0.70 \text{ m}^2$ and drag coefficient $C = 0.70$. Find her terminal velocity. Take $\rho_{\text{air}} = 1.21 \text{ kg/m}^3$.

$$v_t = \sqrt{\frac{2 \times 75 \times 9.80}{1.21 \times 0.70 \times 0.70}} = \sqrt{\frac{1470}{0.593}} = \sqrt{2479} \approx 49.8 \text{ m/s}.$$

So $v_t \approx 50 \text{ m/s}$, or about $180 \text{ km/h}$.

**Sanity check.** Published terminal velocities for face-down skydivers range from about $50$–$60 \text{ m/s}$, depending on body geometry, suit, and posture. Our $50 \text{ m/s}$ sits in the right range. A head-down "speed-flying" position can reach $100+ \text{ m/s}$ by dropping $A$ and $C$.

**A pull-out calculation: how much altitude to reach terminal velocity?**

Treating the early fall as approximately free-fall ($a \approx g$ until drag becomes significant), it takes about $50 / 9.8 \approx 5 \text{ s}$ to reach terminal velocity. In that time, the skydiver falls roughly $\tfrac{1}{2}(9.8)(5)^2 = 122 \text{ m}$ (a rough overestimate, since drag slows the acceleration even before terminal velocity). So you need at least $\sim 200 \text{ m}$ of altitude to reach terminal velocity. Skydives from $4{,}000 \text{ m}$ spend most of the freefall at terminal velocity, falling at about $50 \text{ m/s}$, taking about $4000/50 = 80$ seconds before parachute deployment.

**The general lesson.** Drag is what turns gravity from "infinite acceleration" into "limited speed." For any object falling through air, after enough time, drag wins. The asymptotic speed (terminal velocity) is set by the geometry of the object (its $C A / m$ ratio) and the medium it falls through. This is why a hammer and a feather in air do *not* fall at the same rate — the feather's much larger $A/m$ ratio gives it a much lower terminal velocity, reached almost immediately. On the airless Moon, no drag, no terminal velocity, both fall at the same rate (Apollo 15, Chapter 2).

### Common misconceptions

- *"Heavier objects always fall faster in air."* Only because they typically have a smaller $A/m$ ratio. A bowling ball and a marble in air fall at roughly the same rate over a short drop because both have low $A/m$. A sheet of paper and a crumpled-up sheet of paper of the same mass fall at very different rates because their $A$ values differ.
- *"Terminal velocity is the speed at which drag exists."* No. Drag exists at every nonzero speed. Terminal velocity is the speed at which drag equals weight, so the *net* force is zero.
- *"You stop accelerating when you reach the speed of sound."* No, that's a different effect (compressibility, sound barrier). Terminal velocity for skydivers ($\sim 50 \text{ m/s}$) is far below the speed of sound ($\sim 340 \text{ m/s}$ in air at sea level).

↳ **Dig Deeper — The Stokes regime: where small things live**

*The drag formula $F_D = \tfrac{1}{2} C \rho A v^2$ used in this chapter holds at "normal" speeds and sizes — bicycles, baseballs, skydivers. For very small objects (bacteria, dust particles, raindrops), the drag is instead proportional to $v$, not $v^2$. This is the Stokes regime, and it has profound consequences for biology and atmospheric science.*

**Prompt:**
> Explain the Stokes drag formula $F_D = 6\pi \eta r v$ for a sphere of radius $r$ moving through a fluid of viscosity $\eta$ at low speed. Derive the terminal velocity for a small sphere falling under gravity in this regime. Then compute the terminal velocity of (a) a $1 \text{ μm}$ bacterium ($\rho \approx 1{,}000 \text{ kg/m}^3$) in water ($\eta = 10^{-3}$ Pa·s), (b) a $1 \text{ mm}$ raindrop in air ($\eta_{\text{air}} = 1.8 \times 10^{-5}$ Pa·s, $\rho_{\text{water}} = 1{,}000 \text{ kg/m}^3$). End with one sentence on what dimensionless number (the Reynolds number) decides whether you're in the Stokes regime or the turbulent regime.

**What to do with the output:** Save it. The Stokes vs. turbulent regimes are foundational for fluid dynamics (Ch. 12) and for any biology or atmospheric science problem at small scale. The bacterium calculation is humbling.

---

## Concept 3 — Elasticity: Hooke's law and the deformation of materials

### A guitar string, a tendon, and a steel cable

Pluck a steel guitar string. It vibrates at a definite frequency determined by its tension, length, and density. Tighten the tuning peg, and the string stretches a measurable amount. The pitch rises.

Stretch a tendon in your wrist by lifting a weight. The tendon — a band of collagen running from forearm to fingers — elongates slightly under load and recovers when you put the weight down.

Hang a heavy load from a steel cable on a construction crane. The cable elongates under load, by an amount you can measure with calipers if you're careful. Remove the load, and the cable returns to its original length.

All three behaviors share a structure. Apply a force; the object deforms. Remove the force; the object recovers. The amount of deformation is proportional to the applied force — at least for small enough deformations. This is **Hooke's law**, and it's the foundation of elasticity.

### The mechanism — Hooke's law

For small deformations of a wide range of materials (metals, springs, rubbers, biological tissues, springs), the deformation is proportional to the applied force:

$$F = k \, \Delta L,$$

where $\Delta L$ is the change in length (or in some other deformation measure) and $k$ is the **spring constant** (or elastic modulus) — a property of the object's geometry and material.

Equivalently:

$$\Delta L = \frac{F}{k}.$$

A stiff object has a large $k$: it deforms little for a given force. A floppy object has a small $k$: it deforms a lot. A typical car suspension spring has $k \sim 30{,}000 \text{ N/m}$. A tendon in your finger might be a few thousand $\text{N/m}$. A piano wire at concert pitch is much higher.

For a uniform rod or wire of length $L_0$, cross-sectional area $A$, and Young's modulus $Y$ (a material property):

$$\Delta L = \frac{1}{Y} \frac{F}{A} L_0.$$

Young's modulus measures intrinsic material stiffness (in units of $\text{N/m}^2 = \text{Pa}$), independent of the rod's particular dimensions. Steel has $Y \approx 200 \times 10^9 \text{ Pa}$. Bone has $Y \approx 9 \times 10^9 \text{ Pa}$ (in compression). Rubber has $Y \approx 10^7 \text{ Pa}$ — about $20{,}000$ times less stiff than steel.

The key insight: Hooke's law is a *linear* approximation. For small deformations, force and displacement are proportional. For larger deformations, the relationship curves — and at some point, the **elastic limit** is exceeded, the material deforms *permanently* (plastic deformation), and beyond that it fractures.

### Three kinds of deformation

Hooke's law generalizes to three modes:

1. **Tension or compression** (along an axis): $\Delta L = \frac{1}{Y} \frac{F}{A} L_0$.
2. **Shear** (perpendicular to the surface): $\Delta x = \frac{1}{S} \frac{F}{A} L_0$, where $S$ is the shear modulus.
3. **Volume change** (uniform pressure): $\Delta V = \frac{1}{B} \frac{F}{A} V_0$, where $B$ is the bulk modulus.

All three have the same algebraic structure: deformation proportional to applied force per unit area, with a material-specific modulus governing the proportionality.

### The trade-off

Hooke's law trades **complete material physics for an excellent linear approximation.** Real materials deviate from Hooke's law as soon as deformations get large enough — the curve flattens, then bends back, then breaks. The linear regime, however, is huge for engineering: most structural beams, springs, and biological tissues operate well within it. The cost is having to know where the limit is for your material; the benefit is a single equation that handles structural design, sensor calibration, musical instrument acoustics, and biomechanics.

### Worked example — stretching a steel cable

A steel cable of length $L_0 = 10.0 \text{ m}$ and cross-sectional area $A = 1.0 \text{ cm}^2 = 1.0 \times 10^{-4} \text{ m}^2$ supports a $1{,}000 \text{ kg}$ load. How much does it stretch? Take $Y_{\text{steel}} = 200 \times 10^9 \text{ Pa}$.

**Identify the force.** $F = mg = 1000 \times 9.80 = 9{,}800 \text{ N}$.

**Apply the formula.**

$$\Delta L = \frac{1}{Y} \frac{F}{A} L_0 = \frac{1}{200 \times 10^9} \times \frac{9800}{1.0 \times 10^{-4}} \times 10.0.$$

$$\Delta L = \frac{9800 \times 10.0}{200 \times 10^9 \times 1.0 \times 10^{-4}} = \frac{98000}{2.0 \times 10^7} = 4.9 \times 10^{-3} \text{ m} = 4.9 \text{ mm}.$$

The cable stretches by about $5 \text{ mm}$, or $0.05\%$ of its length.

**Sanity check.** Steel under typical loads stretches by tiny fractions of its length. Five millimeters in ten meters is consistent with the engineering rule of thumb that steel cables operate in the elastic regime when strain ($\Delta L / L_0$) is less than about $0.001$ — and our strain is $4.9 \times 10^{-4}$, well within. Beyond about $0.002$ strain, structural steel begins to yield permanently.

**The general lesson.** Hooke's law lets you back-calculate material properties from displacement measurements (a strain gauge), or design a structure to a specified maximum deformation. Either direction works; both depend on the linear approximation holding.

### Common misconceptions

- *"Hooke's law works for any deformation."* No — only for small deformations, well below the elastic limit. Beyond that, the linear relationship fails and the material may deform permanently.
- *"Stiffness depends only on the material."* The spring constant $k$ depends on geometry too. A long thin steel rod has a smaller $k$ than a short thick steel rod, even though the material's Young's modulus is the same. Geometry matters.
- *"If a spring stretches twice as far, it must have twice the force."* Within Hooke's law, yes — that's exactly what proportionality means. Outside the linear regime, no.

↳ **Dig Deeper — Stress, strain, and the full stress-strain curve**

*Hooke's law is the linear part of a larger curve called the stress-strain curve. Beyond the linear regime, the curve has named features — yield point, ultimate tensile strength, fracture point — that determine how a real material behaves under heavy load. Engineering materials science is largely the discipline of knowing where on the curve you're operating.*

**Prompt:**
> Sketch (in description) the typical stress-strain curve for a ductile metal like mild steel. Label and explain (a) the linear elastic region (where Hooke's law applies), (b) the yield point (where plastic deformation begins), (c) the strain hardening region, (d) the ultimate tensile strength, (e) the fracture point. Explain what happens to a steel beam stressed to each of these regions if you then unload it. End with one sentence on why ductile metals are preferred over brittle ones for many structural applications, despite brittle materials sometimes being stronger.

**What to do with the output:** Save it. The full stress-strain curve is the foundation of mechanical engineering. The Hooke's-law region we worked with in this chapter is one piece of a larger picture.

---

## Synthesis — three force laws, one Newtonian framework

Three contact forces. Three empirical laws. Each one supplements Newton's $F = ma$ with a specific *expression* for a particular kind of force, allowing the second law to be applied quantitatively in the real world.

**Friction:** $f \leq \mu_s N$ (static), $f = \mu_k N$ (kinetic). Opposes relative motion. Coefficient depends on material pair. Variable in practice.

**Drag:** $F_D = \tfrac{1}{2} C \rho A v^2$ (turbulent regime). Opposes motion through a fluid. Depends on shape, area, fluid density, and crucially on $v^2$.

**Elasticity:** $F = k \Delta L$ (Hooke's law, linear regime). A restoring force from a deformed material. Linear in deformation, with proportionality $k$ depending on geometry and material.

The **scale shift** I want you to feel: these three laws cover an enormous range of physics. Friction governs why a car can stop in $30 \text{ m}$ from $100 \text{ km/h}$ but a Mack truck can't. Drag governs why a $747$ needs $40$ MW of engine power to cruise. Elasticity governs why a guitar string vibrates at the pitch it does and why a bridge can hold up under load. They span seven orders of magnitude in mass and a similar range in length, and they all derive (microscopically) from electromagnetism among the atoms in materials. Yet at human scale, the empirical force laws describe them all without invoking quantum mechanics or microscopics directly.

### A worked example using all three concepts — a downhill skier on a long slope

A skier of mass $70 \text{ kg}$ glides down a long $20°$ slope. The coefficient of kinetic friction between skis and snow is $\mu_k = 0.10$. She's tucked into a crouch with cross-sectional area $A = 0.55 \text{ m}^2$ and drag coefficient $C = 0.80$. Air density $\rho_{\text{air}} = 1.21 \text{ kg/m}^3$.

**Concept 1 (friction):** Normal force on her skis is $N = mg \cos 20° = 70 \times 9.80 \times \cos 20° \approx 645 \text{ N}$. Kinetic friction force: $f_k = \mu_k N = 0.10 \times 645 \approx 64.5 \text{ N}$ up the slope.

**Concept 2 (drag):** Her terminal velocity (when drag balances net gravitational pull along the slope minus friction) satisfies:

$$\tfrac{1}{2} C \rho A v_t^2 = mg \sin 20° - f_k.$$

The right side: $mg \sin 20° - f_k = 70 \times 9.80 \times 0.342 - 64.5 \approx 234.6 - 64.5 = 170.1 \text{ N}$.

Solve for $v_t$:

$$v_t = \sqrt{\frac{2 \times 170.1}{1.21 \times 0.80 \times 0.55}} = \sqrt{\frac{340}{0.532}} = \sqrt{639} \approx 25.3 \text{ m/s}.$$

About $91 \text{ km/h}$. That's a fast-but-attainable downhill speed for a recreational skier in a tuck — the terminal velocity reached when drag has caught up with the gravity-minus-friction net.

**Concept 3 (elasticity):** Her ski poles, planted briefly during a turn, deform under load. If a pole is $1.2 \text{ m}$ long, $1.0 \text{ cm}^2$ cross-section, made of aluminum ($Y_{\text{Al}} \approx 70 \times 10^9 \text{ Pa}$), and she briefly puts $200 \text{ N}$ of force through it:

$$\Delta L = \frac{F L_0}{Y A} = \frac{200 \times 1.2}{70 \times 10^9 \times 1.0 \times 10^{-4}} = \frac{240}{7.0 \times 10^6} \approx 3.4 \times 10^{-5} \text{ m} = 34 \text{ μm}.$$

The pole compresses by $34$ micrometers — invisible to the eye, well within the elastic limit, and entirely recoverable when she lifts it.

The whole picture: friction (static for grip on her edges, kinetic for the long-glide drag along snow), drag (the terminal-speed limit set by air resistance), and elasticity (the slight deformation in every piece of her gear under load). All three forces operating simultaneously, all describable by Newton's framework of $F = ma$ once you have the force laws to substitute in.

---

## Exercises

### Warm-up

**5.1** *(LO 1)* A $100 \text{ N}$ horizontal force is applied to a $50 \text{ kg}$ box on a level floor. Coefficients: $\mu_s = 0.4$, $\mu_k = 0.3$. (a) Compute the maximum static friction. (b) Will the box move? (c) If yes, what is the kinetic friction force?

**5.2** *(LO 1)* A box rests on a ramp. The angle is slowly increased. The box first slips at $\theta = 30°$. What is $\mu_s$?

**5.3** *(LO 3)* A $0.145 \text{ kg}$ baseball with $A = 0.0042 \text{ m}^2$ and $C = 0.40$ moves at $40 \text{ m/s}$ through air ($\rho = 1.21 \text{ kg/m}^3$). What is the drag force?

**5.4** *(LO 5)* A spring stretches $5.0 \text{ cm}$ when a $2.0 \text{ kg}$ mass hangs from it. What is the spring constant $k$?

### Application

**5.5** *(LO 2)* A $50 \text{ kg}$ crate is pushed up a $20°$ ramp at constant velocity. Coefficient of kinetic friction is $\mu_k = 0.30$. (a) Draw the free-body diagram. (b) What pushing force (parallel to the ramp) is required?

**5.6** *(LO 1, 2)* A car of mass $1{,}500 \text{ kg}$ brakes from $25 \text{ m/s}$ to a stop on dry pavement ($\mu_k = 0.7$). (a) What is the friction force? (b) What is the deceleration? (c) How far does the car travel before stopping?

**5.7** *(LO 3, 4)* A $60 \text{ kg}$ skydiver has $A = 0.50 \text{ m}^2$ and $C = 0.70$. (a) Compute her terminal velocity. (b) When she opens her parachute, $A$ increases to $30 \text{ m}^2$ and $C$ becomes $1.4$. What is her new terminal velocity?

**5.8** *(LO 5)* A nylon climbing rope of length $50 \text{ m}$ and cross-sectional area $1.0 \text{ cm}^2$ supports a $80 \text{ kg}$ climber. Take $Y_{\text{nylon}} \approx 5 \times 10^9 \text{ Pa}$. How much does the rope stretch?

### Synthesis

**5.9** *(LO 2, 4)* A skier of mass $70 \text{ kg}$ glides down a $25°$ slope. The kinetic friction coefficient is $\mu_k = 0.05$. Her drag area is $A = 0.50 \text{ m}^2$, $C = 0.70$, $\rho_{\text{air}} = 1.21 \text{ kg/m}^3$. Find her terminal velocity down the slope.

**5.10** *(LO 1, 5)* A $20 \text{ kg}$ box is suspended from a vertical spring with $k = 5{,}000 \text{ N/m}$. The system is at rest. (a) What is the spring's stretch? (b) If you press down on the box with $30 \text{ N}$ additional force (and hold it stationary), how much further does the spring stretch? (c) If, instead of pressing on the box, you pull it down by $1 \text{ cm}$ and release, what is the initial restoring force?

**5.11** *(LO 1, 3)* A bicyclist coasts down a hill of slope $5°$ at terminal speed of $15 \text{ m/s}$. Bicycle plus rider mass is $80 \text{ kg}$. Drag area $A = 0.50 \text{ m}^2$, $C = 1.0$, $\rho_{\text{air}} = 1.21 \text{ kg/m}^3$. (a) Compute the drag force at terminal speed. (b) Compute the rolling friction force (the residual after gravity and drag are accounted for). (c) What's the implied "rolling coefficient"?

### Challenge

**5.12** *(LO 4, beyond chapter)* Find the terminal velocity of a $1.0 \text{ μm}$ bacterium ($\rho = 1{,}000 \text{ kg/m}^3$) in water ($\eta = 10^{-3}$ Pa·s) using Stokes drag $F_D = 6 \pi \eta r v$. Compare to the bacterium's own swimming speed (about $30 \text{ μm/s}$). What does this say about why bacteria need flagella to get anywhere useful?

**5.13** *(LO 5, beyond chapter)* A vertical steel column $5 \text{ m}$ long supports a $50{,}000 \text{ kg}$ load. (a) For the column not to compress by more than $1 \text{ mm}$, what must its cross-sectional area be? (Use $Y_{\text{steel}} = 200 \times 10^9$ Pa.) (b) Once the area is computed, what is the stress (force per area) on the column? (c) Look up steel's yield stress and verify the column is well within its elastic limit.

---

## LLM Exercise — Chapter 5: Friction, Drag, and Elasticity in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** Quantitative estimates of one friction, one drag, or one elastic-deformation effect in your anchor phenomenon.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 5, I want to apply one or more of: friction laws, drag equations, or Hooke's law to my phenomenon. Please:

1. Identify ONE relevant friction, drag, or elastic effect in my phenomenon. Examples:
   - Bike commute: rolling friction of tires against road; air drag at cruising speed; tire deformation under weight (Hooke's law in compressed rubber).
   - Coffee maker: friction in the pump; drag of water through coffee grounds; spring loading on the brewing chamber gasket.
   - Basketball: drag on the ball during flight; friction between hand and ball at release; deformation of ball on impact with rim.
   - Marathon: friction at each footstrike (preventing slip); drag at running speed; tendon/Achilles deformation under load.
   - Espresso: friction in the puck during 9-bar extraction; drag of water through grounds; spring force in the pressure relief valve.

2. Identify the relevant equation ($f = \mu N$, $F_D = \tfrac{1}{2} C \rho A v^2$, $F = k \Delta L$).

3. Estimate the relevant inputs: coefficient, area, density, spring constant. For each: where to source the value and what uncertainty to expect.

4. Compute the force or deformation. Report with units, sig figs, and percent uncertainty.

5. Sanity-check with one Fermi estimate.

6. Identify which assumption (linear elasticity, constant μ, constant C, ignored Reynolds-regime change) is most likely to bite.

7. One sentence on what energy is lost to this force (preview Chapter 7).

Save the output as logbook/chapter-05-friction-drag-elasticity.md.
```

### What this produces

A fifth Logbook entry: a quantitative force-law analysis applied to your phenomenon, often surprising in magnitude. (How big is rolling friction on a bike? Bigger than you think at low speeds, smaller than drag at high speeds.)

### How to adapt this prompt

- *For phenomena that are mostly steady-state* (a coffee maker at equilibrium, a marathon at race pace): emphasize force *balance* — what equals the friction or drag.
- *For ChatGPT or Gemini:* identical with interface substitutions.
- *For Claude Code:* if you have video data (e.g., a basketball trajectory you can frame-grab) you can compute drag from the deceleration; pase the data.

### Connection to previous chapters

Builds on Chapter 4 (force, $F = ma$) by giving you specific force laws for contact and deformation. Builds on Chapter 3 (vector decomposition) for inclined-plane work and any 2D friction problem.

### Preview of next chapter

Chapter 6 takes Newton's laws to circular motion and gravitation. The Chapter 6 LLM Exercise will look at any circular or rotational element in your phenomenon (a tire turning, a stirrer, a swung arm, a curved running path) and apply centripetal-force analysis.

---

## Chapter summary

Three contact-force laws. **Friction**: $f \leq \mu_s N$ before sliding, $f = \mu_k N$ during sliding; depends on the materials and the normal force, not the contact area; coefficients are tabulated and approximate. **Drag**: $F_D = \tfrac{1}{2} C \rho A v^2$ at intermediate speeds; turns gravity-driven free fall into terminal-velocity descent; depends crucially on $v^2$. **Elasticity**: $F = k \Delta L$ in the linear (Hooke's-law) regime; below the elastic limit, deformation is recoverable and proportional to load.

The one idea that matters most: **these are empirical force laws, not derivations from first principles.** They work — well — within their domains, fitted to measurement. Outside those domains they fail, and you reach for more sophisticated tools (tribology, the full Navier-Stokes equations, the full stress-strain curve). Knowing the domain is part of knowing the law.

The common mistake to watch for: **applying the force law outside its regime.** Hooke's law breaks at the elastic limit. The $v^2$ drag law breaks at very low speeds (use Stokes) and very high speeds (compressibility). The $f = \mu N$ law breaks when contact-area effects matter or when $N$ is so large the surface plastically deforms. Most freshman-physics errors with these laws are domain errors, not arithmetic errors.

What you should now be able to teach someone else: how to apply each of the three laws to a standard problem, how to compute terminal velocity by setting drag = weight, and how to find friction coefficients by tilting a slope until an object barely slides. Three skills, one underlying framework: each force law tells you what to substitute into Newton's $F = ma$ for a given physical interaction.

---

## What would change my mind

The chapter argues that these three empirical laws are sufficient for most engineering-scale prediction of contact forces. The argument would need revision if a class of common engineering problems systematically required corrections beyond these laws — they often need corrections (lubrication regimes, viscoelasticity, finite-deformation elasticity), but those corrections are layered on the three core laws here, not replacements for them.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **why is friction so well-described by such a simple law?** Microscopic surfaces are atomically rough, contaminated, dynamically rearranging under load. The naive expectation would be that friction behaves complicatedly. Instead, $f \approx \mu N$ holds, often, to within a factor of two, across enormous variations in conditions. Modern tribology offers partial explanations (real contact area, asperity flattening, plastic vs. elastic deformation regimes), but the depth of agreement between the simple law and observation remains philosophically striking — Feynman called friction "still the most poorly understood common phenomenon in classical physics," and that's not entirely wrong.

---

## Connections forward

Chapter 6 applies Newton's laws (and the contact-force laws from this chapter) to circular motion: the friction between car tires and a curved road sets the maximum speed at which a car can round a turn without skidding. Gravity, too, gets the inverse-square treatment. Chapter 7 introduces energy as an alternative accounting; friction and drag will be the principal mechanisms by which mechanical energy converts to heat. Chapter 9 (statics) uses the elasticity framework here to handle small deformations of structures under load. Chapter 12 (fluid dynamics) gives the deeper story behind the drag equation, including the Reynolds number that decides which regime you're in.

---

**Tags:** friction, drag, Hookes-law, terminal-velocity, contact-forces

---

## AI Wayback Machine

**Charles-Augustin de Coulomb** was an 18th-century French physicist who quantified friction in his 1781 prize-winning essay — distinguishing static from kinetic friction, characterizing the role of normal force, and producing the laws we still teach. He's mostly remembered for electricity, but he founded mechanical friction theory.

**Run this:**

```
Who was Coulomb, and how does his work on friction connect to the Newton's-law applications we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Charles-Augustin de Coulomb"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Coulomb's empirical laws of friction — which still hold up under modern materials science?
- Ask it about Coulomb's parallel career as a military engineer in the French colonies.

What changes? What gets better? What gets worse?
