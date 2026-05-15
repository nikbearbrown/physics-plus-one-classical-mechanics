# Chapter 18 — Oscillatory Motion and Waves

**Suggested titles**

1. Oscillatory Motion and Waves
2. The Same Equation that Runs a Pendulum, a Guitar String, and a Quartz Watch
3. Hooke, Galileo, and the Mathematics of Going Back and Forth

**TL;DR.** A surprising fraction of physics is just one equation: $F = -kx$, the linear restoring force, applied to whatever happens to be displaced. From springs to pendulums to atoms in a crystal lattice to the air in front of a speaker, the same differential equation produces sinusoidal motion at a single characteristic frequency. This chapter installs that equation, computes the frequency for the canonical cases, extends to waves traveling in space, and ends at resonance — the trick that lets a small periodic push lift a child to the top of a swing or shatter a wineglass.

---

## A Connecticut quartz factory, 32,768 vibrations per second

Inside a Seiko quartz wristwatch sits a small fork-shaped sliver of crystalline silicon dioxide, machined to about 5 mm long, lacquered, and sealed in vacuum. A tiny voltage from the watch battery sets the fork vibrating. The crystal is cut so its natural mechanical resonance is exactly $2^{15} = 32{,}768$ Hz — chosen because dividing by 2 fifteen times gives 1 Hz, which the watch's circuitry uses to advance the seconds hand.

The accuracy is stunning. A good quartz watch keeps time to about 15 seconds per month — about one part in $10^5$. The mechanism is older than electronics. It is the same mechanism that lets a child on a swing time their kicks: a small periodic push at the system's natural frequency builds amplitude. Take the push away and the system rings down, slowly, at exactly the same frequency it was designed to ring at.

That single fact — *every restoring system has a natural frequency, and pushing it at that frequency builds large response* — is the lever this chapter pulls. Pulled correctly, it predicts how a mass on a spring bounces, how a pendulum ticks, how a guitar sings, how a microwave heats food, and why the Tacoma Narrows Bridge collapsed in 1940. One equation, lots of consequences.

**Learning objectives.** By the end of this chapter you should be able to:

1. State Hooke's law $F = -kx$ and identify the restoring-force structure in a real system.
2. Compute the period and frequency of a mass-spring oscillator: $T = 2\pi\sqrt{m/k}$, $f = 1/T$.
3. Compute the period of a simple pendulum: $T = 2\pi\sqrt{L/g}$, valid for small angles.
4. Apply energy conservation to a simple harmonic oscillator and compute maximum velocity.
5. Distinguish underdamped, critically damped, and overdamped oscillation and identify each in a real system.
6. Compute the wavelength, frequency, and speed of a wave: $v = f\lambda$.
7. Identify resonance and predict where it will appear in a periodically driven system.

**Prerequisites.** Chapter 4 (Newton's laws), Chapter 5 (Hooke's law as a special case of elastic deformation), Chapter 7 (work and energy), Chapter 10 (rotational kinematics, optional but useful for circular-motion analogy).

**Why this chapter matters.** Periodic phenomena are everywhere: the heart's beat, the tides, AC electricity, light, sound, atomic vibrations in matter. The mathematics is the same — simple harmonic motion — and once you have it, you have a master key for the rest of physics.

---

## Concept 1 — Hooke's law and the simple harmonic oscillator

### Robert Hooke, 1660, and the watch spring

In 1660, Robert Hooke — secretary to the Royal Society, future rival of Isaac Newton, polymath, and the man who first looked at cork through a microscope and named the cells he saw — was working out the mathematics of springs. He needed it for the watches he was helping build. The pocket watch was, in 1660, a brand-new instrument, and the question was: how do you make a small spring keep time?

Hooke noticed that for small displacements, the force exerted by a spring is proportional to the amount you stretch or compress it:

$$F = -kx,$$

where $k$ is the spring constant (units: N/m) and the negative sign means the force always points back toward the equilibrium position. He published the result, characteristically, as a Latin anagram — *ceiiinosssttuv* — to claim priority without sharing the result. Two years later he revealed the unscrambling: *ut tensio, sic vis*, "as the extension, so the force." Hooke's law.

