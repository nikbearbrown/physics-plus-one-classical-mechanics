# Chapter 19 — Physics of Hearing

**Suggested titles**

1. Physics of Hearing
2. Sound, Decibels, Doppler: How Pressure Waves Become Music
3. Why a Whisper at 30 dB and a Jackhammer at 110 dB Are Both Logarithmic Lies

**TL;DR.** Sound is a longitudinal pressure wave traveling through a medium — typically air, at about 343 m/s near room temperature. The brain interprets a tiny range of intensities (from 10⁻¹² W/m² to 10 W/m², 13 orders of magnitude) and frequencies (20 Hz to 20 kHz, three orders of magnitude). To make those ranges manageable, hearing is logarithmic — which is why we use the decibel scale. This chapter pins down sound's mechanics, the dB scale, the Doppler shift, and the resonant tubes that make organs and trumpets work.

---

## A whisper at 30 dB and a jackhammer at 110 dB

Stand in a quiet library at midnight and the ambient noise level is about 30 dB. Stand near a working jackhammer and it's about 110 dB. In casual speech, the jackhammer is "much louder" than the whisper — maybe four times, you might guess from the numbers.

The actual ratio of acoustic intensities is a hundred million.

The decibel scale is logarithmic, by a factor of 10 per 10 dB. A 30 dB increase is a thousand-fold increase in power. The jackhammer is delivering a million times more acoustic energy per second per square meter than the whisper, yet your brain registers it as four times louder, because your brain — sensibly — processes intensity logarithmically. Otherwise the dynamic range from a falling leaf to a thunderclap would overwhelm any biological sensor.

This is the puzzle this chapter unpacks. Sound is a pressure wave, governed by the same wave equation as a guitar string or a ripple on water. Its perception, hearing, is biological signal processing that compresses fourteen orders of magnitude of intensity into a manageable scale of "soft" to "deafening." The physics and the biology meet at the decibel.

**Learning objectives.** By the end of this chapter you should be able to:

1. Describe sound as a longitudinal pressure wave and identify wavelength, frequency, period, and amplitude.
2. Compute the speed of sound in air given temperature: $v = 331 \sqrt{T/273}$ m/s.
3. Compute sound intensity (W/m²) and convert between intensity and decibel level: $\beta = 10 \log_{10}(I/I_0)$.
4. Compute the Doppler-shifted frequency for moving source or observer.
5. Compute the resonant frequencies of an open or closed tube (organ pipe, vocal tract).
6. Identify the audible range and the structure of human hearing sensitivity.
7. Reason quantitatively about ultrasound applications (medical imaging, sonography).

**Prerequisites.** Chapter 16 (oscillation, wave fundamentals, $v = f\lambda$). Chapter 13 (temperature, ideal gas), since sound speed depends on temperature.

**Why this chapter matters.** Sound is the primary communication channel for our species. The same physics governs ultrasound imaging in medicine, sonar in submarines, the design of concert halls, the engineering of microphones and loudspeakers, and the noise-cancellation in your headphones. The decibel scale you learn here will reappear anywhere a logarithmic scale captures a wide dynamic range — including the magnitude scale for earthquakes, the apparent magnitude scale for stars, and the bel scale for electrical signal-to-noise ratios.

---

## Concept 1 — Sound as a longitudinal pressure wave

### A clarinet in an anechoic chamber

In 2015, an acoustician at IRCAM in Paris recorded a single sustained note from a clarinet inside an anechoic chamber — a room lined with foam wedges that absorb essentially every reflected sound. With no echoes, no reverberation, just the direct sound of the instrument, what a high-resolution microphone captures is a slightly dirty sine wave at the played frequency, with smaller-amplitude overtones layered on top.

That captured waveform is sound, in its rawest form: a tiny periodic variation in air pressure, traveling outward from the clarinet bell at about 343 m/s. The peak pressure variation of a normal clarinet tone is about 0.02 Pa above and below atmospheric (which is 101,325 Pa) — five parts per million. The eardrum, sensing this five-parts-per-million wobble, sends a signal to the brain, and the brain hears music.

