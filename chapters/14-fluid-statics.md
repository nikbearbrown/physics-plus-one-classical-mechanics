# Chapter 14 — Fluid Statics

*At the bottom of the ocean, everything weighs the same per square inch — and that inch has to hold.*

---

In 2019, Victor Vescovo descended in a titanium submersible called the *Limiting Factor* to the bottom of the Challenger Deep: 10,928 meters below the surface of the Pacific Ocean, the deepest place on Earth. The descent took four hours. At that depth, the pressure outside the hull is roughly 1,100 times atmospheric — about 110 megapascals, or 16,000 pounds per square inch.

To survive this, the crew sphere is a 9-centimeter-thick titanium shell machined to sub-millimeter precision. Every square inch of its outer surface is being squeezed by the equivalent of ten compact cars stacked on top of it.

How do you know the pressure before you go? You don't send a pressure gauge down first. You calculate. The depth is known. The density of seawater is known — about 1,030 kg/m³. Multiply by gravitational acceleration and depth:

$$P = \rho g h = 1030 \times 9.80 \times 10{,}928 \approx 1.10 \times 10^8 \text{ Pa.}$$

That is 110 MPa. The engineers who designed the sphere used that number, derived from nothing more than the weight of a column of water divided by area, to calculate how thick the walls had to be. The submersible was built. Vescovo went down. He came back up. The formula was right.

This chapter is about that formula, why it is right, and what else follows from the same logic. Pressure in a fluid. Why pressure increases with depth. Why an enclosed fluid transmits pressure everywhere (the hydraulic jack). And why things float — which Archimedes figured out in a bath around 250 BCE and which has not required revision since.

---

## Density and Pressure

Two quantities underlie everything else.

**Density** is mass per unit volume:

$$\rho = \frac{m}{V}.$$

Some values worth knowing: fresh water at 4°C has density 1,000 kg/m³; seawater, about 1,030 kg/m³; air at sea level, 1.21 kg/m³. The factor-of-a-thousand difference between water and air sets up all of buoyancy. Aluminum is 2,700 kg/m³; steel 7,800; gold 19,300. Gold is nearly twenty times denser than water — which is why Archimedes's trick works: a gold crown and a fake crown of the same mass will displace very different volumes of water.

**Pressure** is force per unit area:

$$P = \frac{F}{A}.$$

Units: pascals, where 1 Pa = 1 N/m². Atmospheric pressure at sea level is about 101,325 Pa, or 1 atm. One atmosphere is also about 14.7 psi, or 760 mmHg (used in blood pressure). The pascal is a tiny unit — you need 100,000 of them to get to atmospheric pressure — so pressure in practical settings often gets expressed in kilopascals or megapascals or atmospheres instead.

The same force distributed over different areas gives different pressures. A 70 kg person wearing regular boots (total contact area about 0.06 m²) presses on snow with about 11,400 Pa. The same person in snowshoes (area 0.40 m²) presses with about 1,700 Pa — a factor of nearly seven less. Snow that would collapse under the boots holds up under the shoes. Same weight. Different pressure. Different outcome.

Now here is the key property of pressure in a fluid, the one that makes fluid statics different from solid mechanics. Inside a static fluid, at any point, the pressure is the same in every direction. Push a tiny imaginary cube of water — the pressure on its top face equals the pressure on its bottom face, its left face, its right face, all faces. Pressure in a fluid is not a vector. It is a scalar. It has magnitude but no direction.

This is what distinguishes a fluid from a solid. A solid beam can be compressed along one axis while being tensed along another. A static fluid cannot sustain different pressures in different directions — any imbalance would set the fluid in motion, and we have stipulated it is static. The directional complexity collapses to a single number per point, $P(x, y, z)$. Once you know that scalar field, you know all the forces the fluid exerts on any surface you care about: multiply by area, and the force is perpendicular to the surface.