The reason this matters far beyond springs is that *almost any restoring force, near equilibrium, looks like Hooke's law*. Pull an atom slightly from its lattice site; expand it back. Tilt a pendulum slightly off vertical; it returns. Compress the air in front of a speaker; the air pushes back. Each of these systems, for small displacements, has $F \approx -kx$ for some effective $k$. That is not coincidence. It is the mathematical fact that a smooth function near its minimum looks like a parabola, and the gradient of a parabola is a linear restoring force. Taylor's theorem, with the constant chosen to vanish at equilibrium and the linear term chosen to be zero at the minimum, leaves a quadratic potential — and hence a linear force.

So Hooke's law for a spring is one of the most over-engineered laws in physics: it reads as a special claim about springs, but it is a general fact about any system near equilibrium.

### The mechanism — period, frequency, and the SHO equation

A mass $m$ on a spring with constant $k$, displaced by $x$, experiences force $F = -kx$. By Newton's second law, $m \ddot{x} = -kx$, or

$$\ddot{x} + \frac{k}{m} x = 0.$$

This is a differential equation. Its solution, for any initial displacement $x_0$ and zero initial velocity, is

$$x(t) = x_0 \cos(\omega t),$$

where

$$\omega = \sqrt{\frac{k}{m}}$$

is the **angular frequency** in radians per second. The period — time for one complete oscillation — is

$$T = \frac{2\pi}{\omega} = 2\pi \sqrt{\frac{m}{k}},$$

and the frequency in oscillations per second is

$$f = \frac{1}{T} = \frac{1}{2\pi}\sqrt{\frac{k}{m}}.$$

Three things to notice. First, the period depends on $m$ and $k$ but *not* on the amplitude $x_0$. A spring oscillates at the same frequency whether you pull it 1 cm or 5 cm. This is the property that makes pendulums good clocks (Galileo's discovery, 1583, watching a chandelier in Pisa Cathedral). Second, heavier masses oscillate slowly, stiffer springs oscillate fast — both intuitive. Third, the formula gives a definite, calculable number; you can predict the period before the experiment.

### The trade-off

The simple harmonic approximation trades **range of validity for tractability.** Hooke's law is exact only for infinitesimal displacements. Stretch a real spring far enough and it becomes nonlinear (harder to pull), then plastic (it doesn't return), then it breaks. The approximation is excellent for small motions and progressively worse as amplitude grows. The trade is worth it: you get a closed-form solution and a clear physical picture in exchange for working only in the small-amplitude regime.

### Worked example — frequency of a piano string

A piano's middle C string has tension $T = 700 \text{ N}$, length $L = 65 \text{ cm}$, and mass per unit length $\mu = 4.0 \times 10^{-3}$ kg/m. The lowest mode (fundamental) of a string fixed at both ends has frequency

$$f_1 = \frac{1}{2L}\sqrt{\frac{T}{\mu}}.$$

Plugging in:

$$f_1 = \frac{1}{2 \times 0.65}\sqrt{\frac{700}{0.004}} = \frac{1}{1.30} \sqrt{175{,}000} = \frac{418.3}{1.30} \approx 322 \text{ Hz}.$$

Middle C is 261.6 Hz; my back-of-envelope numbers are a bit off (real piano middle C wouldn't have those exact specs), but the right order of magnitude. The string vibrates as a one-dimensional simple harmonic system, with effective $k$ set by tension and effective $m$ set by linear density.

**Sanity check.** Strings on a guitar (much shorter, lower tension) play higher notes; bass strings (longer, much heavier per length, similar tension) play lower notes. The formula gets the qualitative direction right, which is the first thing to verify.

### Common misconceptions

- *"Period depends on amplitude."* For a true SHO, no. For real systems with nonlinear restoring forces, slightly yes — but the change is small for moderate amplitudes.
- *"Hooke's law is just about springs."* No — it's about any restoring force near equilibrium. Springs are the iconic example, not the only one.

↳ **Dig Deeper — Why every potential well looks like a spring near its minimum**

*The chapter claims that almost any restoring force becomes Hooke's law for small enough displacements. The mathematical reason is Taylor expansion of the potential around the minimum — the quadratic term is the leading nonzero term, and it gives a linear force. This explains the surprising universality of simple harmonic motion across physics.*

**Prompt:**
> Walk me through why any potential energy function $U(x)$, near a stable minimum at $x_0$, looks like $U(x) \approx \frac{1}{2}k(x - x_0)^2$. Use Taylor expansion: explain why $U(x_0)$ is a constant we can drop, why $U'(x_0) = 0$ (it's a minimum), and why the leading non-trivial term is the quadratic one with $k = U''(x_0)$. Then explain why this guarantees that almost any oscillating system — atomic vibrations, pendulums, electrical LC circuits — exhibits simple harmonic motion for small amplitudes. End with one sentence on what changes when amplitudes get large enough that higher-order terms in the Taylor series matter.

