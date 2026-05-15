# Chapter 9 — Work, Energy, and Energy Resources

**Suggested titles**

1. Work, Energy, and the Resources They Come From
2. The Currency of Physics
3. Why a Hill Counts the Same Whether You Climb It Steep or Shallow

**TL;DR.** Energy is the universal currency of physics. It comes in many forms (kinetic, gravitational potential, elastic, thermal, chemical, electromagnetic, nuclear), it converts continuously between them, but the *total* is always conserved. This chapter installs the bookkeeping: work is what transfers energy ($W = Fd\cos\theta$); kinetic energy is energy of motion ($KE = \tfrac{1}{2}mv^2$); potential energy is stored energy ($PE_g = mgh$ for gravity, $PE_s = \tfrac{1}{2}k x^2$ for springs); the work-energy theorem links them; and conservation of mechanical energy gives you a powerful shortcut for any problem where friction is small.

---

## A pumped-storage reservoir, off-peak hours

Forty miles outside any city, on a wooded hillside, sits an upper reservoir — a man-made lake with a concrete dam, half a kilometer above a lower lake at the foot of the hill. At 2:00 AM, when electricity demand on the local grid is low and electricity is cheap, large pumps lift water from the lower lake to the upper one. The pumps run for hours. By dawn, the upper reservoir is full.

At 5:00 PM, when demand peaks, valves open. Water flows back down through pipes into hydroelectric turbines and generates electricity that is sold back to the grid at peak prices. By midnight, the upper reservoir is empty again.

This is a pumped-storage hydroelectric plant. It is a battery — but instead of storing energy chemically, it stores energy *gravitationally*. Lifted water has more potential energy than water at the bottom; that potential energy is the "charge." When you let the water fall, the potential energy converts back to kinetic energy (water moving fast through pipes) and then to electrical energy (turbines spinning generators). The whole cycle is a translation between forms.

The roundtrip efficiency is about $75\%$. A quarter of the energy you pump up is lost — to friction in the pumps, drag in the pipes, heat in the generators, and a hundred smaller leaks. Conservation of energy doesn't say all the energy comes back as electricity. It says all the energy goes *somewhere* — and most of what doesn't come back as electricity ends up as low-grade heat in the surrounding rock and water, undetectable except over long times.

This chapter is about that translation: how work transfers energy from one form to another, why the total never changes, where energy goes when it "leaves," and how the human-scale economy of energy resources sits inside this physics. Pumped storage is one example — your body, your car, every electrical appliance, every star burning, is doing the same kind of bookkeeping.

**Learning objectives.** By the end of this chapter you should be able to:

1. Compute the work done by a constant force, including the case of force at an angle to displacement: $W = Fd\cos\theta$.
2. Apply the work-energy theorem $W_{\text{net}} = \Delta KE$ to compute changes in kinetic energy from net work, and vice versa.
3. Compute gravitational potential energy ($PE_g = mgh$) and elastic potential energy ($PE_s = \tfrac{1}{2}k x^2$) and use them in conservation-of-mechanical-energy problems.
4. Distinguish conservative from non-conservative forces, and apply the work-energy theorem with both: $KE_i + PE_i + W_{\text{nc}} = KE_f + PE_f$.
5. Compute power $P = W/t = Fv$ for any energy-conversion process and translate between watts, kilowatt-hours, and other practical units.