<!-- → DIAGRAM: a small cube of fluid shown with pressure arrows on all six faces — each arrow labeled P and equal in magnitude; compare with a neighboring panel showing a solid block with different-length arrows on different faces (labeled σ_xx ≠ σ_yy); caption: "In a static fluid, pressure is the same in every direction — a scalar. In a solid, normal stress can differ by axis." Student should see the key distinction before any formula appears. -->

---

## Pressure with Depth

The depth-pressure formula has the simplest possible derivation. Imagine a column of fluid with cross-section $A$ extending from the surface down to depth $h$. The fluid in the column has mass $\rho A h$. Its weight is $\rho A h g$. That weight is supported by the pressure at the bottom of the column minus the pressure at the top:

$$(P_{\text{bottom}} - P_{\text{top}}) \times A = \rho A h g.$$

Dividing through by $A$:

$$P_{\text{bottom}} = P_{\text{top}} + \rho g h.$$

If the surface is exposed to the atmosphere at pressure $P_0$, then the pressure at depth $h$ is:

$$P = P_0 + \rho g h.$$

<!-- → DIAGRAM: a vertical fluid column of cross-section A extending from the surface to depth h — the top labeled P_top = P_0 with a downward arrow, the bottom labeled P_bottom with an upward arrow, the column itself labeled "mass = ρAh, weight = ρAhg"; a bracket alongside shows the depth h; the derivation steps (P_bottom − P_top) × A = ρAhg are written in a callout; student should see exactly where the formula comes from and why area cancels -->

Notice what does not appear in this formula: the area of the column, the shape of the container, or the total volume of the fluid. The pressure at depth $h$ depends only on the density of the fluid, the gravitational acceleration, and the depth. A narrow laboratory cylinder and a wide ocean basin have exactly the same pressure at 10 meters below their surfaces if both are filled with water. This seems surprising until you see the derivation: it is simply the weight of the column above, per unit area. The width of the container is irrelevant.

<!-- → DIAGRAM: three containers side by side — a narrow graduated cylinder, a wide flat aquarium, and an oddly shaped vessel (wider at top, narrow at bottom) — all filled to the same height h of water; at the bottom of each, an identical pressure label P = P_0 + ρgh; student should see that shape and width make no difference, only depth matters -->

Every meter of fresh water adds $\rho g \times 1\text{ m} = 1000 \times 9.80 \approx 9{,}800$ Pa — about 0.097 atmospheres. Ten meters of water adds almost exactly one atmosphere. This is why scuba divers feel ear pressure at depth and why free divers must equalize frequently. It is also why a swimming pool 2 meters deep, at the bottom, is at 1.2 atmospheres absolute — one atmosphere from the air above, plus 0.2 from the water column.

Now a thought that is easy to miss: this formula assumes the fluid is incompressible and that $g$ is constant. For water, both assumptions are excellent even at thousands of meters of depth — water is nearly incompressible. For air, neither assumption holds well over large altitude ranges. Air is compressible; its density decreases with altitude in a way that must be accounted for by integrating rather than simply multiplying. The linear formula still works over short altitude ranges, but corrects for mountain height, airplane cabins, and atmospheric science need the integral form. The Mariana Trench calculation at the chapter's opening works precisely because seawater is nearly incompressible.

---

## Pascal's Principle and Hydraulic Systems

Here is a fact about enclosed fluids that follows from the depth-pressure relation. Suppose you have a sealed container of fluid — no free surface — and you increase the pressure at one point by pushing on a piston. The pressure at every other point in the fluid increases by the same amount. This is Pascal's principle: pressure applied to an enclosed fluid is transmitted undiminished to every part of the fluid and to the walls of the container.

The proof is in the formula. $P = P_0 + \rho g h$. If $P_0$ increases by $\Delta P$, then $P$ at every depth increases by $\Delta P$. The geometry is irrelevant — the increment propagates.

The hydraulic jack exploits this. A small piston of area $A_1$ is pushed down with force $F_1$, increasing the pressure in the fluid by $\Delta P = F_1 / A_1$. A large piston of area $A_2$ on the other side of the fluid experiences the same pressure increase, generating a force:

$$F_2 = \Delta P \times A_2 = F_1 \times \frac{A_2}{A_1}.$$