The fact that we are biologically tuned to detect pressure variations seven orders of magnitude smaller than atmospheric pressure is one of the most stunning measurement systems in nature. The ear is, in measurement-science terms, a pressure sensor good to one part in $10^{11}$ at the threshold of hearing.

### The mechanism — what sound is

A **sound wave** is a longitudinal disturbance in a fluid (or solid) — alternating regions of compression (pressure slightly higher than ambient) and rarefaction (pressure slightly lower than ambient) propagating outward from a source.

In air, the molecules don't travel with the wave. They oscillate back and forth around their equilibrium positions — by less than a millimeter for ordinary sounds — and the *pattern* of their oscillation moves at the speed of sound. Same as the wave on the string in Chapter 16: the medium oscillates locally, the pattern propagates.

The standard wave relations apply: $v = f\lambda$, where for sound in air at room temperature $v \approx 343$ m/s. So a 440 Hz "A" note has wavelength $\lambda = 343/440 \approx 0.78$ m. A 20 Hz bass tone has wavelength $\sim 17$ m — about the size of a room. A 20 kHz trumpet harmonic has wavelength $\sim 1.7$ cm — about the diameter of a grape.

### Speed of sound depends on the medium

In an ideal gas, the speed of sound depends only on the temperature and the gas's molecular structure:

$$v = \sqrt{\frac{\gamma R T}{M}},$$

where $\gamma$ is the ratio of specific heats (1.40 for air), $R = 8.314$ J/(mol·K), $T$ is absolute temperature, and $M$ is the molar mass. For air at 0 °C (273 K) this gives $v \approx 331$ m/s. A practical formula:

$$v = 331 \sqrt{\frac{T}{273}} \text{ m/s} \quad (T \text{ in kelvin}),$$

or equivalently $v \approx 331 + 0.6 T_C$ m/s with $T_C$ in Celsius. At 20 °C, $v \approx 343$ m/s.

In other media, sound is faster — about 1480 m/s in water, about 5000 m/s in steel. This is why a child placing an ear to a railroad track hears the approaching train long before the airborne sound arrives.

### The trade-off

Treating sound as a pure longitudinal wave trades **complexity of real waveforms for the cleanness of $v = f\lambda$.** Real sound is messy — overtones, transients, room acoustics, partial reflections. The simplification gives us a clean equation set; reality is a sum of many such waves, computable with Fourier decomposition (saved for a future chapter).

### Worked example — speed of sound in summer vs. winter

A friend on the other side of an open field is 100 m away. They clap their hands. How long until you hear the clap, on a winter day at $-10$ °C and a summer day at $30$ °C?

**Winter:** $T = 263$ K, $v = 331\sqrt{263/273} \approx 325$ m/s. Time: $100/325 \approx 0.308$ s.

**Summer:** $T = 303$ K, $v = 331\sqrt{303/273} \approx 348$ m/s. Time: $100/348 \approx 0.287$ s.

The difference is about 21 milliseconds — small but consistently in the predicted direction. For musicians performing outdoors, even this small temperature dependence matters: the speed of sound in a brass instrument's tube changes with temperature, shifting the resonant frequency and the pitch.

### Common misconceptions

- *"Sound carries air with it."* No — air molecules oscillate locally. Place a feather in front of a speaker and it doesn't drift away (much).
- *"Sound is faster in warm air because warm air is less dense."* Density actually plays the opposite role in the formula. The driver is temperature itself: warmer molecules move faster on average, transmitting collisions more rapidly.
- *"There is no sound in space."* Correct — vacuum has no medium to support pressure waves. *Star Wars* dogfight sound is dramatic license. The Sun's interior, however, does support pressure waves (helioseismology), since it has a medium.

↳ **Dig Deeper — Why sound is faster in solids than liquids than gases**

*The speed of sound depends on two material properties: how stiff the medium is (resistance to compression) and how dense it is. In a stiffer medium, restoring forces are stronger, so disturbances propagate faster. In a denser medium, more inertia must be moved, so disturbances propagate slower. The ratio of these competing effects gives the wave speed.*