**What to do with the output:** Save it. The Taylor-expansion argument is one of the most reused tricks in physics. You will see it again in molecular vibrations (Chapter 30), in field theory, and in quantum perturbation theory.

---

## Concept 2 — The pendulum, energy, and damping

### Galileo at Pisa Cathedral, 1583

The story is repeated in every physics textbook because it is too good to leave out: a 19-year-old Galileo Galilei, sitting through a long Mass at Pisa Cathedral in 1583, watches a swinging chandelier overhead and notices something odd. The chandelier's swings get smaller as friction drains the energy, but the *time per swing seems unchanged*. He times them against his own pulse — there are no clocks accurate enough yet — and convinces himself: the period of a pendulum is independent of amplitude.

Galileo never quite published the result formally, but the insight launched pendulum-based timekeeping (and Galileo himself). In 1657, Christiaan Huygens patented the first pendulum clock, accurate to about 10 seconds per day — a hundred times better than any earlier mechanism. Pendulums ran the world's clocks for the next 270 years.

The physics: a pendulum of length $L$, displaced by small angle $\theta$, has restoring force $F = -mg\sin\theta \approx -mg\theta$ for small $\theta$. The "effective spring constant" works out to give

$$T = 2\pi\sqrt{\frac{L}{g}}.$$

Notice what is *not* in the formula: the mass $m$. A heavier bob does not change the period. Galileo could (and did) demonstrate this by hanging two pendulums of different mass side-by-side and watching them swing in lock-step. Notice also: the period grows with $\sqrt{L}$ — a 1-meter pendulum has period $T = 2\pi\sqrt{1/9.80} \approx 2.01$ s. (This is approximately why old grandfather clocks are about a meter tall — their pendulum ticks every second.)

### The mechanism — energy in a simple harmonic oscillator

A simple harmonic oscillator has two reservoirs of energy that trade back and forth. Kinetic energy lives in the moving mass: $KE = \frac{1}{2}mv^2$. Potential energy lives in the deformed spring (or the lifted pendulum bob): for a spring, $PE = \frac{1}{2}kx^2$. The total mechanical energy

$$E = \frac{1}{2}kx^2 + \frac{1}{2}mv^2$$

is constant in the absence of friction. At maximum displacement ($x = x_0$), all the energy is potential and the mass is momentarily at rest. At equilibrium ($x = 0$), all the energy is kinetic and the mass is moving fastest.

Maximum speed:

$$v_\text{max} = x_0 \omega = x_0 \sqrt{\frac{k}{m}}.$$

This trade between KE and PE — twice per oscillation — is the energy fingerprint of simple harmonic motion. In a damped system, the trade still happens, but a small amount of energy leaves the system as heat each cycle, and the amplitude shrinks.

### Damping: under, critical, over

Real oscillators lose energy to friction, air drag, internal hysteresis. Add a damping force proportional to velocity ($F_\text{damp} = -bv$, where $b$ is the damping constant) and three regimes appear:

**Underdamped** — $b$ small. The system oscillates many cycles, with the amplitude decaying exponentially. Most musical instruments, tuning forks, cymbals, your tuning-fork-style quartz crystal.

**Critically damped** — $b$ tuned to a specific value where the system returns to equilibrium as fast as possible *without overshooting*. Door closers, car shock absorbers, many control systems. The mathematician's favorite damping regime — the boundary between two qualitative behaviors.

**Overdamped** — $b$ large. The system creeps slowly back to equilibrium, never overshooting, but slower than critical. Honey-thick dashpots, very viscous systems.

A car suspension is designed to be just under critical — bouncing slightly when you go over a bump, but settling fast. If your shock absorbers fail (worn-out struts), the system becomes underdamped: every bump produces a long, sickening oscillation.

