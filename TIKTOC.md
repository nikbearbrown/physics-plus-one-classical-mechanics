# TIKTOC.md — Physics +1, Classical Mechanics

## Physics +1 Series · Classical Mechanics

**Author:** Nik Bear Brown
**Series:** Physics +1
**Format:** $1 Kindle · Brutalist D3 + Claude Code
**Brutalist reference:** brutalist-d3-x-claude
**Series prototype:** quantum-mechanics-plus-one
**Source chapters:** _src_* files in chapters/ (college-physics-bundle-with-llms spine + physics-with-llms voice)

---

## Series contract (every chapter)

Every chapter contains, in order:

1. Mechanism deep-dive — the physics, done correctly
2. Exercises — at least one Apply-or-above; at least one produces an artifact
3. "What would change my mind"
4. "Still puzzling"
5. LLM Exercise — D3 + Claude Code simulation (PROJECT.md update → CLAUDE.md amendment → simulation prompt → exploration tasks)
6. AI Wayback Machine — one historical figure per chapter, never repeated, diversity tracked
7. Bridge to next chapter

---

## D3 simulation character: Confirmation

Classical mechanics simulations are confirmation tools. The student's physical intuition can verify the output — throw a ball, check the trajectory. Every simulation should be something the student can test against lived experience.

Known CLAUDE.md failure modes for mechanics simulations:

- Energy not conserved in collision simulators (use exact kinematics, not numerical integration)
- Drag force applied in wrong direction
- Angular momentum not conserved in rotation simulations
- Orbit simulators using linear instead of inverse-square gravity

---

## Chapter list

### Chapter 1 — What is Physics? / The Nature of Science

**Source:** _src_ college-physics ch1 + _src_ physics ch1
**D3 simulation:** Scale explorer — powers of ten, from Planck length to observable universe
**Core concepts:** Scientific method, measurement, units, significant figures, orders of magnitude
**Research focus:** Best "powers of ten" frameworks for intro physics; common misconceptions about what physics is vs. what engineering is; Attenborough-voice cold open ideas for "what is physics"

### Chapter 2 — Motion in One Dimension / Kinematics

**Source:** _src_ college-physics ch2 + _src_ physics ch2
**D3 simulation:** Position-velocity-acceleration live plotter — drag position curve, watch v and a derived in real time
**Core concepts:** Displacement, velocity, acceleration, kinematic equations, free fall
**Research focus:** Most common student errors in kinematics (sign conventions, average vs instantaneous velocity); best worked examples for free fall; CLAUDE.md failure modes for kinematic plotters

### Chapter 3 — Two-Dimensional Kinematics

**Source:** _src_ college-physics ch3
**D3 simulation:** Projectile trajectory simulator — vary launch angle and speed, watch range and max height, show optimal 45° result
**Core concepts:** Vector decomposition, projectile motion, independence of x and y motion
**Research focus:** Why students struggle with independence of components; best "surprising result" for projectile motion (45° optimal angle, same-height landing time); real cases where projectile intuition fails

### Chapter 4 — Forces and Newton's Laws

**Source:** _src_ college-physics ch4
**D3 simulation:** Free-body diagram builder + net force animator — add forces, watch acceleration
**Core concepts:** Force, mass, Newton's three laws, free-body diagrams
**Research focus:** Most persistent misconceptions about Newton's third law; best free-body diagram pedagogy; CLAUDE.md failure modes for force simulators (sign errors, forgetting normal force)

### Chapter 5 — Friction, Drag, and Elasticity

**Source:** _src_ college-physics ch5
**D3 simulation:** Terminal velocity race — vary mass and drag coefficient, watch objects reach terminal v at different rates
**Core concepts:** Static vs kinetic friction, drag forces, Hooke's law, elastic limit
**Research focus:** Why terminal velocity is counterintuitive; Stokes vs quadratic drag — which regime for intro physics; real cases where friction intuition fails (coefficient >1)

### Chapter 6 — Circular Motion and Gravitation