**Prompt:**
> Explain why the speed of sound in a medium goes as $v = \sqrt{B/\rho}$, where $B$ is the bulk modulus (stiffness) and $\rho$ is the density. Walk me through the physical intuition: why stiffer = faster, why denser = slower. Then explain why sound goes faster in steel ($v \approx 5000$ m/s) than in water ($v \approx 1480$ m/s) than in air ($v \approx 343$ m/s) despite their increasing densities — show that the bulk modulus increases far faster than the density across these materials. End with one sentence on why this matters for non-destructive testing of metals using ultrasound.

**What to do with the output:** Save it. The same $v = \sqrt{(\text{stiffness})/(\text{inertia})}$ pattern appears for every wave: strings, electromagnetic waves in media, even matter waves in quantum mechanics.

---

## Concept 2 — Intensity and the decibel scale

### The threshold of hearing — $10^{-12}$ W/m²

A human ear at peak sensitivity (around 3000–4000 Hz, the frequency band of speech consonants) can detect sound intensities as low as $10^{-12}$ W/m². That number is so small it is hard to grasp. One trillionth of a watt per square meter. A whole human eardrum, with area about 60 mm² = $6 \times 10^{-5}$ m², receives a signal of $\sim 6 \times 10^{-17}$ W at threshold — about half a femtowatt.

The same ear can tolerate intensities up to about 10 W/m² before pain — thirteen orders of magnitude higher. A single sensor with 13 orders of magnitude of useful range is unprecedented in engineering. Your eyes have about 11 orders. Almost no engineered sensor matches either.

The trick the ear uses is logarithmic compression. Intensity at the eardrum is converted to firing rate of auditory nerves in a way that approximately respects $\log(I/I_0)$ — meaning equal *ratios* feel like equal *steps* in loudness. Doubling intensity feels like one constant amount more, regardless of what the starting intensity was. This is Weber's law applied to hearing, and it is also why we use the decibel.

### The mechanism — intensity, sound intensity level, decibels

**Intensity** $I$ is power per unit area, units W/m². For a spherical wave radiating from a point source of power $P$, intensity falls as $1/r^2$:

$$I = \frac{P}{4\pi r^2}.$$

A 1 W loudspeaker at 1 m distance delivers $I = 1/(4\pi) \approx 0.080$ W/m² to a listener. At 10 m, intensity drops by 100×, to $8 \times 10^{-4}$ W/m². At 100 m, by another 100×, to $8 \times 10^{-6}$ W/m². The inverse-square law is one of the cleanest geometric facts in physics.

**Sound intensity level** $\beta$, in decibels, compares an intensity $I$ to the threshold $I_0 = 10^{-12}$ W/m²:

$$\beta = 10 \log_{10}\left(\frac{I}{I_0}\right) \text{ dB}.$$

The factor of 10 is convention. The base-10 logarithm makes equal increments in $\beta$ correspond to equal *factors* in $I$.

A useful table:

| Sound | Intensity (W/m²) | Level (dB) | Description |
|---|---|---|---|
| Threshold of hearing | $10^{-12}$ | 0 | barely audible |
| Rustling leaves | $10^{-11}$ | 10 | very quiet |
| Whisper at 1 m | $10^{-10}$ | 20 | quiet library |
| Quiet room | $10^{-9}$ | 30 | |
| Normal conversation | $10^{-6}$ | 60 | |
| Heavy traffic | $10^{-3}$ | 90 | hearing damage with prolonged exposure |
| Jackhammer at 1 m | $10^{-1}$ | 110 | painful |
| Threshold of pain | $10^1$ | 130 | dangerous |
| Jet engine at 30 m | $10^2$ | 140 | hearing damage from brief exposure |

Notice the pattern: each 10 dB step is a 10× increase in intensity. Each 3 dB step is a 2× increase (since $\log_{10} 2 \approx 0.30$). A whisper and a jackhammer are 80 dB apart, which is $10^8 = 100$ million times in intensity — but maybe only ~30× in perceived loudness, because perception is logarithmic.