### The trade-off

Adding damping to the model trades **mathematical elegance for physical realism.** The undamped SHO has clean, closed-form sinusoids. The damped SHO requires exponentials multiplying the sinusoids. The critically damped case is a special tuning that doesn't quite oscillate. Each step toward realism costs you simplicity. The trade is necessary because real systems all damp.

### Worked example — the second's pendulum

Build a pendulum that has period exactly 2 seconds (a "second's pendulum," historically used in clocks because it ticks once per second). Required length:

$$T = 2\pi\sqrt{L/g} \implies L = \frac{T^2 g}{4\pi^2} = \frac{(2)^2 (9.80)}{4\pi^2} = \frac{39.2}{39.48} \approx 0.993 \text{ m}.$$

About 99.3 cm. This is approximately why grandfather clocks are about a meter tall. The pendulum case must be tall enough to accommodate the full swing.

**Sanity check.** At the equator, $g = 9.78 \text{ m/s}^2$; at the poles, $g = 9.83 \text{ m/s}^2$. A second's pendulum tuned at the poles would tick faster at the equator (longer period than 2 seconds) by a fraction of a percent. This is exactly how, in the 17th and 18th centuries, scientists first measured the variation of $g$ across the Earth's surface — by noting that a pendulum clock that kept perfect time in Paris ran slow in Cayenne (Jean Richer, 1672). The local oblateness of the Earth (Earth is fatter at the equator) was inferred from this measurement before it could be observed any other way.

### Common misconceptions

- *"A heavier pendulum bob has a longer period."* No — the period is independent of mass for a simple pendulum, just like free-fall acceleration is independent of mass.
- *"A damped oscillator's frequency is exactly the same as the undamped one."* Slightly different. The damped angular frequency $\omega_d = \sqrt{\omega_0^2 - (b/2m)^2}$ is slightly less than $\omega_0$. For light damping, the difference is tiny; for heavy damping, the system stops oscillating altogether (critical / overdamped).
- *"Critically damped means it stops moving."* It means it returns to equilibrium fastest *without overshoot*, not that it stops oscillating instantaneously. There is still a transient.

↳ **Dig Deeper — Resonance, the Tacoma Narrows Bridge, and the wineglass**

*Resonance is the most dramatic consequence of harmonic motion: when a periodic driving force matches the natural frequency of an oscillator, the response builds to enormous amplitude. The famous case is the 1940 Tacoma Narrows Bridge collapse, though the physics is more nuanced than usually told.*

**Prompt:**
> Explain mechanical resonance — what happens when a driven oscillator is forced at its natural frequency, why the steady-state amplitude depends on the quality factor Q, and how the bandwidth of resonance narrows as Q increases. Then evaluate the standard story of the 1940 Tacoma Narrows Bridge collapse — was it actually resonance with wind gusts, or was it aeroelastic flutter (a more nonlinear mechanism)? Use the mechanical-resonance equations to compute roughly how an opera singer can shatter a wineglass with a sustained note. End with one sentence on the engineering response — why bridges and skyscrapers now incorporate tuned mass dampers.

**What to do with the output:** Save it. Resonance shows up in every chapter going forward — in AC circuits (Ch 23), in light-matter interaction (Ch 25-27), and in MRI imaging (Ch 31).

---

## Concept 3 — Waves: oscillation in space and time

### Hokusai's Great Wave, c. 1831

Katsushika Hokusai's woodblock print *The Great Wave off Kanagawa*, made around 1831, shows three boats and Mount Fuji in the trough of an enormous breaking wave. The wave is famous because it captures something physical about how water moves: the foam at the crest, the curl, the textured surface. What it does *not* capture — what no still image can capture — is that the water itself is mostly moving up and down, not horizontally. The wave moves across the surface; the water particles oscillate in place. A floating object bobs and barely drifts.

This is the single most important fact about waves. The wave is a propagating *pattern*, not a propagating *substance*. A wave on a string, a sound wave in air, a wave on the ocean — in each case, the medium oscillates locally, and the disturbance moves through the medium.

### The mechanism — what a wave is

A **wave** is a disturbance that propagates through a medium (or through vacuum, in the case of light). Waves carry energy without carrying matter. The basic quantities:

- **Wavelength** $\lambda$: the spatial distance between consecutive crests.
- **Frequency** $f$: the number of crests passing a fixed point per second.
- **Period** $T = 1/f$: the time between consecutive crests passing a fixed point.
- **Wave speed** $v$: how fast the pattern moves.
- **Amplitude** $A$: the maximum displacement of the medium from rest.

The relationship that ties them:

$$v = f \lambda.$$

This is exact. A wave covers a distance of one wavelength in one period, so distance/time = $\lambda / T = \lambda f$.

Two flavors of wave:

**Transverse:** The medium oscillates *perpendicular* to the direction of wave travel. A wave on a string. Light. Stadium "waves" of standing fans.

**Longitudinal:** The medium oscillates *parallel* to the direction of wave travel — compression and rarefaction. Sound waves in air. Seismic P-waves.

Wave speed depends on the medium. For a wave on a stretched string, $v = \sqrt{T/\mu}$, where $T$ is tension and $\mu$ is mass per length. For sound in air at room temperature, $v \approx 343$ m/s. For light in vacuum, $v = 2.998 \times 10^8$ m/s. The wave equation that produces all of these comes from applying Newton's laws to the local oscillating medium and asking how disturbances propagate.

### Standing waves and resonance

When a wave reflects from a boundary and overlaps itself, it can produce a **standing wave** — a pattern that oscillates in place rather than propagating. A guitar string fixed at both ends supports standing waves only at specific wavelengths: those for which the string length is a half-integer multiple of the wavelength. The lowest mode (fundamental) has $\lambda = 2L$; higher modes (harmonics or overtones) have $\lambda = L, 2L/3, L/2, \dots$.

The corresponding frequencies are

$$f_n = \frac{n v}{2L}, \quad n = 1, 2, 3, \dots,$$

a "harmonic series." Pluck a guitar string and you excite the fundamental plus a slowly decaying mix of overtones; the relative strengths of the overtones are what give different instruments their characteristic timbre.

This is also resonance, in spatial form. The string "wants" to vibrate at its natural frequencies. Drive it at any of those frequencies (by bowing, plucking, or air pressure) and you get a large amplitude response.

### Wave intensity

The energy a wave carries per unit area per unit time is its **intensity**:

$$I = \frac{P}{A},$$

units W/m². For a spherical wave radiating from a point source, energy spreads over a sphere of area $4\pi r^2$, so intensity falls with the inverse square of distance:

$$I = \frac{P}{4\pi r^2}.$$

This is why a stereo speaker sounds quieter as you walk away — not because the wave is dying but because the same energy is spread over a larger sphere. Sound, light, gravity — all obey inverse-square laws when they spread spherically from a point source.

### The trade-off

The wave description trades **microscopic detail for macroscopic prediction.** We don't track every air molecule in a sound wave; we track the local pressure deviation. We don't track every photon in a light wave (in classical wave theory); we track the field amplitude. The trade is excellent in the regimes where wave behavior dominates and worsens at very high or very low intensities, where particle (quantum) descriptions become necessary.

### Worked example — the speed of sound from a thunderclap

You see a flash of lightning. Five seconds later, you hear the thunder. How far away is the lightning?

**Reasoning.** Light travels at $3 \times 10^8$ m/s — the lightning flash arrives essentially instantaneously across any earthly distance. Sound travels at about 343 m/s. So the time delay between flash and sound is governed by the sound's travel time.

$$d = v_\text{sound} \times t = 343 \text{ m/s} \times 5 \text{ s} \approx 1715 \text{ m} \approx 1.7 \text{ km}.$$

Or, if you prefer the rule of thumb: about 1 km for every 3 seconds of delay (or 1 mile per 5 seconds). The lightning is about a mile and a quarter away.

**Sanity check.** Lightning bolts often light entire cloud banks, which are several kilometers up. A few-kilometer distance is typical. The number passes the smell test.

### Common misconceptions

- *"A wave carries the medium with it."* No — the wave carries energy; the medium oscillates in place. Hokusai's swimmers would bob, not be swept off to Honshu.
- *"Frequency and wavelength are independent."* For a fixed medium, they are coupled by $v = f\lambda$. You can vary one and the other changes inversely.
- *"Standing waves are stationary, so they don't carry energy."* They are made of two waves moving in opposite directions and the *net* energy flow is zero, but each component wave carries energy. The vibration is real and dissipates over time as the system damps.