<!-- → DIAGRAM: cross-section of a hydraulic jack — a small piston on the left (labeled A_1, F_1 ↓) connected via fluid to a large piston on the right (labeled A_2, F_2 ↑, with A_2 ≫ A_1); the same ΔP arrow points into both fluid columns; below the diagram, two annotations: "force amplification = A_2/A_1" and "distance ratio = A_1/A_2 (large piston moves less)"; student should see both the force amplification and the distance trade-off in one image -->

If the large piston has fifty times the area of the small one, you get fifty times the force. A modest push produces a force large enough to lift a car.

This is not free energy. Energy is conserved. The large piston moves $A_1/A_2$ times as far as the small one. Work in (small force times large distance) equals work out (large force times small distance). Pascal's principle redistributes force at the cost of distance — exactly the same trade as a mechanical lever, expressed in fluid rather than rigid-body language. A hydraulic jack is a lever with an arbitrarily adjustable ratio, set by the ratio of piston areas.

The hydraulic brake system in your car works the same way. You push on a small pedal; the master cylinder transmits the pressure to brake cylinders at each wheel that have larger areas; the calipers grip the rotors with forces much larger than your foot could produce directly. The fluid is the mechanical linkage. Unlike a cable, it can route around corners, through complex geometry, to every wheel simultaneously.

---

## Archimedes' Principle

Around 250 BCE, Archimedes of Syracuse was asked whether King Hiero's crown was pure gold or had been adulterated with silver. The density argument was obvious in retrospect: gold and silver have different densities, so a crown of the same mass would have different volumes if it contained silver. But how to measure the volume of an irregular shape? The legend says a bath gave him the insight — water displaced by a submerged object reveals the object's volume. The principle he arrived at is more powerful than just volume measurement.

The buoyant force on any object submerged in a fluid equals the weight of the fluid the object displaces.

The derivation is clean. Consider a cube submerged in fluid with its top face at depth $h_1$ and bottom face at depth $h_2 = h_1 + L$. Pressure on the top face: $P_0 + \rho g h_1$, pushing down. Pressure on the bottom face: $P_0 + \rho g h_2$, pushing up. Net upward force:

$$(P_0 + \rho g h_2 - P_0 - \rho g h_1) \times A = \rho g (h_2 - h_1) \times A = \rho g L A = \rho g V.$$

<!-- → DIAGRAM: a cube submerged in fluid — top face at depth h_1 with a downward pressure arrow labeled P_top = P_0 + ρgh_1; bottom face at depth h_2 = h_1 + L with a larger upward pressure arrow labeled P_bottom = P_0 + ρgh_2; the side faces show equal horizontal arrows (they cancel); a net upward arrow labeled F_buoy = ρgV appears beside the cube; the caption notes: "bottom pressure exceeds top pressure by ρgL — that difference times area gives the buoyant force" -->

Here $V = LA^2$ is the cube's volume and $\rho g V$ is the weight of a volume $V$ of fluid — the weight of the displaced fluid. The argument generalizes to any shape, because any shape can be decomposed into small cubes.

Whether an object sinks or floats comes down to a comparison of densities. If the object's density is greater than the fluid's, its weight exceeds the maximum buoyant force (when fully submerged), and it sinks. If less, the buoyant force when fully submerged exceeds the weight, and the object rises until it is only partially submerged — floating at whatever depth brings the buoyant force back into balance with the weight.

A floating object displaces a weight of fluid equal to its own weight. This is worth pausing on. An iceberg whose density is 917 kg/m³ in fresh water (density 1,000 kg/m³) submerges $917/1000 = 91.7\%$ of its volume. In seawater (1,030 kg/m³), it submerges $917/1030 = 89\%$. The famous "nine-tenths underwater" is close to correct for seawater. The exact fraction depends only on the ratio of densities.

<!-- → DIAGRAM: an iceberg cross-section — the full volume drawn as a vertical rectangle; a waterline cuts across it; above the waterline labeled "~11% visible" with hatching; below labeled "~89% submerged (seawater)"; a second smaller panel shows the same iceberg in fresh water with slightly more submerged (~92%); beneath both: "submerged fraction = ρ_ice / ρ_fluid — only the density ratio matters" -->