### The trade-off

The decibel scale trades **intuitive direct measurement for logarithmic compression.** Using dB, "loud" and "soft" become single-digit numbers across the entire human range. The cost: arithmetic on dB requires care (you cannot add dB values to combine sources; you must convert to intensity, add intensities, convert back to dB).

### Worked example — a 1 kW concert speaker at 50 m

A rock-concert speaker delivers 1 kW of acoustic power. What is the sound intensity level at 50 m distance?

**Reasoning.** Treat the speaker as a point source radiating into a hemisphere (the floor blocks downward radiation), so the relevant area is $2\pi r^2$:

$$I = \frac{P}{2\pi r^2} = \frac{1000}{2\pi (50)^2} = \frac{1000}{15{,}708} \approx 0.064 \text{ W/m}^2.$$

Convert to dB:

$$\beta = 10 \log_{10}\left(\frac{0.064}{10^{-12}}\right) = 10 \log_{10}(6.4 \times 10^{10}) \approx 108 \text{ dB}.$$

That is dangerous-territory loud, even at 50 m from the stage. Consistent with concerts that issue earplugs to attendees in the front rows.

**Sanity check.** At 50 m, the inverse-square law says we have 1/(50²) = 1/2500 of the intensity at 1 m. At 1 m, $I = 1000/(2\pi) \approx 159$ W/m² — far above the pain threshold of 10 W/m². You would not stand 1 m from the speaker without ear protection. The numbers all line up.

### Common misconceptions

- *"Adding two equal sounds doubles the dB."* No — it adds 3 dB. (Intensity doubles, $\log_{10}(2) \approx 0.30$, multiply by 10 = 3.)
- *"0 dB means silence."* No — 0 dB is the threshold of hearing, not zero intensity. Quieter sounds exist; we just can't hear them.
- *"Negative dB is impossible."* No — sound below the human threshold can still be measured; an ultrasonic detector can register sounds at $-40$ dB SPL.

↳ **Dig Deeper — Why hearing is logarithmic across many senses**

*Weber's law (sometimes called the Weber-Fechner law) holds that perception of stimulus intensity is logarithmic across many senses — hearing, vision, weight, even time. The logarithmic compression turns ratios into perceived equal steps. This is biological signal processing's solution to the "huge dynamic range" problem.*

**Prompt:**
> Explain the Weber-Fechner law: that perceived stimulus intensity scales as the logarithm of physical intensity. Walk through how this applies to (a) hearing (the dB scale), (b) vision (stellar magnitude scale), and (c) the perception of weight ("just noticeable difference"). Then critique it: where does the law fail? In what regimes does perception scale linearly or sub-logarithmically? End with one sentence on why this matters for designing user interfaces — display brightness, audio volume controls, etc.

**What to do with the output:** Save it. The Weber-Fechner generalization will reappear in any course that touches psychophysics, vision (Ch 26), or signal-processing engineering.

---

## Concept 3 — Doppler effect, resonant tubes, and sonic booms

### A passing motorcycle at 60 mph

You are standing on the curb. A motorcycle passes by at 27 m/s (60 mph), engine humming at a steady frequency. As the bike approaches, the engine sounds higher-pitched than it really is. The instant it passes, the pitch drops abruptly to a lower note. After it passes, you hear the lower note steady until the bike vanishes from earshot.

This is the **Doppler effect**, named for Christian Johann Doppler (1803–1853), who first explained it. The wave fronts emitted by the moving source pile up in the direction of motion (shorter wavelength, higher frequency at the listener) and stretch out behind (longer wavelength, lower frequency). The observed frequency depends on the relative motion of source and observer:

$$f_\text{obs} = f_\text{src} \left(\frac{v_\text{sound} \pm v_\text{obs}}{v_\text{sound} \mp v_\text{src}}\right),$$

with the upper signs when source and observer are approaching, lower when separating. For the motorcycle approaching at 27 m/s, with $v_\text{sound} = 343$ m/s and engine fundamental $f_\text{src} = 200$ Hz:

$$f_\text{obs} = 200 \left(\frac{343}{343 - 27}\right) = 200 \left(\frac{343}{316}\right) \approx 217 \text{ Hz}.$$

After passing:

$$f_\text{obs} = 200 \left(\frac{343}{343 + 27}\right) \approx 185 \text{ Hz}.$$

A jump of 32 Hz, from 217 to 185, as the bike passes — about a minor third on a piano. Easily perceptible. This is why we use Doppler shifts for radar speed traps, weather radar, ultrasound flow measurement, and astronomical redshift estimates of stellar velocity.

### The mechanism — Doppler in detail

The geometric origin: in time $t$, a source emits $f_\text{src} t$ wave crests. If the source is moving at $v_\text{src}$ toward an observer, those crests are packed into the distance $(v_\text{sound} - v_\text{src}) t$ instead of $v_\text{sound} t$. The compressed wavelength is

$$\lambda_\text{obs} = \frac{v_\text{sound} - v_\text{src}}{f_\text{src}}$$

and the observed frequency is $v_\text{sound}/\lambda_\text{obs}$, which gives the formula above.

When the source moves at the speed of sound ($v_\text{src} = v_\text{sound}$), the denominator vanishes — the wave fronts pile up into a sharp shock, and we have a **sonic boom**. The Concorde supersonic airliner produced a boom that could shatter windows on the ground; this is why supersonic flight over populated land is largely banned.

### Resonant tubes — open and closed

A tube of length $L$ supports standing waves at specific frequencies, just like a string. The boundary conditions matter:

**Both ends open (flute, organ pipe with open end):** Pressure nodes at both ends; allowed wavelengths $\lambda_n = 2L/n$, so

$$f_n = \frac{n v}{2L}, \quad n = 1, 2, 3, \dots$$

All harmonics present.

**One end closed (clarinet, panpipe, the human vocal tract):** Pressure node at the open end, antinode at the closed end; allowed wavelengths $\lambda_n = 4L/(2n-1)$, so

$$f_n = \frac{(2n-1)v}{4L}, \quad n = 1, 2, 3, \dots$$

Only odd harmonics (fundamental, third, fifth, …). This is why a clarinet (closed at the mouthpiece, open at the bell) and a flute (open at both ends) sound different even at the same pitch — different overtone structure.

**Worked example — flute fundamental.** A concert C flute is about 67 cm long, open at both ends. Fundamental:

$$f_1 = \frac{v}{2L} = \frac{343}{2 \times 0.67} = \frac{343}{1.34} \approx 256 \text{ Hz}.$$

Middle C is 261.6 Hz — close to my back-of-envelope number, with the small discrepancy from end corrections that the simple formula ignores.

### Ultrasound applications

Ultrasound is sound above the human hearing range ($> 20$ kHz). Common medical ultrasound runs at 1–10 MHz. The wavelengths in tissue (sound speed ~1540 m/s in soft tissue) are 1.5 mm to 0.15 mm — fine enough to image small structures. Ultrasound imaging works by sending a pulse and timing the echoes from tissue boundaries:

$$d = \frac{v_\text{tissue} \times t_\text{echo}}{2}.$$

A 50 μs echo from a heart valve corresponds to $d = (1540)(50 \times 10^{-6})/2 = 0.039$ m = 3.9 cm depth. Doppler ultrasound, additionally, shifts give blood flow velocity in real time — used routinely in cardiac and obstetric imaging.

### The trade-off

Wave-physics treatment of sound trades **mathematical idealization for physical universality.** Real sound has finite-amplitude effects (shock waves, harmonic distortion), and real boundaries reflect imperfectly. The wave-equation framework gets the basics right, in the regime where most musical and engineering applications live, but breaks down at very high amplitudes and at very high frequencies near molecular scales.

### Common misconceptions

- *"The Doppler shift is the same for source-moving and observer-moving."* Approximately true at low speeds, exactly true only in the relativistic case (which we will meet in Chapter 28). Classical Doppler distinguishes the two.
- *"A sonic boom happens once when the plane breaks the sound barrier."* No — the boom is continuous, traveling with the plane, like a wake from a boat. People on the ground hear it as a single bang because the boom passes them once.
- *"Open tubes and closed tubes are interchangeable for music."* No — they have qualitatively different harmonic structures (all harmonics vs. odd harmonics only), which is why instruments have characteristic timbre.