↳ **Dig Deeper — Why waves obey the same equation in different media**

*Sound in air, light in vacuum, ripples on a pond, vibrations on a string — all obey the same mathematical wave equation, with only the wave speed changing. Understanding why takes seeing the equation itself derived from local Newton's-law balances in the medium.*

**Prompt:**
> Walk me through how the wave equation $\partial^2 y/\partial t^2 = v^2 \partial^2 y/\partial x^2$ arises. Pick a stretched string under tension and apply Newton's second law to a small element of the string undergoing small transverse displacement. Show how the tension on both sides of the element produces a net restoring force proportional to the local curvature ($\partial^2 y/\partial x^2$), and derive the wave speed $v = \sqrt{T/\mu}$. Then briefly note how the analogous derivation for sound in air (using pressure, density, and bulk modulus) produces the same wave equation with $v = \sqrt{B/\rho}$. End with one sentence on why this universality is the reason "wave physics" is a single subject across optics, acoustics, and quantum mechanics.

**What to do with the output:** Save it. The same equation appears in light (Chapter 24), water waves, seismology, quantum mechanics (Schrödinger), and general relativity (gravitational waves). The universality is one of the deepest in physics.

---

## Synthesis — one equation, many systems

Step back. Three concepts:

1. **Hooke's law and SHO.** $F = -kx$ produces sinusoidal motion at $\omega = \sqrt{k/m}$. The same equation governs anything near equilibrium.

2. **Pendulum, energy, damping.** Pendulums use gravity as the restoring force; period $T = 2\pi\sqrt{L/g}$. Energy oscillates between KE and PE. Real systems damp; tuning the damping is engineering.

3. **Waves.** Oscillation propagates through space, with $v = f\lambda$. Strings, sound, light, water — same mathematics, different speeds.

The unifying claim: *simple harmonic motion is the universal small-amplitude behavior of any restoring system.* The fingerprint is sinusoidal motion at a single characteristic frequency. Once you can recognize it, you have a powerful tool.

### A worked example combining all three concepts — a tuned-mass damper in a skyscraper

Taipei 101 (constructed 2004, 508 m tall) sits on the seismic edge of the Pacific Plate and is regularly hit by typhoons. To keep it from swaying dangerously, the architects installed a **tuned-mass damper** at the top: a 660-tonne steel pendulum, 5.5 m in diameter, suspended from the building itself by cables.

The building has its own natural sway frequency around 0.15 Hz (period about 6.7 s). The damper is tuned to the same frequency: when the building sways one way, the damper swings the other way, and the inertia of the 660-ton ball pushes the building back toward equilibrium. The system is overdamped at the chosen damping coefficient — the goal is not to oscillate, but to absorb energy from the building's sway.

How long is the damper pendulum? Using $T = 2\pi\sqrt{L/g}$ with $T = 6.7$ s:

$$L = \frac{T^2 g}{4\pi^2} = \frac{(6.7)^2 (9.80)}{39.48} = \frac{440}{39.48} \approx 11.1 \text{ m}.$$

The cable suspension is about 11 m long. (Real Taipei 101 uses a 42 m cable in a different geometry that effectively shortens the pendulum, but the principle is correct.) The damper's mass is small compared to the building (about 0.2%), but tuned at the right frequency it absorbs enough sway energy to keep occupants from feeling sick on a windy day.

**Scale shift.** Same physics: a child on a swing pumping at the swing's natural frequency builds amplitude. A wineglass shattered by a soprano hitting its resonant note builds amplitude until structural failure. A bridge in a steady wind that excites its natural mode (Tacoma Narrows in 1940) builds amplitude until collapse. The tuned-mass damper is the engineering response: deliberately install something that *resists* resonant build-up. Same equation, applied with opposite intent.

---

## Exercises

### Warm-up

**16.1** *(LO 1, 2)* A 0.20 kg mass on a spring oscillates with period 0.50 s. What is the spring constant?

**16.2** *(LO 3)* A pendulum on the Moon (where $g_\text{Moon} = 1.62$ m/s²) is 1.00 m long. What is its period?