A steel ship floats not because steel is less dense than water — steel is about 7.8 times denser. It floats because the average density of the ship as a whole (steel hull plus enclosed air) is less than water. The hull's volume gives the ship enough displacement capacity that the buoyant force, spread across all that volume, exceeds the ship's weight. Fill the hull with water — which eliminates the air — and the average density becomes much greater than water's, and the ship sinks. The Titanic sank not because water is heavier than steel but because flooding the compartments eliminated the air volume that gave the ship its buoyancy.

**The gold crown, quantitatively.** A crown weighs 7.84 N in air. Submerged in water, it reads 6.84 N on the scale. The buoyant force is $7.84 - 6.84 = 1.00$ N. By Archimedes' principle, this equals the weight of the displaced water: $F_b = \rho_\text{water} g V$, so $V = 1.00 / (1000 \times 9.80) \approx 1.02 \times 10^{-4}$ m³. The mass of the crown is $7.84/9.80 = 0.800$ kg. Its density is therefore $0.800 / (1.02 \times 10^{-4}) \approx 7{,}840$ kg/m³. Gold's density is 19,300 kg/m³. The crown is not pure gold. Archimedes was right to be suspicious, and now you know exactly how suspicious to be.

---

## The Pressure Field From Trench to Teacup

Return to the opening. Why does the depth-pressure formula work across such a vast range — from a 2-meter swimming pool to an 11-kilometer ocean trench? Because it is, at its core, just Newton's second law applied to a column of fluid in equilibrium. The weight of the fluid above pushes down; the pressure from the fluid below pushes up; they balance. The formula $P = P_0 + \rho g h$ is Newton's first law for a fluid column. Nothing more.

The same logic that produces 9,800 Pa per meter of water produces 110 MPa at 11,228 meters. The multiplier is the depth. The machinery is identical. This is the kind of universality that is worth pausing to appreciate: a formula derived by balancing the weight of a thin fluid layer works equally well for a teacup and for the deepest trench in the ocean.

The limits of the formula are worth noting. Water is nearly incompressible, so $\rho$ stays constant — the formula is exact to within fractions of a percent even at full ocean depth. Air is not: its density falls off exponentially with altitude, and integrating the formula gives an exponential rather than linear pressure-altitude relation. But for everyday heights — a few hundred meters — the linear approximation holds well. The correction matters for airplane cabins, mountaineering, and atmospheric science, not for hydraulics or diving.

What the formula does not contain: the horizontal extent of the fluid, the shape of the container, the position in the horizontal plane. Pressure in a static fluid is a function only of depth (and the surface conditions). This simplicity is the gift of isotropy. Because the fluid has no preferred direction, the pressure field has no preferred horizontal direction. It varies only with the one remaining variable: vertical position.

---

## What Would Change My Mind

The incompressible-static-fluid framework, with $P = \rho g h$ and Archimedes' principle, has been tested against everything from ship design to submarine engineering to blood pressure physiology, and it has not failed at the scales where its assumptions hold. The argument would require revision if a class of fluids routinely violated the incompressible assumption at pressures where the formula is commonly applied — but water, which is by far the most common fluid in engineering and biology, is compressible by only about 0.05% per atmosphere. At Mariana Trench pressures, the true density of seawater is about 5% higher than surface density — a small but real correction that deeper precision calculations must include.

## Still Puzzling

Why is pressure isotropic in a static fluid? The mechanics argument — fluids cannot sustain static shear, so the stress tensor must be isotropic — is correct, but its molecular basis is in statistical mechanics: the thermal motion of molecules distributes momentum equally in all directions, and at equilibrium the time-averaged pressure from molecular collisions is the same on every face of any small element. We will not reach kinetic theory until Chapter 19. Until then, isotropy is a fact to use; the reason it is true requires a different framework.

---

## Exercises

### Warm-up