↳ **Dig Deeper — Why doppler ultrasound can measure blood flow**

*Doppler ultrasound is one of the most powerful non-invasive medical imaging techniques. By measuring the frequency shift of ultrasound reflected from moving red blood cells, doctors can map blood flow velocity in real time. The physics is the same Doppler effect that explains the changing pitch of a passing siren — applied at megahertz frequencies inside the body.*

**Prompt:**
> Walk me through how Doppler ultrasound measures blood flow velocity in arteries. Start with the physical setup: an ultrasound transducer emits ~5 MHz waves, which reflect off red blood cells moving with the blood. Show how the round-trip Doppler shift depends on blood velocity, ultrasound frequency, sound speed in tissue, and the angle between the ultrasound beam and the blood flow direction. Compute a sample case: 50 cm/s blood flow, 5 MHz transducer, 60° angle. End with one sentence on why mis-estimating the angle produces a systematic error in the velocity reading.

**What to do with the output:** Save it. Doppler ultrasound is a clean, computable medical application of Chapter 17 physics and an excellent example of how undergraduate-level wave equations show up in clinical practice.

---

## Synthesis — sound is wave physics, biologically tuned

Step back. Three concepts:

1. **Sound is a longitudinal pressure wave.** It obeys $v = f\lambda$ with speed depending on temperature and medium. Wavelengths in the audible range span $\sim 17$ m (bass) to $\sim 1.7$ cm (high treble).

2. **Intensity is power per area; the decibel scale compresses 13 orders of magnitude into single digits.** $\beta = 10\log_{10}(I/I_0)$ with $I_0 = 10^{-12}$ W/m². Each 10 dB = 10× intensity = perceived doubling of loudness.

3. **Doppler shifts, resonant tubes, sonic booms.** Moving sources/observers shift frequency; bounded media support discrete resonant modes; supersonic motion piles up shock waves.

The unifying claim: *sound physics is wave physics, applied to a longitudinal mode in air, and the human auditory system is engineering that compresses an enormous range into useful biological signals.* The decibel is the meeting point between physics (intensity in W/m²) and biology (perception in barely-discriminable steps).

### A worked example combining all three concepts — designing a public address system

You need to install a PA system at an outdoor stadium. Goal: deliver 75 dB SPL (comfortable speech level) to a listener at the back of the stadium, 80 m from the speaker. The speaker can be approximated as a hemispherical radiator. What acoustic power is required?

**Step 1 — Required intensity.** $\beta = 75$ dB, so

$$I = 10^{\beta/10} \cdot I_0 = 10^{7.5} \times 10^{-12} = 3.16 \times 10^{-5} \text{ W/m}^2.$$

**Step 2 — Power.** For hemispherical radiation, $P = 2\pi r^2 I$:

$$P = 2\pi (80)^2 (3.16 \times 10^{-5}) = 2\pi \times 6400 \times 3.16 \times 10^{-5} \approx 1.27 \text{ W}.$$

**Step 3 — Doppler check.** For static listeners and a fixed source, no Doppler shift; the frequency arrives unmodified. (If the singer moved across the stage, a 1 m/s walk would shift a 1 kHz tone by $\sim 3$ Hz — imperceptible.)

**Step 4 — Sanity check.** Stadium PA systems rated at hundreds to thousands of acoustic watts to deal with multiple listeners, ambient noise, and uneven coverage. 1.27 W gets one listener at the back; multiply by area-coverage factor and inefficiency to scale up.

**Scale shift.** That same calculation, applied at $r = 1$ km for a sonic boom from a supersonic jet at 50 m altitude, governs why people on the ground hear an earsplitting bang: the boom intensity, even after spreading geometrically, can exceed 130 dB at ground level. Same equations, different scale, dramatically different consequence.

---

## Exercises

### Warm-up