**16.3** *(LO 6)* A wave on a string has frequency 500 Hz and wavelength 0.40 m. What is its speed?

**16.4** *(LO 4)* A 0.50 kg mass on a spring (k = 100 N/m) is pulled 0.10 m from equilibrium and released. What is its maximum speed?

### Application

**16.5** *(LO 1, 2)* A car of mass 1200 kg sits on four identical springs. When you push down on it and release, the car bounces with period about 0.80 s. What is the spring constant of each spring?

**16.6** *(LO 5)* A car shock absorber should be critically damped. If it becomes underdamped (wear), describe what the driver feels going over a bump. If it becomes overdamped (clogged with old oil), describe what the driver feels.

**16.7** *(LO 6, 7)* A guitar's high-E string has fundamental 329.6 Hz. The string is 0.65 m long. What is the wave speed on the string? Compare to the speed of sound in air (343 m/s) — which is faster?

**16.8** *(LO 3)* You build a pendulum exactly 0.5 m long and observe a period of 1.42 s. What is the local value of $g$?

### Synthesis

**16.9** *(LO 1, 4, 7)* A child on a swing has effective length 2.5 m. (a) What is the natural period? (b) An adult pushes the swing at intervals matched to that period. After 5 pushes, the amplitude has built to 1 m. What does this tell you about the energy delivered per push, ignoring damping?

**16.10** *(LO 6, 7)* A piano A above middle C is 440 Hz. You strike it; the sound reaches your ear 0.10 s later. (a) How far is the piano? (b) What is the wavelength of the sound in air? (c) What is the wavelength of the same sound in water (sound speed ~1480 m/s)?

**16.11** *(LO 5, 7)* The 1940 Tacoma Narrows Bridge collapsed under a steady 19 m/s wind. The standard textbook story attributes this to resonance, but engineers now agree it was *aeroelastic flutter*. Without doing detailed math, explain the difference in one paragraph: what is resonance vs. flutter, and why does flutter not require the wind to oscillate?

### Challenge

**16.12** *(beyond chapter)* A quartz crystal in a wristwatch resonates at 32,768 Hz. The watch keeps time to about 15 s/month. (a) Express the timekeeping accuracy as a fractional uncertainty in frequency. (b) The Q factor (quality factor) of a resonant system is roughly the number of oscillations before amplitude decays significantly. Estimate the Q of the quartz crystal needed for this accuracy. (c) Compare to a typical pendulum's Q (~100) and a tuning fork's Q (~1000).

**16.13** *(beyond chapter)* Two identical pendulums of length 1.0 m are coupled by a weak spring connecting their bobs. If you start one swinging and leave the other at rest, energy slowly transfers back and forth between them — a "beating" pattern. Without doing the formal coupled-oscillator math, sketch what you predict the amplitudes of both pendulums look like over time, and explain why the energy transfer rate depends on the strength of the coupling.

---

## LLM Exercise — Chapter 16: Find the Oscillation in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** Identification of one oscillatory or wave-like component of your anchor phenomenon, with computed period/frequency/wavelength as appropriate.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste from Chapter 1].

For Chapter 16 (Oscillations and Waves), I want to find ONE periodic or wave-like component of my phenomenon and analyze it.

Please:

1. Identify the oscillation. Examples:
   - Bike commute: pedal cadence (cyclic crank rotation), or the bike's natural wheel-and-spring suspension frequency.
   - Coffee maker: thermostat heating cycle frequency.
   - Marathon: cardiac frequency (heart rate), respiratory rate, stride frequency.
   - Espresso machine: pump pulsation frequency, or the resonance of the boiler.
   - Basketball shot: the wobble frequency of the ball's spin.

2. Identify the underlying restoring mechanism. Is it Hooke's-law-like (a spring or pendulum)? A driven oscillator (heart muscle pacemaker)? A wave (sound)?

3. Compute the period and frequency. State inputs and uncertainty.

4. If it's a wave, also compute the wavelength using v = fλ.

5. Identify the damping in the system. Is it underdamped (rings for many cycles), critically damped (settles fast), or overdamped (creeps back)?

6. Identify whether resonance is helping or hurting the system.

7. Connect to Chapter 17 (Sound), where we extend wave physics to acoustics.