**1.** A 5.0 kg block of aluminum ($\rho = 2{,}700$ kg/m³) is placed in a tank of water. (a) What is its volume? (b) What is the buoyant force when fully submerged? (c) Does it sink or float? Explain using density, not force.

*Tests: density calculation; buoyant force from Archimedes; float/sink criterion.*

**2.** A force of 600 N is applied to a surface of area 0.015 m². (a) What is the pressure in Pa? (b) Convert to atm and psi. (c) Is this above or below atmospheric pressure?

*Tests: $P = F/A$; unit conversion.*

**3.** What is the gauge pressure (above atmospheric) at a depth of 8.0 m in fresh water? Express in Pa and in atm.

*Tests: $P = \rho g h$ for gauge pressure; 9,800 Pa/m rule.*

**4.** A 2.0 kg object weighs 18 N in air and 12 N when fully submerged in water. (a) What is the buoyant force? (b) What is the object's volume? (c) What is its density? (d) Does it sink or float in seawater ($\rho = 1{,}030$ kg/m³)?

*Tests: buoyant force from apparent weight difference; Archimedes applied to density measurement.*

---

### Application

**5.** A hydraulic lift has a small piston of area $15 \text{ cm}^2$ and a large piston of area $600 \text{ cm}^2$. (a) What input force is needed to lift a 1,200 kg car? (b) If the small piston moves down 25 cm, how far does the car rise? (c) How much work is done by the input force? By the output force? Are they equal?

*Tests: Pascal's principle for force amplification; energy conservation check.*

**6.** A scuba diver descends to 30 m depth in seawater ($\rho = 1{,}030$ kg/m³). (a) What is the absolute pressure at that depth? Express in Pa and atm. (b) If the diver's tank delivers air at the same pressure as the surrounding water, what pressure is the air inside at 30 m?

*Tests: absolute vs. gauge pressure; $P = P_0 + \rho g h$ with seawater density.*

**7.** A wooden block ($\rho_{\text{wood}} = 650$ kg/m³, volume $0.0040$ m³) floats in fresh water. (a) What fraction of the block is submerged? (b) What is the mass of water displaced? (c) What is the weight of displaced water, and how does it compare to the block's weight?

*Tests: floating fraction = density ratio; displaced-weight equals object weight.*

**8.** The Mariana Trench calculation from the chapter opening: verify that $P = \rho g h$ at $h = 10{,}928$ m in seawater ($\rho = 1{,}030$ kg/m³) gives approximately 110 MPa. Then express this in atmospheres and in psi. Confirm it is roughly 1,100 times atmospheric pressure.

*Tests: direct application of depth-pressure formula; unit conversions at extreme scales.*

---

### Synthesis

**9.** A hollow steel sphere (outer radius 0.15 m, inner radius 0.12 m, steel density 7,800 kg/m³) is placed in seawater. (a) Calculate the mass of steel in the sphere. (b) Calculate the buoyant force when fully submerged. (c) Does it float or sink? (d) If it floats, what fraction protrudes above the waterline? If it sinks, how much additional air volume (sealed inside) would be needed to make it neutrally buoyant?

*Tests: average density of a composite object; buoyancy applied to a hollow structure; connecting to ship/submarine design.*

**10.** A person's blood pressure is measured as 120/80 mmHg at heart level. The person stands upright. Blood ($\rho_{\text{blood}} \approx 1{,}060$ kg/m³) must travel from the heart to the brain (approximately 30 cm above heart level) and to the feet (approximately 120 cm below heart level). (a) What is the hydrostatic pressure increase in the blood at foot level compared to heart level? Express in mmHg and in Pa. (b) What pressure must the heart supply to push blood upward to the brain against the hydrostatic gradient? (c) Why might standing for long periods cause fluid to pool in the legs?

*Tests: $P = \rho g h$ applied to physiology; reasoning about hydrostatic gradient in a living system; connecting to real medical phenomena.*

---

### Challenge