**17.1** *(LO 1, 2)* Compute the speed of sound in air at $-10$ °C and at $40$ °C. By what percentage does it differ from the room-temperature value (343 m/s at 20 °C)?

**17.2** *(LO 3)* A jet engine at takeoff produces 140 dB SPL at 30 m. What is the intensity in W/m²?

**17.3** *(LO 3)* If you halve the distance from a point source, what is the dB increase in level?

**17.4** *(LO 4)* A police siren at 1 kHz approaches you at 30 m/s. What frequency do you hear? After it passes, what frequency?

### Application

**17.5** *(LO 3)* Two identical sources, each at 70 dB at your location, are heard simultaneously. What is the combined dB level?

**17.6** *(LO 5)* An organ pipe open at both ends is 1.5 m long. What are the first three resonant frequencies (in air at 20 °C)?

**17.7** *(LO 5)* A clarinet (closed at one end) is 60 cm long. What are the first three resonant frequencies?

**17.8** *(LO 4, 7)* A Doppler ultrasound at 5 MHz reflects off a red blood cell moving at 30 cm/s toward the transducer. What is the round-trip Doppler shift?

### Synthesis

**17.9** *(LO 3, 6)* Hearing damage from noise exposure is often quantified as "dose" — proportional to $I \times t$. OSHA permits 8 hours of 90 dB exposure per day. How long is the safe exposure at 95 dB? At 105 dB? At 115 dB?

**17.10** *(LO 4, 5)* A tuning fork vibrates at 440 Hz. You hold it next to an open organ pipe of variable length. By what range of pipe lengths does the system go through resonance?

**17.11** *(LO 4)* The redshift of distant galaxies is the optical Doppler effect, applied to light from receding sources. The formula for low velocities is $\Delta f / f = -v/c$. A distant quasar shows a 10% wavelength shift toward longer wavelengths. What is its recession velocity?

### Challenge

**17.12** *(beyond chapter)* The "cocktail party effect" is the brain's ability to focus on one voice in a crowd. (a) Compute the wavelength of a 3 kHz speech consonant in air. (b) Argue from interference (Chapter 16) why the brain might use phase information at the two ears to localize a sound source. (c) Why does this work better at 3 kHz than at 30 Hz?

**17.13** *(beyond chapter, LO 7)* A medical ultrasound at 7 MHz produces resolution comparable to its wavelength in tissue ($v_\text{tissue} = 1540$ m/s). (a) What is the resolution? (b) Why don't doctors use 100 MHz ultrasound for finer resolution? (Hint: think about absorption with depth.) (c) For deep imaging, what trade-off do they make?

---

## LLM Exercise — Chapter 17: Sound in Your Anchor Phenomenon

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** An acoustic measurement of one component of your anchor phenomenon — a sound level, a frequency, or a Doppler shift.
**Tool:** Claude Project.

### The Prompt

```
I'm continuing my Physics Reality Check Logbook for College Physics with LLMs. My anchor phenomenon is [paste from Chapter 1].

For Chapter 17 (Physics of Hearing), I want to identify ONE acoustic component of my phenomenon and characterize it.

Please:

1. Identify the sound. Examples:
   - Bike commute: tire-road noise, wind whistling past helmet, brake squeal.
   - Coffee maker: pump noise, steam wand whistle.
   - Marathon: cadence of footstrikes (audible if running on pavement), breathing sound.
   - Espresso machine: pump pulse frequency.
   - Basketball: bounce thump frequency, swish of the net.

2. Estimate the sound's:
   (a) Frequency (in Hz). What part of the audible range?
   (b) Intensity at the listener's location (in dB SPL). Use a smartphone app for a measurement, or estimate.
   (c) Wavelength.

3. If there's a Doppler shift relevant to the situation (e.g., someone whistling past you on a bike), compute the shift.

4. Identify whether the sound is harmless, annoying, or potentially damaging (>85 dB sustained, >100 dB even briefly).

5. State inputs and uncertainty.

6. Connect to Chapter 18 (Electric Charge) — specifically, how a microphone converts the acoustic signal you just analyzed into an electrical signal.

Save the output as logbook/chapter-17-sound.md.
```