Save the output as logbook/chapter-16-oscillations.md.
```

### What this produces

Your sixteenth Logbook entry — a quantified periodic component of your phenomenon.

### How to adapt this prompt

- *For phenomena with no obvious oscillation*: every system has a natural frequency. A coffee cup has a "ringing" frequency if you tap it; a bike frame has a vibrational mode; a marathon runner has stride and heartbeat frequencies. Find one.
- *For Claude Code:* If you have an audio recording or accelerometer log, fit a Fourier transform and extract the dominant frequency.

### Connection to previous chapters

Builds on Chapters 4–7 (Newton's laws, work and energy). The energy-conservation argument for max velocity (Concept 2) uses Chapter 7 directly.

### Preview of next chapter

Chapter 17 zooms in on sound waves specifically — speed, intensity, the decibel scale, hearing, Doppler effect. The Chapter 17 LLM Exercise will analyze the acoustic component of your phenomenon.

---

## Chapter summary

Oscillation and wave behavior is governed by one structural pattern: a restoring force proportional to displacement, producing sinusoidal motion at a single characteristic frequency. Three commitments:

1. **Hooke's law $F = -kx$ produces simple harmonic motion** with period $T = 2\pi\sqrt{m/k}$ for a mass-spring or $T = 2\pi\sqrt{L/g}$ for a pendulum. The period is independent of amplitude.

2. **Energy oscillates between kinetic and potential** in the absence of damping, with maximum velocity $v_\text{max} = x_0\omega$. Real systems damp; engineering tunes the damping (under for music, critical for car shocks, over for door closers).

3. **Waves are oscillations propagating through space.** $v = f\lambda$ ties speed, frequency, and wavelength. Standing waves on a bounded medium produce a harmonic series of resonant frequencies. Energy spreads as $1/r^2$ for spherical sources.

The one idea that matters most: **almost any system, near equilibrium, looks like a simple harmonic oscillator.** Recognize the pattern and you can predict frequencies, energies, and resonant responses across an enormous range of physical systems.

The common mistake to watch for: **forgetting the small-amplitude approximation.** Pendulums are SHO only for small angles; springs follow Hooke's law only for small extensions. Push past the limit and the math breaks.

---

## What would change my mind

The chapter argues that the linear restoring-force model captures the dominant behavior of almost all oscillating systems near equilibrium. The argument would need revision if a class of important real-world oscillators were shown to be intrinsically nonlinear at the amplitudes of practical interest, requiring chaos theory or nonlinear dynamics from the start. (Some are — large-amplitude pendulums; turbulent flows — but the introductory linear approximation remains the right starting point for most problems.)

## Still puzzling

The deepest puzzle this chapter raises: *why is the same wave equation that describes sound in air and waves on a string also the equation that describes light in vacuum, and (with quantum modifications) electrons bound in atoms?* The mathematical universality of wave behavior — across mechanical, electromagnetic, and quantum systems — is striking and not fully explained at this level. We will revisit it when we meet electromagnetic waves (Chapter 24) and the Schrödinger equation (Chapter 29). For now, hold the puzzle: a small set of equations governs oscillation across the entire physical world.

---

## Connections forward

Chapter 17 is a focused application of this chapter to **sound** — speed, intensity, the decibel scale, the Doppler effect, acoustic resonance in tubes (organ pipes, the human vocal tract). Chapter 23 extends harmonic oscillation to AC circuits. Chapter 24 extends waves to light (electromagnetic). Chapter 29 extends harmonic oscillators to quantum mechanics, where the simple harmonic oscillator becomes the foundational worked-example for wave-mechanical particles in a potential well. The mathematics you installed here recurs in nearly every later chapter.

---

**Tags:** oscillation, simple-harmonic-motion, pendulum, waves, resonance

---

## AI Wayback Machine

**Robert Hooke** worked out the law of elasticity in 1660 — the stress-strain relationship for springs that still bears his name. He published it as the anagram "ceiiinosssttuv" before revealing the law to ensure priority.

**Run this:**

```
Who was Robert Hooke, and how does Hooke's law connect to the oscillatory motion we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Robert Hooke"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through why a spring obeying Hooke's law produces simple harmonic motion when displaced.
- Ask it about Hooke's bitter rivalry with Isaac Newton and how it shaped his historical reputation.

What changes? What gets better? What gets worse?