**11.** Design problem: you want to build a submersible that can descend to 500 m in seawater. The crew sphere must maintain interior pressure at 1 atm. (a) What is the exterior pressure at 500 m? (b) What is the pressure difference the hull must withstand, in MPa? (c) The sphere has inner radius 0.80 m. If the hull material has a compressive yield strength of 500 MPa and the required safety factor is 3, what minimum wall thickness is needed? (Use the thin-shell approximation: wall stress $= \Delta P \times r / (2t)$ where $t$ is wall thickness.) (d) Compare to the 9 cm titanium hull of the *Limiting Factor* at 11 km.

*Tests: $P = \rho g h$ at engineering scale; thin-shell stress analysis; connecting chapter physics to actual design constraints.*

---

## LLM Exercise — Chapter 14: Fluid Statics in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** A pressure or buoyancy analysis of one fluid element in your anchor phenomenon.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics
with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 14, I want to apply fluid statics — pressure, depth,
buoyancy — to one fluid in my phenomenon. Please:

1. Identify ONE fluid element in my phenomenon (a static fluid or
   a fluid at near-equilibrium). Examples:
   - Bike commute: tire pressure (gauge vs. absolute); pressure
     under each wheel.
   - Coffee maker: pressure of the water column above the heating
     element; pressure at the brewing chamber gasket.
   - Basketball: pressure inside the inflated ball.
   - Marathon: blood pressure in the runner's circulatory system
     at heart vs. feet (hydrostatic gradient).
   - Espresso: pressure profile in the puck during 9-bar
     extraction (the static piece can be analyzed first).

2. Identify the relevant fluid statics quantity: pressure, depth,
   density, buoyancy.

3. Compute it using P = F/A, P = ρgh, or Archimedes' principle
   as appropriate.

4. Express the result in multiple units (Pa, atm, mmHg, psi as
   appropriate).

5. Sanity check: does the magnitude match what you'd expect?
   (Tire pressures ~a few atm; blood pressure ~100 mmHg systolic;
   a basketball ~8 psi gauge.)

6. Identify which assumption (incompressible, static, no
   temperature gradient) is most likely to bite.

7. One sentence on how this connects to Chapter 15 (fluid
   dynamics) — when fluid moves, pressure becomes part of an
   energy budget along with kinetic energy and elevation.

Save the output as logbook/chapter-14-fluid-statics.md.
```

### What this produces

A Logbook entry: a fluid-statics analysis of one element in your phenomenon, often surprising in the magnitudes.

### How to adapt this prompt

- *For phenomena with no obvious fluid* (a basketball shot in air): the air around the ball is a fluid; air pressure changes with altitude can be relevant.
- *For ChatGPT or Gemini:* identical with substitutions.
- *For Claude Code:* if you have pressure-time data (e.g., from a pressure sensor), paste it for analysis.

### Connection to previous chapters

Builds on Chapter 6 (force, here as pressure × area), Chapter 9 (energy in hydraulic systems), Chapter 12 (statics — fluid statics is a special case of static equilibrium).

### Preview of next chapter

Chapter 15 takes fluids into motion. Bernoulli's principle relates fluid speed to pressure along a streamline: $P + \rho g h + \frac{1}{2}\rho v^2 = \text{constant}$. The continuity equation describes how flow speed changes with pipe cross-section. Together they predict everything from Venturi meters to airplane lift to blood flow through arteries.

---

## AI Wayback Machine

**Blaise Pascal** worked out fluid pressure in the 1640s — including the principle that any pressure applied to an enclosed fluid is transmitted undiminished throughout. Modern hydraulic systems are still applications of Pascal's principle.

**Run this:**

```
Who was Blaise Pascal, and how does Pascal's principle connect to
the fluid statics we covered in this chapter? Keep it to three
paragraphs. End with the single most surprising thing about his
career or ideas.
```

→ Search **"Blaise Pascal"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how a hydraulic press multiplies force using Pascal's principle.
- Ask it about Pascal's parallel career inventing the first calculating machine and pioneering probability theory.

What changes? What gets better? What gets worse?

---

*Tags: fluid-statics; pressure; buoyancy; Pascals-principle; Archimedes; density; depth*