### What this produces

Your seventeenth Logbook entry — a quantified acoustic component of your phenomenon.

### How to adapt this prompt

- *For phenomena that are silent* (a sleeping person, a still cup of coffee): use ambient room noise as your subject, or consider an ultrasound or infrasound that would be present but inaudible.
- *For Claude Code:* If you have a smartphone audio recording, run a Fourier transform and identify the spectral peaks. Compare with the chapter's frequency formulas.

### Connection to previous chapters

Builds directly on Chapter 16's wave equation. The decibel scale is logarithmic compression you have not formally encountered before, but it generalizes anything where the human range is wide.

### Preview of next chapter

Chapter 18 introduces electric charge and electric fields — the foundation of all electricity, electronics, and ultimately the microphones that converted the sound you just analyzed into a digital signal. The Chapter 18 LLM Exercise will identify one electrical component of your phenomenon.

---

## Chapter summary

Sound is a longitudinal pressure wave; hearing is biological signal processing tuned to compress an enormous dynamic range. Three commitments:

1. **Sound is a wave with $v = f\lambda$,** with $v \approx 343$ m/s in air at 20 °C and faster in denser, stiffer media. Audible range: 20 Hz to 20 kHz.

2. **Intensity is power per area, and the decibel scale is logarithmic.** $\beta = 10\log_{10}(I/I_0)$, with $I_0 = 10^{-12}$ W/m². 0 dB is the threshold of hearing; 130 dB is the threshold of pain; the human range spans 13 orders of magnitude in intensity.

3. **Doppler shifts and resonant tubes are everyday wave physics applied.** Moving sources shift frequency; bounded tubes and strings support discrete resonant frequencies that determine musical instrument pitch and timbre.

The one idea that matters most: **sound is wave physics applied to a specific medium, and human hearing is logarithmic compression of an extraordinarily wide dynamic range.** The decibel is where the physics meets the biology.

The common mistake to watch for: **adding decibel levels arithmetically.** Two 70 dB sources don't make 140 dB; they make 73 dB. Convert to intensity, add, convert back.

---

## What would change my mind

The chapter argues that classical wave physics with logarithmic perception captures the dominant features of sound and hearing. The argument would need revision if a regime of audible sound were shown to require quantum-acoustic treatment (at the threshold of hearing, the energies *are* close to thermal-noise levels, and the question of whether single phonons can be heard is genuinely open in physiology).

## Still puzzling

The deepest puzzle this chapter raises: *why is human hearing approximately logarithmic and not linear?* The Weber-Fechner law is an empirical generalization, not a derived theorem, and the underlying neural mechanism (compression at multiple stages of the auditory pathway) is partially understood but not yet derivable from first principles. We can describe it; we cannot fully predict it from the molecular physiology.

---

## Connections forward

Chapter 18 begins **electricity** — electric charge, Coulomb's law, electric fields. The next several chapters build through circuits, magnetism, and electromagnetic induction toward the Chapter 24 climax: light as an electromagnetic wave. The wave physics you installed here recurs at every scale, from sound (this chapter) to light (Ch 24) to quantum matter waves (Ch 29). The decibel scale you learned will reappear in any context where you need to compress a wide dynamic range — including signal-to-noise ratios in electronics and the Richter scale for earthquakes.

---

**Tags:** sound, decibels, doppler-effect, wave-physics, hearing

---

## AI Wayback Machine

**Hermann von Helmholtz** wrote *On the Sensations of Tone* in 1863 — building a comprehensive theory of how the ear analyzes sound into its frequency components. Modern audiology, psychoacoustics, and audio engineering all begin with him.

**Run this:**

```
Who was Hermann von Helmholtz, and how does his work on hearing connect to the physics of hearing we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Hermann von Helmholtz"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Helmholtz's resonance theory of hearing — and where modern cochlear mechanics has revised it.
- Ask it about Helmholtz's range across physiology, physics, and philosophy.

What changes? What gets better? What gets worse?