**Source:** _src_ college-physics ch6
**D3 simulation:** Orbit animator — tune mass and orbital speed, see stable orbit vs escape vs crash; show centripetal acceleration direction
**Core concepts:** Centripetal acceleration, centripetal force, Newton's law of gravitation, orbital mechanics
**Research focus:** Why "centrifugal force" is a persistent misconception and how to correct it; connection between circular motion and gravitation (Newton's cannon); CLAUDE.md failure modes for orbit simulators

### Chapter 7 — Work, Energy, and Energy Resources

**Source:** _src_ college-physics ch7
**D3 simulation:** Energy bar chart — track KE, PE, thermal energy through a roller coaster or collision; show conservation
**Core concepts:** Work, kinetic energy, potential energy, conservation of energy, power
**Research focus:** Most common errors in energy conservation problems (forgetting thermal energy); best "surprising" energy examples; real energy resource data for current examples

### Chapter 8 — Momentum and Collisions

**Source:** _src_ college-physics ch8 + _src_ physics ch8
**D3 simulation:** 1D collision simulator — elastic/inelastic toggle, vary masses and initial velocities, verify momentum and energy conservation
**Core concepts:** Momentum, impulse, conservation of momentum, elastic vs inelastic collisions
**Research focus:** Why elastic collisions conserve KE (not just momentum); real collision examples (air bags, crumple zones); CLAUDE.md failure mode: energy NOT conserved in inelastic (common LLM error)

### Chapter 9 — Statics and Torque

**Source:** _src_ college-physics ch9
**D3 simulation:** Torque balance — place weights at different positions on a beam, find equilibrium; show net torque
**Core concepts:** Torque, static equilibrium, center of mass, conditions for equilibrium
**Research focus:** Best "surprising" statics examples (why is the Eiffel Tower stable); common student errors in torque problems (wrong moment arm); real structural engineering applications

### Chapter 10 — Rotational Motion and Angular Momentum

**Source:** _src_ college-physics ch10
**D3 simulation:** Figure skater — pull in arms (decrease r), watch angular velocity increase; show L = Iω conservation
**Core concepts:** Angular velocity, angular acceleration, moment of inertia, angular momentum, conservation of angular momentum
**Research focus:** Why moment of inertia depends on mass distribution (not just mass); best "surprising" angular momentum examples (bicycle wheel gyroscope, spinning neutron stars); CLAUDE.md failure modes for rotation simulations

### Chapter 11 — Fluid Statics

**Source:** _src_ college-physics ch11
**D3 simulation:** Pressure depth explorer — vary fluid density and depth, show pressure; Archimedes — submerge object, show buoyant force vs weight
**Core concepts:** Pressure, Pascal's principle, Archimedes' principle, buoyancy
**Research focus:** Why objects float (buoyancy vs weight — not density alone); best surprising buoyancy examples (ships made of steel); Pascal's principle real applications (hydraulics)

### Chapter 12 — Fluid Dynamics

**Source:** _src_ college-physics ch12
**D3 simulation:** Bernoulli flow visualizer — narrow pipe section, show velocity increase and pressure decrease; continuity equation demonstrated
**Core concepts:** Continuity equation, Bernoulli's principle, viscosity, turbulence
**Research focus:** Why Bernoulli is commonly misapplied (airplane lift explanation controversy); best real applications; common LLM failure mode: confusing static and dynamic pressure

### Chapter 13 — Waves and Their Properties

**Source:** _src_ college-physics ch16 + _src_ physics ch13
**D3 simulation:** Wave interference — two point sources, vary frequency and separation, show constructive/destructive interference pattern
**Core concepts:** Wave properties, superposition, interference, standing waves, resonance
**Research focus:** Why interference is counterintuitive (two waves can cancel); best interference demonstrations; connection to Chapter 4 of Optics volume (double slit)

### Chapter 14 — Sound and Hearing

**Source:** _src_ college-physics ch17 + _src_ physics ch14
**D3 simulation:** Standing wave modes — tube open/closed ends, harmonic selector, show node and antinode positions
**Core concepts:** Sound as pressure wave, speed of sound, intensity, decibels, Doppler effect, standing waves in pipes
**Research focus:** Why Doppler effect is directional; best cold open for sound (bat echolocation, SONAR, medical ultrasound); connection to music and musical instruments