**Prerequisites.** Chapter 4 (Newton's laws). Chapter 5 (friction as a non-conservative force). Vector decomposition from Chapter 3 (force-and-displacement angles).

**Why this chapter matters.** Energy is the most general accounting tool in physics. Every later chapter — heat (Ch. 14), waves (Ch. 16), thermodynamics (Ch. 15), electricity (Ch. 21), nuclear (Ch. 31) — uses some form of energy conservation as its central organizing principle. This chapter installs the language and the ledger. It also connects physics to the practical economy: energy resources, efficiency, the cost of running a house, the metabolic cost of running a marathon.

---

## Concept 1 — Work and the work-energy theorem

### A briefcase up the stairs vs. across the room

A person carries a briefcase across a level office floor at constant velocity. From a physicist's perspective, how much work is done on the briefcase?

Zero.

The person feels tired (their muscles are doing work — but on themselves, against their own bones, not on the briefcase). The briefcase moves a distance. But the *force the person applies on the briefcase* (upward, supporting its weight) is *perpendicular* to the *displacement of the briefcase* (horizontal). Force perpendicular to motion does no work.

Now the same person carries the briefcase up a flight of stairs at constant velocity. Same forces, same speed. But this time, the upward force has a component aligned with the upward displacement — and the work done equals the briefcase's weight times the height climbed.

The everyday word "work" includes the level walk. The physics definition does not. This is a specification move worth making carefully.

### The mechanism — work as force times parallel displacement

For a constant force $\mathbf{F}$ acting on an object that moves through displacement $\mathbf{d}$:

$$W = F d \cos\theta,$$

where $\theta$ is the angle between $\mathbf{F}$ and $\mathbf{d}$.

Three cases worth keeping straight:

- $\theta = 0°$: force aligned with motion. $W = Fd$. (Push something forward; full work.)
- $\theta = 90°$: force perpendicular to motion. $W = 0$. (Carry something at constant height; no work.)
- $\theta = 180°$: force opposite to motion. $W = -Fd$. (Friction slowing a moving object; negative work.)

Negative work removes energy from the object. Positive work adds energy.

Units of work: $\text{N} \cdot \text{m} = \text{joule (J)}$.

### The work-energy theorem

The **net** work done on an object — sum of work by every force acting on it — equals the change in its kinetic energy:

$$W_{\text{net}} = \Delta KE = \tfrac{1}{2} m v_f^2 - \tfrac{1}{2} m v_i^2.$$

This is one of the deepest results in mechanics. It links a force-times-distance quantity (work) to a velocity-squared quantity (kinetic energy). The derivation is short — apply $F = ma$, multiply both sides by $d$, use the kinematic equation $v_f^2 = v_i^2 + 2ad$ — and the result is universal: any time net work is done on an object, its kinetic energy changes by exactly that much.

Kinetic energy itself: $KE = \tfrac{1}{2} m v^2$. Units: joules. A $1 \text{ kg}$ object moving at $1 \text{ m/s}$ has $0.5 \text{ J}$ of kinetic energy. A car of $1{,}500 \text{ kg}$ at $30 \text{ m/s}$ has $675{,}000 \text{ J}$.

### The trade-off

The work-energy framework trades **vector calculus for scalar bookkeeping.** Newton's laws are vector equations: you have to keep track of directions. The work-energy theorem is scalar: just add up the work, get the kinetic energy change. The cost is that you don't know in what *direction* the kinetic energy went — only the magnitude. The benefit is that for many problems (especially those involving work over a path), the scalar accounting is much simpler.

### Worked example — pushing a stalled car

You push a $1{,}500 \text{ kg}$ stalled car along a level road. You apply a horizontal force of $400 \text{ N}$ for a distance of $20 \text{ m}$. Friction opposes the motion at $200 \text{ N}$. (a) How much work does each force do? (b) What is the car's final speed if it started from rest?

**Work by your push.** $W_{\text{push}} = (400)(20)\cos 0° = 8000 \text{ J}$.

**Work by friction.** $W_{\text{fric}} = (200)(20)\cos 180° = -4000 \text{ J}$.

**Work by gravity and normal force.** Both perpendicular to motion: $0$.

**Net work.** $W_{\text{net}} = 8000 - 4000 = 4000 \text{ J}$.

**Apply work-energy theorem.** $W_{\text{net}} = \tfrac{1}{2} m v_f^2 - 0$:

$$4000 = \tfrac{1}{2}(1500) v_f^2 \implies v_f^2 = \frac{8000}{1500} \approx 5.33 \text{ m}^2/\text{s}^2 \implies v_f \approx 2.31 \text{ m/s}.$$

The car ends up moving at about $2.3 \text{ m/s}$.

**Sanity check.** Using $F = ma$ from Chapter 4: net force $= 200 \text{ N}$, $a = 200/1500 \approx 0.133 \text{ m/s}^2$. Using $v^2 = v_0^2 + 2ad$: $v^2 = 0 + 2(0.133)(20) = 5.33$, $v = 2.31 \text{ m/s}$. Same answer. The work-energy theorem is consistent with Newton's laws, as it must be.

### Common misconceptions

- *"If you exert force, you do work."* Only if the object moves *and* the force has a component along that motion. Holding a $20 \text{ kg}$ weight steady above your head does *no* work (the displacement is zero), even though it feels exhausting.
- *"Negative work means the force is negative."* Negative work means the force has a component *opposite* to the displacement. Friction always does negative work on a moving object (if friction is the only force in question). The force itself isn't "negative" — it's a positive-magnitude force pointing the wrong way.

↳ **Dig Deeper — Work done by a variable force**

*The work formula $W = Fd\cos\theta$ assumes the force is constant over the displacement. For a variable force (a spring, gravity at varying altitude, a person whose pushing force changes), the work is the integral $W = \int F \cdot dx$, which corresponds to the area under the force-vs-position graph.*

**Prompt:**
> Explain how to compute work done by a variable force using the integral $W = \int F(x) dx$, and interpret it as the area under the $F$-vs-$x$ curve. Compute the work to stretch a spring (with spring constant $k$) from its natural length to a stretch of $\Delta L$ — show that this gives $W = \tfrac{1}{2} k (\Delta L)^2$, the elastic potential energy. End with one sentence on how this generalizes to non-constant forces in 3D.

**What to do with the output:** Save it. The integral form of work is the bridge to elastic potential energy and to all later energy calculations involving non-constant forces.

---

## Concept 2 — Potential energy and conservation of mechanical energy

### A roller coaster at the top of the first hill

A roller coaster car sits at the top of the first big hill. Its speed is essentially zero — the chain has just released it at the crest. Below, the track drops $40 \text{ m}$ to the bottom of the first valley, where the speed of the car will be at its maximum.

How fast will it be going at the bottom?

You could solve this with kinematics if you knew the slope at every point and the friction coefficient. It would be tedious. Or you could use energy conservation: at the top, the car has gravitational potential energy and zero kinetic energy. At the bottom, it has zero potential energy (relative to the bottom) and maximum kinetic energy. Ignoring friction, those two are equal:

$$mgh = \tfrac{1}{2} m v^2 \implies v = \sqrt{2gh} = \sqrt{2(9.8)(40)} \approx 28 \text{ m/s}.$$

About $100 \text{ km/h}$ — the kind of thrill speed real roller coasters reach. One line of algebra. No need to know the shape of the track.

This is the power of conservation of mechanical energy: when forces are conservative, the total mechanical energy (KE + PE) of a system stays constant, and you can compute final speeds from heights without integrating along the path.

### The mechanism — potential energy and conservative forces

A **conservative force** is one whose work depends only on the start and end points of a path, not on the path taken. Gravity is conservative. Spring forces are conservative. The electric force from a fixed charge is conservative. Friction is *not* — it depends on the path length.

For a conservative force, you can define a **potential energy** $PE$ such that the work done by the force equals the *negative* change in $PE$:

$$W_{\text{conservative}} = -\Delta PE.$$

For gravity near Earth's surface (taking up as positive):

$$PE_g = mgh,$$

where $h$ is height above some chosen reference level. The reference is arbitrary; only *changes* in $PE_g$ are physically meaningful.

For a spring obeying Hooke's law:

$$PE_s = \tfrac{1}{2} k x^2,$$

where $x$ is displacement from the spring's natural length.

**Conservation of mechanical energy.** If only conservative forces act (no friction, no external pushes), then the total mechanical energy is constant:

$$KE_i + PE_i = KE_f + PE_f.$$

This is the workhorse equation of energy-conservation problems.

If non-conservative forces (like friction) are also present, the work they do appears as an additional term:

$$KE_i + PE_i + W_{\text{nc}} = KE_f + PE_f.$$

Friction's $W_{\text{nc}}$ is negative (friction removes mechanical energy — converts it to heat, which is a different kind of energy not yet in our ledger).

### The trade-off

The potential-energy framework trades **a slightly abstract concept (stored energy) for an enormous calculational simplification.** PE is not a physical thing you can point to. It's a bookkeeping device that makes conservation of energy work cleanly. The cost is conceptual; the benefit is that you can solve problems involving conservative forces without ever computing trajectories — just compare states at start and end.

### Worked example — a pendulum at the bottom

A pendulum bob of mass $0.50 \text{ kg}$ is held to one side at a height $0.20 \text{ m}$ above its lowest point and released from rest. Ignoring air resistance, what is its speed at the lowest point?

**Choose a reference.** Let $h = 0$ at the bob's lowest point.

**Initial state.** $h_i = 0.20 \text{ m}$, $v_i = 0$. So $PE_i = mgh_i = (0.50)(9.80)(0.20) = 0.98 \text{ J}$. $KE_i = 0$.

**Final state.** $h_f = 0$, $v_f = ?$. $PE_f = 0$, $KE_f = \tfrac{1}{2} m v_f^2$.

**Conservation.** $0.98 + 0 = 0 + \tfrac{1}{2}(0.50) v_f^2$.

$$v_f^2 = \frac{2 \times 0.98}{0.50} = 3.92 \text{ m}^2/\text{s}^2 \implies v_f = 1.98 \text{ m/s}.$$

About $2.0 \text{ m/s}$ at the bottom.

**Sanity check.** $v = \sqrt{2gh} = \sqrt{2 \times 9.8 \times 0.2} = \sqrt{3.92} = 1.98 \text{ m/s}$ ✓. The mass cancels — the pendulum's bob speed at the bottom depends only on the height it fell from, not on its mass. This is why a heavier pendulum bob and a lighter one with the same string length have the same period.

### Common misconceptions

- *"Higher up means more potential energy, period."* Higher up *relative to your chosen reference* means more PE. The reference level is arbitrary; what matters physically is *changes* in PE.
- *"Energy conservation is exact, so you can ignore friction."* Mechanical energy conservation requires conservative forces only. With friction, mechanical energy decreases (some converts to heat), and you must include the work done by friction explicitly. *Total* energy is still conserved — it just requires expanding the ledger.
- *"Potential energy belongs to the object."* Strictly, $PE_g$ belongs to the object-Earth *system*, not the object alone. (You can't have gravitational PE without two interacting masses.) The single-object phrasing is a useful shorthand.

↳ **Dig Deeper — Why isn't friction conservative?**

*Friction depends on the path length, not just the start and end points. Two paths between the same points but with different lengths produce different amounts of friction work. This is what makes friction non-conservative — and explains why mechanical energy is "lost" when friction is present (it's actually transformed to thermal energy in the surfaces).*

**Prompt:**
> Explain why friction is a non-conservative force, with a specific worked example: comparing the friction work for a block sliding directly across a $5 \text{ m}$ table versus a block sliding $5 \text{ m}$ across the table along a zigzag path of total length $10 \text{ m}$ (same start and end points). Show that friction work differs in the two cases. Then explain where the "lost" mechanical energy goes — what physical process turns it into thermal energy. End with one sentence on whether energy conservation is violated by friction (it isn't — the total energy is conserved if you include the thermal energy).

**What to do with the output:** Save it. The conservative/non-conservative distinction is the bridge to the broader concept of total energy conservation, including thermal forms.

---

## Concept 3 — Power, efficiency, and the human/economic scale of energy

### A 100-watt light bulb left on overnight

You leave a $100 \text{ W}$ incandescent light bulb on for $10$ hours overnight. How much energy did it use? At U.S. retail electricity prices (call it $\$0.15$ per kWh), how much did it cost?

Energy used: $100 \text{ W} \times 10 \text{ h} = 1{,}000 \text{ Wh} = 1.0 \text{ kWh}$.

Cost: $1.0 \text{ kWh} \times \$0.15/\text{kWh} = \$0.15$.

A dollar fifty over ten nights. Manageable. Multiply by every house in the country leaving a few bulbs on per night, and you get the kind of demand on the grid that determines whether power plants operate at peak or trough — which is exactly why pumped-storage hydroelectric plants exist.

This worked example brings us to the practical scale of energy. Power and efficiency are how we connect the joule (a tiny unit, hard to feel) to the everyday economics of running the world.

### The mechanism — power

**Power** is the rate at which energy is transferred or work is done:

$$P = \frac{W}{t} \quad \text{or} \quad P = \frac{\Delta E}{\Delta t}.$$

Units: $\text{joule/second} = \text{watt (W)}$.

For a force $\mathbf{F}$ moving an object at velocity $\mathbf{v}$:

$$P = \mathbf{F} \cdot \mathbf{v} = F v \cos\theta.$$

Some power scales worth feeling:

- A human at rest: $\sim 100 \text{ W}$ (most of it heat from metabolism).
- Walking briskly: $\sim 200$–$300 \text{ W}$.
- A serious athlete sprinting: $\sim 1{,}000$–$2{,}000 \text{ W}$ (briefly).
- A horse working: $\sim 750 \text{ W}$ (the historical definition of one horsepower).
- A small car cruising on highway: $\sim 30{,}000 \text{ W}$ (40 hp).
- A locomotive: $\sim 4 \text{ MW} = 4 \times 10^6 \text{ W}$.
- A nuclear reactor: $\sim 1{,}000 \text{ MW} = 10^9 \text{ W}$.

**Efficiency** is the ratio of useful output energy to total input energy:

$$\eta = \frac{E_{\text{useful}}}{E_{\text{input}}}.$$

A car engine: $\sim 25\%$ (the rest is waste heat). A coal-fired power plant: $\sim 35\%$. A modern LED light: $\sim 40\%$ light, $60\%$ heat. An incandescent bulb: $\sim 5\%$ light, $95\%$ heat.

Efficiencies are limited not just by engineering but by thermodynamic laws (which we'll meet in Chapter 15). For now: every conversion costs some energy to entropy and heat. The total is conserved, but the *useful* fraction shrinks at every step.

### The trade-off

The power-and-efficiency framework trades **a single accounting (energy total)** for **a process-aware accounting (rates and conversions).** Energy alone doesn't tell you whether a process is fast or slow, useful or wasteful. Power tells you the rate; efficiency tells you the loss. Both are needed to engineer real systems.

### Worked example — the human-body energy budget

A person consumes $2{,}500 \text{ kcal}$ in food per day. (a) How many joules is that? (b) What is the average power produced if all of it is used over the $86{,}400$ seconds of a day?

**Conversion.** $1 \text{ kcal} = 4{,}184 \text{ J}$. So:

$$E = 2500 \times 4184 \approx 1.05 \times 10^7 \text{ J} = 10.5 \text{ MJ}.$$

**Average power.**

$$P = \frac{E}{t} = \frac{1.05 \times 10^7}{86{,}400} \approx 121 \text{ W}.$$

About $120 \text{ W}$ on average — close to the resting metabolic rate of $\sim 100 \text{ W}$ plus the active-metabolic power of light activity throughout the day.

**Sanity check.** A typical 100 W light bulb runs at the same power as a sedentary human. A vigorously exercising person ($500$–$1000 \text{ W}$) is putting out the equivalent of $5$–$10$ light bulbs of metabolic heat — which is why exercise rooms get warm fast and why marathon runners need massive cooling.

### Common misconceptions

- *"Power and energy are the same thing."* Power is energy per unit time. A $100 \text{ W}$ light bulb on for $10$ hours uses the same energy ($1 \text{ kWh}$) as a $1{,}000 \text{ W}$ heater on for $1$ hour.
- *"Efficiency over $100\%$ is possible if you're clever enough."* No. The first law of thermodynamics (energy conservation) caps it at $100\%$. The second law usually drops it much lower.
- *"Renewable energy is free."* The energy itself is free, but the infrastructure to capture it (solar panels, wind turbines, hydroelectric dams) has finite efficiency, finite lifespan, and finite cost. The relevant question is always: efficiency at what stage, over what lifecycle.

↳ **Dig Deeper — Energy resources and the global picture**

*The world used roughly $6 \times 10^{20} \text{ J}$ of primary energy in 2024 (about $19 \text{ TW}$ continuous power). Of that, roughly $80\%$ comes from fossil fuels (coal, oil, natural gas), with the rest from nuclear, hydro, wind, solar, and biomass. The numbers, the mix, and the trends are decisive for both economics and climate policy.*

**Prompt:**
> Walk me through the global energy budget for the most recent year you have data on. Break it down by source (oil, coal, natural gas, nuclear, hydro, wind, solar, biomass) in both percentage and absolute terms (TW or EJ/year). Then explain (a) which sources have grown fastest in the past decade, (b) which have shrunk, (c) what the scale comparison is between human energy use and incoming solar power on Earth's surface (a useful order-of-magnitude check). End with one sentence on what scaling factor renewable sources would need to cover all of human demand.

**What to do with the output:** Save it. Energy resources are the topic of OpenStax's section 7.10 in this chapter; the Dig Deeper substitutes for the body coverage and connects to up-to-date data the textbook can't easily maintain.

---

## Synthesis — energy as universal currency

Step back. Three concepts.

**Work** ($W = Fd\cos\theta$) transfers energy between systems. The work-energy theorem links net work to kinetic-energy change.

**Potential energy** stores energy in configurations: gravitational ($mgh$), elastic ($\tfrac{1}{2} k x^2$), and others. Conservation of mechanical energy lets you compute speed from height (or vice versa) without solving the equations of motion along the path.

**Power** is the rate of energy transfer; **efficiency** is the fraction that ends up useful. These are the practical-economy quantities that connect physics to engineering and policy.

The **scale shift** I want you to feel: the same conservation principle covers a $0.5 \text{ kg}$ pendulum bob swinging through $20 \text{ cm}$ ($\Delta E \sim 1 \text{ J}$), a roller coaster falling $40 \text{ m}$ ($\Delta E \sim 10^5 \text{ J}$), a pumped-storage reservoir ($\Delta E \sim 10^{12}$–$10^{13} \text{ J}$), and the kinetic energy of the Earth orbiting the Sun ($\sim 10^{33} \text{ J}$). The framework — KE, PE, conservation — applies across $33$ orders of magnitude. The arithmetic is the same; only the prefactors change.

### A worked example using all three concepts — a pumped-storage cycle

A pumped-storage reservoir holds $1.0 \times 10^9 \text{ kg}$ of water (about a million tons) at an average height of $400 \text{ m}$ above the lower reservoir. (a) What is the total gravitational potential energy stored? (b) If this is released over $4$ hours through turbines with $90\%$ efficiency, what is the average electrical power output? (c) If the pumps that lifted the water operated at $85\%$ efficiency, how much grid electricity did it take to fill the reservoir?

**Concept 2 — potential energy stored.**

$$PE = mgh = (1.0 \times 10^9)(9.80)(400) = 3.92 \times 10^{12} \text{ J} = 3.92 \text{ TJ}.$$

In kilowatt-hours: $3.92 \times 10^{12} / (3.6 \times 10^6) \approx 1.09 \times 10^6 \text{ kWh}$. About a million kWh — enough to power roughly $30{,}000$ U.S. homes for a day.

**Concept 1 + Concept 3 — power output.** The turbines are $90\%$ efficient:

$$E_{\text{electrical}} = 0.90 \times 3.92 \text{ TJ} = 3.53 \text{ TJ}.$$

Released over $4$ hours $= 14{,}400 \text{ s}$:

$$P_{\text{out}} = \frac{3.53 \times 10^{12}}{14{,}400} \approx 2.45 \times 10^8 \text{ W} = 245 \text{ MW}.$$

About $245 \text{ MW}$ — typical for a mid-size pumped-storage plant.

**Concept 3 — input energy.** The pumps are $85\%$ efficient (electrical to potential):

$$E_{\text{input}} = \frac{PE}{0.85} = \frac{3.92}{0.85} \approx 4.61 \text{ TJ}.$$

So the cycle: $4.61 \text{ TJ}$ of grid electricity in → $3.53 \text{ TJ}$ of grid electricity out. Roundtrip efficiency: $3.53 / 4.61 = 0.766$, or about $77\%$. The remaining $23\%$ is lost as heat in pumps, friction in pipes, electrical losses in motors and generators, and turbulence in the water column.

This is the bookkeeping of an industrial-scale energy economy. The same equations that gave us a roller-coaster speed gave us a multimillion-dollar electrical output. The framework scales.

---

## Exercises

### Warm-up

**7.1** *(LO 1)* You push a $20 \text{ kg}$ box across a frictionless floor with $50 \text{ N}$ for $4.0 \text{ m}$. (a) How much work do you do? (b) What is the box's final kinetic energy if it started from rest? (c) What is its final speed?

**7.2** *(LO 1)* You carry a $5 \text{ kg}$ bag of groceries at constant velocity for $20 \text{ m}$ across a level parking lot. How much work do you do on the bag?

**7.3** *(LO 3)* A $0.5 \text{ kg}$ rock is held $3.0 \text{ m}$ above the ground. (a) What is its gravitational PE (relative to the ground)? (b) If dropped, what is its speed just before hitting the ground (ignore air drag)?

**7.4** *(LO 5)* A $1{,}500 \text{ W}$ hair dryer runs for $10$ minutes. (a) How much energy in joules? (b) In kWh? (c) At $\$0.15$/kWh, what does it cost?

### Application

**7.5** *(LO 2, 3)* A $60 \text{ kg}$ skier starts from rest at the top of a slope $30 \text{ m}$ above the bottom. Ignoring friction, what is her speed at the bottom?

**7.6** *(LO 2, 3, 4)* A $1{,}200 \text{ kg}$ car traveling at $20 \text{ m/s}$ skids to a stop on a level road. The kinetic friction coefficient is $\mu_k = 0.6$. (a) Compute the initial KE. (b) Use the work-energy theorem to find the stopping distance.

**7.7** *(LO 3)* A spring with $k = 200 \text{ N/m}$ is compressed by $0.10 \text{ m}$. (a) What is the elastic PE stored? (b) If released and pushing a $0.20 \text{ kg}$ ball, what is the ball's launch speed?

**7.8** *(LO 5)* A car climbs a $5\%$ grade ($\sin\theta \approx 0.05$) at a constant $20 \text{ m/s}$. Mass is $1{,}500 \text{ kg}$. (a) What is the rate at which the engine does work against gravity (ignoring friction and drag)? (b) What is this in horsepower ($1 \text{ hp} = 746 \text{ W}$)?

### Synthesis

**7.9** *(LO 2, 3, 4)* A roller coaster car of mass $400 \text{ kg}$ starts from rest at the top of the first hill ($h = 50 \text{ m}$) and reaches the bottom at $25 \text{ m/s}$. (a) Compute the final KE. (b) Compute the initial PE. (c) How much mechanical energy was lost to friction? (d) Where did that energy go?

**7.10** *(LO 3, 5)* You climb a $20 \text{ m}$ flight of stairs in $30 \text{ s}$. Your mass is $70 \text{ kg}$. (a) How much work do you do against gravity? (b) What is your average mechanical power output? (c) At what efficiency (food calories to mechanical work) does the human body operate? Look up a typical value.

**7.11** *(LO 1, 2, 3)* A $0.5 \text{ kg}$ ball is thrown straight up at $15 \text{ m/s}$ from ground level. Using energy conservation, find: (a) the maximum height, (b) the speed when the ball is half that height, (c) the speed when it returns to ground level.

### Challenge

**7.12** *(beyond chapter)* A pumped-storage plant lifts $3 \times 10^9 \text{ kg}$ of water through $250 \text{ m}$ of elevation. (a) Total gravitational PE stored? (b) If pumped over $8$ hours at $80\%$ efficiency, what input power is required? (c) If discharged over $4$ hours at $90\%$ efficiency, what output power is delivered? (d) What roundtrip efficiency does this plant achieve?

**7.13** *(beyond chapter)* Estimate the kinetic energy of (a) a $5 \text{ g}$ bullet at $400 \text{ m/s}$; (b) a $1{,}500 \text{ kg}$ car at $30 \text{ m/s}$; (c) the Earth orbiting the Sun (mass $6 \times 10^{24} \text{ kg}$, orbital speed $30{,}000 \text{ m/s}$). Compare them in orders of magnitude.

---

## LLM Exercise — Chapter 7: Energy Bookkeeping for Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** An energy budget for one cycle of your anchor phenomenon, with input, useful output, and dissipated forms identified.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste 1-sentence description].

For Chapter 7, I want to build an energy budget for one cycle or one event of my phenomenon. Please:

1. Identify ONE complete energy cycle or event in my phenomenon. Examples:
   - Bike commute: one full ride from home to work — chemical (food) → mechanical (legs) → kinetic (bike) → friction/drag (heat).
   - Coffee maker: one brew cycle — electrical → thermal (heating water) → kinetic (water through grounds) → thermal (final coffee).
   - Basketball shot: chemical (muscles) → kinetic (ball) → gravitational PE (peak of arc) → kinetic (descent) → thermal (rim/net friction).
   - Marathon: 4-hour race — chemical (food + reserves) → mechanical (forward motion) → thermal (heat dissipated by sweating, drag, ground friction).
   - Espresso: electrical (pump) → mechanical (pressure) → kinetic (water flow) → thermal (final extracted shot).

2. Estimate the input energy (in joules or kWh).

3. Estimate the useful output (the energy that did the thing you wanted: forward motion, heated coffee, brewed shot).

4. Estimate the dissipated energy (where it went — friction, drag, heat to surroundings).

5. Compute the efficiency (useful / input).

6. Apply conservation of energy as a check: do all the pieces add up to the input?

7. One sentence on how this connects to Chapter 8 (momentum) — energy conservation gives you speeds; momentum conservation gives you what gets transferred in collisions.

Save the output as logbook/chapter-07-energy.md.
```

### What this produces

A seventh Logbook entry: an energy budget for your phenomenon, often illuminating which parts are inefficient and which are not.

### How to adapt this prompt

- *For phenomena with mostly heat output* (a coffee maker, a hair dryer): efficiency is mostly the question of "what fraction of electrical input ends up doing the intended thing vs. heating the surroundings."
- *For ChatGPT or Gemini:* identical with interface substitutions.
- *For Claude Code:* if you have power data (a smart-meter reading, an electricity bill), paste it; let Claude compute energy and efficiency directly.

### Connection to previous chapters

Builds directly on Chapter 4 (force). Energy is what work *transfers* — and work is force times displacement. Friction (Chapter 5) is the principal source of mechanical-to-thermal conversion. Chapter 6's circular motion is interesting here: at constant speed, gravity does no net work on a satellite.

### Preview of next chapter

Chapter 8 introduces momentum, the other great conservation law of mechanics. While energy conservation gives you final speeds, momentum conservation is what governs collisions — what shares with what when two objects hit each other.

---

## Chapter summary

Three layers of one idea: work, energy, and power. **Work** ($W = Fd\cos\theta$) transfers energy. The **work-energy theorem** ($W_{\text{net}} = \Delta KE$) links net work to kinetic-energy change. **Potential energy** ($PE_g = mgh$, $PE_s = \tfrac{1}{2}k x^2$) stores energy in configurations. **Conservation of mechanical energy** ($KE + PE = $ const, when only conservative forces act) is the most powerful shortcut in introductory mechanics. **Power** ($P = W/t = Fv$) is the rate at which energy is transferred. **Efficiency** is the fraction that ends up useful.

The one idea that matters most: **energy is conserved, period.** It changes form continuously (kinetic to potential, mechanical to thermal, chemical to electrical), but the total never changes. This is the deepest principle in physics — deeper than Newton's laws, in some sense, because it survives both quantum mechanics and relativity intact.

The common mistake to watch for: **forgetting that mechanical energy alone is not always conserved.** With friction or other non-conservative forces present, mechanical energy decreases. Total energy (including thermal) is still conserved — but you have to account for the heat that friction generates explicitly.

What you should now be able to teach someone else: how to compute work, kinetic energy, and gravitational potential energy; how to apply conservation of mechanical energy as a shortcut for problems that would be hard with kinematics; how to compute power and efficiency for real systems; and how the universal conservation of energy sits underneath all of this. Five skills, one organizing principle.

---

## What would change my mind

The chapter argues that conservation of energy is universal and exact across all classical (and quantum) physics. The argument would need revision if a careful experimental test ever found energy appearing or disappearing without conversion to a known form — historically, every such "violation" has been resolved by discovering a new form of energy that was previously unaccounted for (the neutrino was hypothesized in 1930 to save energy conservation in beta decay; it was experimentally detected in 1956). I expect the pattern to continue.

## Still puzzling

The deepest puzzle this chapter raises and does not resolve: **what is energy, really?** We can compute it, conserve it, transform it, sell it. But asking "what is the substance of energy?" is like asking "what is the substance of momentum?" — there isn't one, in any conventional sense. Energy is a number we can compute about a system that has the property of being conserved through time. Feynman, in his lectures, said: "It is important to realize that in physics today, we have no knowledge of what energy *is*." The conservation law works whether or not you understand what's conserved.

---

## Connections forward

Chapter 8 (linear momentum) presents the *other* great conservation law, governing collisions and rocket-like systems. Together with energy conservation, it forms the bedrock of classical mechanics. Chapter 9 (statics) treats the special case where mechanical energy is constant because nothing moves. Chapter 10 (rotation) generalizes work and kinetic energy to rotating bodies (rotational $KE = \tfrac{1}{2} I \omega^2$). Chapters 14–15 (heat, thermodynamics) extend energy conservation to thermal forms — and introduce the second law, which says that while *total* energy is conserved, the *useful* fraction always decreases in any real process. Chapter 21 (electricity) introduces electrical energy and power, central to modern engineering and the global energy economy.

---

**Tags:** energy, work, power, conservation, potential-energy

---

## AI Wayback Machine

**James Prescott Joule** demonstrated in 1843 that mechanical work can be converted to heat at a fixed ratio — the mechanical equivalent of heat. The result killed the caloric theory of heat and unified energy as a single quantity that flows between forms.

**Run this:**

```
Who was James Prescott Joule, and how does the mechanical equivalent of heat connect to the work and energy we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"James Prescott Joule"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Joule's paddle-wheel experiment in detail — what was measured, how was it converted?
- Ask it about Joule's role as a brewer's son and how that work shaped his physics.

What changes? What gets better? What gets worse?
