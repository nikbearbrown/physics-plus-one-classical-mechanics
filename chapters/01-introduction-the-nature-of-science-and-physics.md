# Chapter 1 — The Nature of Science and Physics

**Suggested titles**

1. The Nature of Science and Physics
2. Where Physics Begins: Laws, Units, and Honest Numbers
3. Le Grand K: How Physics Decides What a Thing Actually Is

**TL;DR.** Physics is the discipline that refuses to let a measurement be vague. This chapter walks you into the field by way of three commitments physicists make: that nature has discoverable order (laws, theories, models), that every quantity must be tied to a unit you can defend (the SI system), and that every number must carry an honest claim about how well you know it (uncertainty, significant figures, estimation). By the end, you should be able to convert between units fluently, propagate uncertainty through a calculation, and make a Fermi-style estimate without flinching.

---

## A vault outside Paris, May 2019

In a temperature-controlled vault at the Bureau International des Poids et Mesures in Sèvres, just outside Paris, sits a small cylinder of platinum-iridium alloy about the size of a golf ball. For 130 years it had a job. It *was* the kilogram. Not represented the kilogram, not approximated the kilogram. *Was.* If you wanted to know what one kilogram of mass actually felt like, your reference, in the end, was that cylinder. It had a name — *Le Grand K* — and replicas of it sat in similarly guarded vaults from Maryland to Tokyo, calibrated against the original every few decades.

There was a problem. The cylinder was changing. Not by much — perhaps fifty micrograms over a century, the weight of an eyelash. But it was changing, and the replicas were drifting from it in different directions, and nobody could say which one was right because *the kilogram was defined to be the cylinder*. The original was, by definition, exactly one kilogram, even if it was getting heavier or lighter. Which meant that the mass of every other object in the universe was, in some sense, also drifting, because the yardstick they were measured against was drifting.

On May 20, 2019, a vote of the General Conference on Weights and Measures put an end to this. From that day forward, the kilogram would no longer be the cylinder. It would be a number — a particular value of Planck's constant, $h = 6.62607015 \times 10^{-34}$ joule-seconds, fixed by international agreement, from which mass could be derived through quantum mechanics and a precision instrument called a Kibble balance. The cylinder kept its name, but lost its job. It is now a museum piece.

Hold this scene for a moment. A small lump of metal in a French vault. A 2019 vote that ended a 130-year arrangement. A definition that now lives inside a quantum-mechanical equation rather than inside a cabinet. This is what physics actually is — not the equations on the chalkboard, but the discipline of pinning down, to within the smallest expressible uncertainty, what each of your words and numbers means.

This chapter is the entry point. You walk in with curiosity. You walk out with three commitments physicists make, every time:

**Learning objectives.** By the end of this chapter you should be able to:

1. Distinguish a model, a theory, and a law, and explain why each lives at a different level of generality.
2. Identify the four fundamental SI units and explain why other units (force, energy, charge) are *derived* from them.
3. Convert fluently between units in any system using the cancellation method, and apply SI prefixes from $10^{-18}$ to $10^{18}$.
4. Calculate percent uncertainty, propagate uncertainty through multiplication and division using the method of adding percents, and apply the correct rules for significant figures in addition, subtraction, multiplication, and division.
5. Make a Fermi-style order-of-magnitude estimate of an unknown quantity from known reference values, and judge whether an answer is *reasonable*.

**Prerequisites.** Algebra. Scientific notation. Comfort with the idea that *x times some power of ten* is just a way of writing very small or very large numbers without losing your place. Nothing else.

**Why this chapter matters.** Every later chapter calculates something — a force, a charge, an angle, a frequency, a half-life. None of those calculations are trustworthy without the three habits this chapter installs. Skip this chapter and the rest of the book reads like a magic trick. Take it seriously and the rest of the book reads like a discipline.

---

## Concept 1 — What physics actually is

### The dim outline of an atom, 2013

In 2013, a research group at IBM Almaden, working with carbon monoxide molecules on a copper surface and a scanning tunneling microscope, made a stop-motion movie called *A Boy and His Atom*. Each frame is a still photograph of individual atoms — one xenon atom per pixel — pushed into position with the tip of the microscope. There are 242 frames. It is the smallest movie ever made.

What you are looking at, when you watch it, is not a representation of atoms. It is a photograph of atoms. The boy is built from atoms. The "ball" he plays with is one atom. You can see them because the microscope's tip senses the quantum-mechanical tunneling current between itself and each atom on the surface, and that current depends on what atom is there.

A century earlier, no one had ever seen an atom. Atoms were a *model* — a useful mental picture — that explained why gases behaved the way they did, why chemistry combined elements in fixed ratios, why brownian motion looked the way it looked. Now we have movies of them. The model became something we can photograph.

That arc — from useful fiction to photographable fact — is the arc physics aims for, and it is the reason the field draws careful distinctions between models, theories, and laws. They are not synonyms. They occupy different rungs.

### The mechanism — three rungs of generality

A **model** is a mental picture you build because the actual thing is too small, too large, too fast, or too abstract to apprehend directly. Bohr's planetary atom — electrons orbiting a nucleus like planets around a sun — is a model. It is wrong in several technical senses (electrons don't have orbits; they have probability clouds), but it is right in the sense that it lets you predict the spectrum of hydrogen with surprising accuracy. A model is justified by what it lets you compute. Its claim is local. When the model fails — and every model does, eventually — you swap it for one that works in the regime you've moved into.

A **theory** is bigger. It is a body of explanation, supported by many lines of evidence, that accounts for an entire category of phenomena. Newton's theory of gravity explains the fall of an apple, the orbit of the Moon, the tides, the precession of the equinoxes, and the trajectory of a cannonball, all from the same idea: every mass attracts every other mass with a force proportional to the product of the masses and inversely proportional to the square of the distance. A theory's claim is universal within its domain. When experiment contradicts a theory, the theory is either modified (Einstein's relativity refined Newton's gravity at high speeds and large masses) or, if the contradiction is fundamental, replaced.

A **law** is a concise mathematical statement, often expressible as a single equation, that captures a generalization of how nature behaves. Newton's second law,

$$F = ma,$$

is a law. The law of conservation of energy — that energy can change form but is never lost — is a law. Laws are smaller than theories in vocabulary but often larger in reach. The conservation of energy isn't about any specific situation; it's a constraint every situation satisfies.

The boundaries between these are not always sharp. Pascal's principle is sometimes called a principle, sometimes a law. Newton's "laws of motion" form the core of his "theory of mechanics." But the spirit of the distinction is clear enough to be useful: models are pictures you can swap when better ones come along; theories explain whole classes of things; laws are the tightest expressible compressions of regularities in nature.

### The trade-off

The trade physicists make: **simplicity for accuracy, accuracy for scope.** A model is simple but local. A theory is comprehensive but cumbersome. A law is exact within its terms but says nothing about what those terms physically *mean* — Newton's $F = ma$ tells you what force does without telling you what force *is*. The discipline accepts these trade-offs as productive. You reach for the level of generality that fits the question you are actually asking.

### Worked example — what counts as physics, and what doesn't?

Suppose someone tells you they have a "theory of love." Is that the same kind of object as Einstein's theory of relativity?

**Reasoning.** A scientific theory has three features absent from the love theory: (1) it makes predictions specific enough to be wrong; (2) those predictions have been tested across many independent experiments by independent groups; (3) it produces quantitative results that line up with measured values to within some specified uncertainty. The love theory is missing all three. It is using "theory" in the everyday sense — a guess, an idea, a hunch.

This is why scientists wince at "it's just a theory." In everyday English, *theory* means *speculation*. In science, *theory* means the highest-confidence kind of explanation we have. Evolution is *just a theory* in the same sense that gravity is *just a theory*: each is a body of explanation supported by every test ever brought against it. Words drift across contexts. Watch the slippage.

### Common misconceptions

- *"A theory becomes a law when it's proven."* No. They are different objects entirely. A law is a concise mathematical generalization; a theory is the surrounding explanatory structure. Newton's law of gravitation lived inside Newton's theory of mechanics, which lived inside the broader Newtonian worldview. Theories don't graduate into laws; they coexist with them.
- *"Classical physics was wrong, and modern physics is right."* Also no. Classical physics is an excellent approximation when matter moves at less than about 1% of the speed of light, when the objects are larger than a microscope can resolve, and when gravitational fields are weak. Inside those bounds, classical physics is essentially exact. Outside them — at the speed of light, at atomic scales, near a black hole — you reach for relativity or quantum mechanics. Each theory has a *domain of applicability*. Knowing the domain is part of knowing the theory.

↳ **Dig Deeper — Where does Newton's gravity stop being a good description?**

*The chapter argues that classical physics is "essentially exact" inside its domain of applicability. The interesting question is where the boundary actually sits — at what point in the real universe does Newtonian gravity start producing measurably wrong predictions, and what physical scenarios force you to reach for general relativity instead?*

**Prompt:**
> Walk me through three real physical scenarios where Newtonian gravity gives a measurably wrong answer that general relativity gets right: (1) the precession of Mercury's orbit, (2) the rate at which atomic clocks run on GPS satellites versus on the ground, and (3) the bending of starlight near the Sun observed during the 1919 eclipse. For each, name the size of the discrepancy in concrete units, and explain in plain language what physical effect general relativity is capturing that Newtonian gravity misses.

**What to do with the output:** Save it. The pattern — *a successful theory's failures pointing toward the next theory* — recurs in chapters 28 (special relativity) and 29 (quantum mechanics). This is your first encounter.

---

## Concept 2 — How a number gets to mean something

### A vibration in a vacuum, every nine billion times

In 1967, the international scientific community redefined the second.

For most of human history, the second had been a bookkeeping convenience: $\frac{1}{86{,}400}$ of a mean solar day, where 86,400 is the number of seconds in 24 hours. This worked, more or less, until clocks got accurate enough to notice that the solar day itself was not a fixed length. The Earth's rotation is slowing — by tidal friction, by the redistribution of mass after every earthquake. A second defined by the day was a second built on a wobbling foundation.

So they moved the foundation. From 1967 onward, the second has been defined as the time it takes for an undisturbed cesium-133 atom to complete exactly **9,192,631,770** oscillations between two specific energy states. Cesium atoms vibrate at this frequency anywhere in the universe, in any laboratory, at any time. A standard built on cesium isn't tied to the Earth's rotation or to a particular cylinder in a particular vault. It is portable, reproducible, and as accurate as you can build the apparatus to count.

Here is the move physics has been making, for two centuries, with every fundamental unit. Pull the standard off something that drifts (a planet, a metal bar, a metal cylinder) and onto something that doesn't (the speed of light, Planck's constant, the vibration of an atom). The kilogram redefinition of 2019 was the last of the major ones. Every base unit of the SI system is now defined by a constant of nature.

### The mechanism — fundamental and derived units

Most physical quantities — velocity, force, energy, pressure, electric charge, magnetic flux, temperature gradient — turn out to be combinations of just a few **fundamental units**. The SI system uses seven fundamentals; in this textbook we will use four of them constantly:

| Quantity | Unit | Symbol |
|---|---|---|
| Length | meter | m |
| Mass | kilogram | kg |
| Time | second | s |
| Electric current | ampere | A |

Everything else is **derived**. Speed is length divided by time, $\text{m/s}$. Acceleration is length divided by time squared, $\text{m/s}^2$. Force is mass times acceleration, so a newton is $1 \text{ N} = 1 \text{ kg} \cdot \text{m/s}^2$. Energy is force times distance, so a joule is $1 \text{ J} = 1 \text{ kg} \cdot \text{m}^2 / \text{s}^2$. Once you know the fundamentals, the derivation tells you what a unit physically *means*. A joule isn't a magic word; it's the energy required to push with one newton through one meter, which is exactly what its dimensional decomposition says it is.

This is why dimensional analysis is so powerful. If your final answer for an energy comes out with units of $\text{kg} \cdot \text{m} / \text{s}$ — that's momentum, not energy — you know, before checking a single number, that you've made an algebra mistake somewhere. The units are a parallel proof that the calculation is right.

### The metric prefixes — leverage across thirty-six orders of magnitude

The SI system has another feature you should not undersell: every unit can be scaled by a power of ten using a fixed set of prefixes. A nanometer is $10^{-9}$ meters; a gigahertz is $10^9$ hertz; a femtosecond is $10^{-15}$ seconds. The prefixes run from atto ($10^{-18}$) to exa ($10^{18}$) — thirty-six orders of magnitude in a single coherent system. There is no "1,728 cubic inches per cubic foot" memorization tax. There is no separate king's foot and standard foot. There is no system of measurement for chemists and another for cooks.

Compare this to U.S. customary units, which have served the United States well at the cost of inheriting some peculiar arithmetic. Twelve inches per foot. Three feet per yard. 1,760 yards per mile. Sixteen ounces per pound. Two pints per quart, four quarts per gallon, but the U.S. gallon is not the same as the imperial gallon. Each conversion requires a number you have to look up. Every metric conversion requires only a count of zeros.

### The trade-off

The trade SI made: **easy arithmetic for cultural inertia.** A country that switches to SI gives up the embedded familiarity of inches and pounds — the way a six-foot-one person knows what their height *feels* like. SI gains the ability to do every calculation in the same coherent system without the friction of memorized conversion factors. For science, the trade is unambiguously worth it. Every other country in the world has made the switch.

### Worked example — the unit-cancellation method

Suppose you want to convert an average speed of $30.0 \text{ km/h}$ into meters per second. Don't memorize a conversion factor. Build it.

We want to cancel kilometers and replace them with meters; we want to cancel hours and replace them with seconds. Set up the calculation as a chain of multiplications, where each fraction has the unit you want to *cancel* on the bottom and the unit you want to *keep* on top:

$$30.0 \frac{\text{km}}{\text{h}} \times \frac{1{,}000 \text{ m}}{1 \text{ km}} \times \frac{1 \text{ h}}{3{,}600 \text{ s}} = 8.33 \frac{\text{m}}{\text{s}}.$$

Notice what happened. The "km" on top of the first term cancels the "km" on the bottom of the second. The "h" on the bottom of the first term cancels the "h" on the top of the third. Whatever remains uncancelled is your answer's units — meters on top, seconds on the bottom.

**Sanity check.** A car going $30 \text{ km/h}$ — that's about $19 \text{ mph}$ — covers something like one car-length per second, where a car is about three meters. Eight or nine meters per second is close enough to that estimate to be obviously correct. If your answer had been $0.83$ or $83$ instead of $8.33$, you would have known immediately that you had inverted a conversion factor. The order of magnitude is your friend.

**The general lesson.** Always treat units as algebraic quantities that obey the rules of multiplication and division. They cancel just like variables. If you set up the calculation right, the units carry the proof of correctness. If your final answer has units you didn't expect, you have made a structural error — and you should fix the structure before fiddling with the arithmetic.

### Common misconceptions

- *"The kilogram is a unit of weight."* It is a unit of mass. Weight is the force that gravity exerts on a mass: $W = mg$. On Earth, the weight of a 1-kg mass is about $9.8 \text{ N}$. On the Moon, the same 1-kg mass weighs about $1.6 \text{ N}$ — different weight, same mass. The English unit *pound* is a unit of force, not mass, which is part of why mixing the two systems leads to so many freshman lab errors.
- *"Conversion factors only work in one direction."* No. $1 \text{ km} = 1{,}000 \text{ m}$ can be read as $\frac{1{,}000 \text{ m}}{1 \text{ km}}$ or as $\frac{1 \text{ km}}{1{,}000 \text{ m}}$, depending on which unit you need to cancel. The conversion factor is a *ratio*, and a ratio equal to 1 can be flipped without changing its value.

↳ **Dig Deeper — How is the kilogram actually realized today?**

*The chapter said the kilogram is now defined by Planck's constant. But "defined by" and "physically realized as" are different things. There is a real instrument — the Kibble balance — that turns the abstract definition into a concrete measurement of mass. Understanding how it works opens up surprisingly deep physics about the relationship between mechanical and electromagnetic forces.*

**Prompt:**
> Explain how a Kibble balance works to physically realize the kilogram from Planck's constant. Walk me through the two phases (the weighing mode and the velocity mode), the physics in each (the balance of gravitational force against an electromagnetic force; the induction of voltage by motion through a magnetic field), and how the two phases combine to extract a mass measurement. Include rough numbers — what kind of currents and voltages are involved, what kind of precision is achieved.

**What to do with the output:** Save it. The Kibble balance is a beautiful piece of metrology that quietly relies on quantum mechanics (the Josephson and quantum Hall effects). Re-read it after Chapter 22 (magnetism) and Chapter 29 (quantum mechanics) — it will read differently.

---

## Concept 3 — Honest numbers

### A bag of apples at the grocery store

You buy a 5-pound bag of apples. You weigh it on your kitchen scale. It reads 5.1 pounds. You buy three more bags over the next three weeks. They read 4.8, 4.9, and 5.4 pounds. The label on each bag says "5 lb."

Were you cheated? Were the apples mismeasured at the grocery? Or is the variation just *what measurement is*?

The honest answer is the third one. Every measurement comes with an irreducible scatter. The scale has a smallest reading; the apples are heterogeneous; the person doing the weighing has limited eyesight and patience. You did not measure 5.1 pounds. You measured $5.1 \pm \delta$ pounds, where $\delta$ is the uncertainty — a quantitative statement of how much your number might be off. Without the $\delta$, the 5.1 is half the story. *Every measurement carries an uncertainty, and stating only the central value is a form of dishonesty by omission.*

This concept is what separates a physics calculation from a guess. Not the precision of the central value. The honesty about the spread.

### The mechanism — accuracy, precision, and uncertainty

These three words are routinely confused in everyday speech. In physics they are distinct.

**Accuracy** is how close your measurement is to the true value. Measure an 11.0-inch stick. If you get 11.1, 11.2, and 10.9 inches across three trials, your measurements are accurate — they cluster around the true value. If you got 12.0 inches all three times, you would be precise but not accurate.

**Precision** is how close your repeated measurements are to *each other*. The 12.0, 12.0, 12.0 case is precise (no spread) and inaccurate (wrong center). The 10.5, 11.0, 11.5 case is accurate (right center on average) and imprecise (large spread). You can have either without the other.

**Uncertainty** is the formal quantitative statement of how confident you are in a measurement. Written as $A \pm \delta A$. The 11-inch stick measured with a millimeter ruler might be reported as $11.0 \pm 0.05$ inches.

What feeds the uncertainty in any real measurement:

- The smallest division on the measuring device. A stopwatch with $\pm 0.01$ s resolution cannot tell you anything tighter than that.
- The skill of the person doing the measurement.
- Real variation in the thing being measured (the apples are not all the same).
- Environmental factors — temperature, vibration, lighting.

A measurement without an uncertainty is a measurement without a claim. *"My car gets 28 miles per gallon"* with no uncertainty might mean $28 \pm 1$ or $28 \pm 8$. Without knowing which, you cannot decide whether the measurement is even useful.

### Percent uncertainty

When uncertainties get compared across measurements with very different magnitudes — a kilometer with a centimeter uncertainty, a gram with a microgram uncertainty — it helps to express the uncertainty as a fraction of the measurement itself:

$$\text{\%unc} = \frac{\delta A}{A} \times 100\%.$$

So our apple bag, with $A = 5.1 \text{ lb}$ and $\delta A = 0.4 \text{ lb}$ (the spread we measured), has

$$\text{\%unc} = \frac{0.4}{5.1} \times 100\% \approx 8\%.$$

A measurement with 8% uncertainty is fine for buying apples and useless for surveying property lines. Whether an uncertainty is *acceptable* is always a question about what the measurement is *for*.

### Propagating uncertainty through a calculation

Here is the move that most distinguishes a physicist from a casual user of arithmetic. When you multiply or divide measured quantities, you have to propagate the uncertainty into the answer. The simplest rule, accurate when uncertainties are small (a few percent or less):

**The percent uncertainty in a quantity calculated by multiplication or division is the sum of the percent uncertainties in the input quantities.**

Example. A floor measures $4.00 \text{ m}$ long with 2% uncertainty and $3.00 \text{ m}$ wide with 1% uncertainty. The area is $A = L \times W = 12.0 \text{ m}^2$. The uncertainty:

$$\text{\%unc}_A = 2\% + 1\% = 3\%.$$

Convert that back to absolute units: $3\%$ of $12.0 \text{ m}^2$ is $0.36 \text{ m}^2$, which we round to $0.4 \text{ m}^2$ to match the precision of the inputs. The honest report is $A = 12.0 \pm 0.4 \text{ m}^2$.

Notice what this rule does. It tells you that uncertainty *grows* as you compound measurements. A calculation with five measured inputs will have an uncertainty larger than any single input. If you want a precise final answer, every input has to be precise — and you cannot make up precision the inputs do not have.

### Significant figures — uncertainty's bookkeeping shorthand

Significant figures are how you encode uncertainty in the way you write a number. The convention: *the last digit you write is the first digit that has any uncertainty*. A measurement of $36.7 \text{ cm}$ on a millimeter ruler has three significant figures because the millimeter digit (the 7) is the one you had to estimate.

The two governing rules for calculations:

**For multiplication and division:** the result should have the same number of significant figures as the input with the *fewest* significant figures.

So $\pi \times r^2$ with $r = 1.2 \text{ m}$ (two sig figs) gives, on the calculator, $4.5238934 \text{ m}^2$. But the input has only two sig figs, so the answer is

$$A = 4.5 \text{ m}^2.$$

Reporting eight digits implies a precision your input did not have.

**For addition and subtraction:** the result has no more decimal places than the input with the *fewest* decimal places.

So $7.56 \text{ kg} - 6.052 \text{ kg} + 13.7 \text{ kg}$ on the calculator is $15.208 \text{ kg}$. But the $13.7 \text{ kg}$ input is precise only to the tenths place, so the answer rounds to

$$15.2 \text{ kg}.$$

A note on zeros, which is where most students first stumble. Zeros that mark a decimal place are *not* significant: $0.053$ has two sig figs (the 5 and the 3). Zeros between significant digits *are* significant: $10.053$ has five. Trailing zeros in a number without a decimal point are ambiguous — $1{,}300$ might have two, three, or four. Write it in scientific notation ($1.3 \times 10^3$ or $1.300 \times 10^3$) to remove the ambiguity.

### The trade-off

The trade significant-figure rules make: **convenience for honesty.** Reporting fewer digits costs you the satisfaction of writing down everything your calculator displayed. It buys you a number that does not lie about its own precision. The convenience is small; the honesty matters.

### Approximation — when a rough answer is the right answer

There is a separate skill physicists develop, and it is worth naming explicitly: the order-of-magnitude estimate, sometimes called a *Fermi problem* after Enrico Fermi, who was famous for them. The point is to get an answer that is right within a factor of ten without doing any precise measurement at all.

**Worked example — the height of a 39-story building.**

You don't have a measuring tape. You don't know the building. But you know the average height of an adult is roughly 2 meters, and one story of a building is roughly the height of two adults stacked end to end (a generous overhead, allowing for floor structure). So:

$$\text{height} \approx \frac{2 \text{ m}}{1 \text{ person}} \times \frac{2 \text{ persons}}{1 \text{ story}} \times 39 \text{ stories} = 156 \text{ m}.$$

The answer is good to within a factor of two, certainly within a factor of ten. That is enough for most decisions ("can a fire ladder reach this floor?") and certainly enough for sanity-checking a more elaborate calculation.

The discipline of estimation is what tells you when a precise calculation has gone off the rails. If the formal calculation says the building is $1{,}560 \text{ m}$ tall, you know — without re-doing the arithmetic — that something is wrong, because nothing in your back-of-envelope sanity check produced anything close to that. The estimate is a guardrail.

### Common misconceptions

- *"Significant figures are about how many digits the calculator shows."* The calculator shows whatever the digital display can fit. Significant figures are about which of those digits *mean* something — that is, which are tied to a measurement and which are computational artifacts. Always round to honor the precision of your inputs.
- *"More precise is always better."* Sometimes precision is the wrong question. If you are estimating whether a 39-story building is taller than a fire ladder can reach, knowing the height to the nearest meter is overkill. The right precision is the one the decision requires, not the one your instrument can deliver.

↳ **Dig Deeper — Beyond percent uncertainty: the propagation by quadrature**

*The chapter taught the "method of adding percents" as a simple-but-conservative rule for combining uncertainties through multiplication and division. The more honest rule, used in laboratory physics and engineering, treats uncertainties as statistically independent and combines them in quadrature (sum of squares). This produces tighter, more accurate uncertainty estimates — and reveals when uncertainties are actually correlated.*

**Prompt:**
> Explain the difference between (a) the simple "method of adding percents" used in this chapter and (b) the more rigorous "propagation by quadrature" used in laboratory physics. Show with one worked example — say, computing the volume of a rectangular box from three measured side lengths — how the two methods give different uncertainty estimates, and explain when each is appropriate. Then briefly note what changes when the input uncertainties are correlated rather than independent.

**What to do with the output:** Save it. This is the next-level uncertainty rule you will need in any physics laboratory course. The quadrature method also generalizes cleanly to addition/subtraction (where the simple method does not) — ask Claude to walk through that case as a follow-up if you're interested.

---

## Synthesis — the discipline these three concepts make together

Step back and look at what you've just walked through. Three commitments:

1. **Nature has discoverable order.** The whole game starts with the bet that careful observation, controlled experiment, and mathematical generalization can produce models, theories, and laws that predict outcomes nobody has yet measured. Without that bet, none of the rest of physics is worth doing.

2. **Every quantity must be tied to a defensible unit.** The SI system is the discipline of writing down what each of your numbers physically *means* by tying them to a small set of fundamental units, each of which is in turn tied to a constant of nature. The meter, the second, the kilogram, the ampere — anywhere in the universe, with sufficient apparatus, you can construct one of each.

3. **Every number must carry its own uncertainty.** The discipline of significant figures, the propagation of uncertainty through calculations, the order-of-magnitude estimate as sanity check — these are how a physicist tells you not just *what* they measured but *how well* they measured it.

These three commitments are not separate. They braid. The reason the kilogram had to be redefined in 2019 — the reason that small lump of platinum-iridium near Paris had to be retired — is that the existing definition could no longer support the precision modern measurements demanded. The cylinder was changing by tens of micrograms over decades, which is unacceptable when you are trying to measure mass to one part in $10^9$. The redefinition lifted the kilogram off the cylinder and onto Planck's constant precisely because the universe respects Planck's constant in a way it does not respect a piece of metal.

This is the **scale shift** I want you to feel. Down at the level of the cesium atom, oscillating $9{,}192{,}631{,}770$ times every second. Up at the level of the international community of metrologists voting on what the kilogram shall be from this moment forward. The seemingly mundane task of agreeing on units is, when examined closely, one of the deepest acts of cooperation our species engages in. Every measurement you make in a laboratory anywhere on Earth is comparable to every measurement in every other laboratory on Earth because of agreements like this one. The science is collaborative all the way down to its definitions.

### A worked example using all three concepts — the speed of a tectonic plate

Consider a tectonic plate moving with an average speed of $4.0 \text{ cm/year}$. Two questions a geologist might ask:

(a) How far does it move in one second?

(b) What is its speed in kilometers per million years?

For (a), apply unit cancellation:

$$4.0 \frac{\text{cm}}{\text{yr}} \times \frac{1 \text{ m}}{100 \text{ cm}} \times \frac{1 \text{ yr}}{3.16 \times 10^7 \text{ s}} = 1.3 \times 10^{-9} \text{ m} \text{ per second}.$$

That is roughly the diameter of a few atoms. Per second.

For (b),

$$4.0 \frac{\text{cm}}{\text{yr}} \times \frac{1 \text{ km}}{10^5 \text{ cm}} \times \frac{10^6 \text{ yr}}{1 \text{ My}} = 40 \frac{\text{km}}{\text{My}}.$$

Forty kilometers per million years. The same rate of motion, expressed in two units, looks completely different — atomic-scale per second, continental-scale per geological epoch. The physics is identical. Only the bookkeeping changed.

Notice the input — $4.0 \text{ cm/year}$ — has two significant figures. So the answer should also have two: $1.3 \times 10^{-9} \text{ m/s}$ and $40 \text{ km/My}$. Reporting $1.265823 \times 10^{-9} \text{ m/s}$ would be inventing precision the input does not have.

This is what the discipline looks like in action: a unit conversion that makes the same physical fact legible at two different scales, with significant figures preserving the honest precision of the input. Three concepts, one calculation, one cleanly defensible answer.

---

## Exercises

The exercises graduate. The warm-ups check that you can apply a single concept mechanically. The applications force translation. The synthesis exercises ask you to combine concepts. The challenges point past the chapter's edges.

### Warm-up

**1.1** *(LO 1)* In your own words, distinguish a model from a theory from a law. Give one physics example of each that is *not* gravity.

**1.2** *(LO 2)* Express the following measurements in scientific notation, with the indicated SI prefix substituted: $1{,}500$ meters in km; $0.0042$ seconds in ms; $7{,}300{,}000{,}000$ hertz in GHz; $0.000000056$ meters in nm.

**1.3** *(LO 3)* Determine the number of significant figures in each: $0.0009$; $15{,}450.0$; $6 \times 10^3$; $87.990$; $30.42$.

**1.4** *(LO 4)* The speed limit on some interstate highways is roughly $100 \text{ km/h}$. (a) What is this in $\text{m/s}$? (b) What is this in miles per hour? (Use $1 \text{ km} = 0.6214 \text{ mi}$.)

### Application

**1.5** *(LO 4)* A car speedometer has a 5.0% uncertainty. (a) What is the range of possible speeds when it reads $90 \text{ km/h}$? (b) Convert this range to miles per hour. ($1 \text{ km} = 0.6214 \text{ mi}$.)

**1.6** *(LO 4)* The sides of a small rectangular box are measured to be $1.80 \pm 0.01 \text{ cm}$, $2.05 \pm 0.02 \text{ cm}$, and $3.1 \pm 0.1 \text{ cm}$ long. Calculate its volume and its uncertainty, expressed in cubic centimeters.

**1.7** *(LO 5)* A friend claims to have run a marathon ($42.188 \text{ km}$) in $2$ hours, $30$ minutes, and $12$ seconds. Estimate her average speed in $\text{m/s}$ — do this in your head before pulling out a calculator, then check against a precise calculation. By how much did your estimate miss?

**1.8** *(LO 1, LO 2)* Newton's gravitational force between two point masses is $F = G \frac{m_1 m_2}{r^2}$, where $G$ is a constant. Without computing anything, work out what units $G$ must have for the equation to be dimensionally consistent (i.e., for the right-hand side to come out in newtons). What does this tell you about $G$?

### Synthesis

**1.9** *(LO 3, LO 4)* You weigh yourself five times in succession on a digital bathroom scale and get readings of $72.1$, $72.3$, $72.0$, $72.2$, and $72.4 \text{ kg}$. The scale's resolution is $\pm 0.1 \text{ kg}$. Report your weight as $\bar{m} \pm \delta m$, justifying your choice of $\delta m$ — is it the resolution, the spread, or some combination?

**1.10** *(LO 1, LO 4)* Suppose a rival theory of gravity predicts that, near the surface of Earth, $g = 9.85 \pm 0.05 \text{ m/s}^2$, where the standard value is $9.81 \text{ m/s}^2$. Is this prediction consistent with experiment? (You will need to look up the experimental uncertainty on $g$.) Explain what *consistent* means in this context.

**1.11** *(LO 5)* Estimate the number of heartbeats in a human lifetime. State your reasoning, and bracket your answer with an upper and lower estimate. Compare to the OpenStax sample answer of $2 \times 10^9$ — does your reasoning produce a similar number?

### Challenge

**1.12** *(LO 1, beyond chapter)* The kilogram was redefined in 2019 to be tied to Planck's constant rather than to a specific cylinder of metal. Why does it matter that the kilogram is now defined in terms of a constant of nature rather than an artifact? Construct an argument that addresses both the practical (precision, drift) and the philosophical (what does "one kilogram" *mean*?) sides of the question.

**1.13** *(LO 5, beyond chapter)* Estimate the total number of atoms in your body. State your input assumptions; show the chain of estimates; report your final answer to one significant figure. (Hint: start from the mass of a person and the mass of an "average" atom in the body, which is roughly the mass of a hydrogen atom times 10 — most of you is hydrogen, oxygen, and carbon.)

---

## LLM Exercise — Chapter 1: Anchor Quantity for the Reality Check Logbook

**Project:** Physics Reality Check Logbook
**What you're building this chapter:** Your project's first entry — one anchor quantity, measured or sourced honestly, with units, significant figures, and an explicit uncertainty.
**Tool:** Claude Project (the same one you set up in Chapter 00).

### The Prompt

```
I'm building a Physics Reality Check Logbook for College Physics with LLMs. Each chapter contributes one entry analyzing a real-world physical phenomenon using that chapter's physics. For Chapter 1, the entry tests my ability to report a measured quantity honestly — with proper units, significant figures, and uncertainty.

I want my anchor phenomenon for this whole logbook to be: [paste a 1-sentence description of the phenomenon you'll track across the book — e.g., "the daily commute by bicycle from my apartment to campus," "the operation of my coffee maker," "the trajectory of a basketball shot from the free-throw line," "the energy budget of running a marathon"].

For Chapter 1, please:

1. Identify ONE quantitative property of this phenomenon that I should measure or source carefully (e.g., for the bike commute: the elevation gain in meters; for the coffee maker: the steady-state operating temperature in Celsius). Explain why this quantity is foundational for the analyses that will follow in later chapters.

2. Tell me where I would source this number from primary references vs. measure myself, and what kind of uncertainty I should expect from each path.

3. Show me how to report it correctly: value ± uncertainty, with proper units and significant figures.

4. Walk through one Fermi-style sanity check I can do mentally to verify the number is in the right order of magnitude.

5. Identify two ways the number could mislead me later (e.g., variability across measurements, dependence on conditions I didn't record).

Be specific to my chosen phenomenon. Don't give me a generic "uncertainty 101" answer.
```

### What this produces

A one-page Logbook entry — your first — that establishes the phenomenon you'll track across the book. The entry includes one carefully sourced number with explicit uncertainty, a Fermi-check, and two named pitfalls for future chapters. Save as `logbook/chapter-01-anchor.md` (or your preferred filename convention).

### How to adapt this prompt

- *For your chosen phenomenon:* Replace the bracketed description with the phenomenon you'll track for the whole book. Picking it well now matters — you'll come back to it 33 more times.
- *For ChatGPT or Gemini:* Works identically. Replace "Claude Project" with "Custom GPT" or "Gemini Gem" for setup, but the prompt itself transfers.
- *For a more code-heavy approach:* If you have measurement data (a fitness tracker recording your bike commute, a thermocouple log from your coffee maker), use Claude Code instead — paste the data and ask Claude to compute the mean and standard deviation, then report properly.

### Connection to previous chapters

Builds on Chapter 00's project setup. The Claude Project you created in Chapter 00 should now hold both the project foundation document and this Chapter 1 anchor entry.

### Preview of next chapter

Chapter 2 introduces kinematics — position, velocity, acceleration. The Chapter 2 LLM Exercise will ask you to extract one kinematic property of your chosen phenomenon (a speed, an acceleration, a stopping distance) using the equations of motion, and add it as the second entry in your Logbook.

---

## Chapter summary

Physics is the science of describing the interactions of energy, matter, space, and time. It begins with a bet — that nature is orderly enough to be modeled, theorized, and lawfully described — and proceeds by demanding two disciplines of every claim: that every quantity be tied to a defensible unit, and that every number carry an honest statement of how well it is known.

The one idea that matters most: **physics earns its results by being more careful about its words and numbers than other disciplines.** When a physicist says "the cesium-133 atom oscillates at $9{,}192{,}631{,}770$ Hz," the precision is the point. When a physicist says "$F = ma$," the equation is shorthand for an enormous body of confirmed prediction. When a physicist says "this measurement is $5.1 \pm 0.4 \text{ kg}$," the $\pm$ is part of the claim. Strip the precision, and you are no longer doing physics.

The common mistake to watch for: **treating significant figures as a stylistic choice rather than a quantitative claim.** Reporting $4.5238934 \text{ m}^2$ when your input has two significant figures is not just imprecise — it is dishonest about what you actually know. The number of digits is the claim.

What you should now be able to teach someone else: how to convert between units fluently using the cancellation method; how to propagate uncertainty through a multiplication or division using the percent-addition rule; how to make a Fermi-style estimate that is good to within a factor of ten and use it to sanity-check a more elaborate calculation. If you can teach those three things to a friend, in your own words, with your own examples, you have understood this chapter.

---

## What would change my mind

The chapter argues that the SI system's coupling of every fundamental unit to a constant of nature — the kilogram to Planck's constant, the meter to the speed of light, the second to the cesium hyperfine transition — represents a strict improvement over artifact-based definitions. The argument would need revision if a future redefinition demonstrated that one of these "constants" was itself drifting at a precision relevant to measurement, requiring yet another reformulation.

## Still puzzling

The deepest unresolved question this chapter raises and does not answer: *why* the universe is so cooperative — why the same set of mathematical regularities work in a physics lab in Boston and in the atmosphere of a star $10$ billion light-years away. We can demonstrate the cooperation. We can even, in some cases, derive one regularity from a deeper one. But the meta-question — *why does nature have such order at all?* — sits at the edge of what physics can address. Eugene Wigner, in 1960, called it "the unreasonable effectiveness of mathematics in the natural sciences." The puzzle has not gone away.

---

## Connections forward

Chapter 2 introduces **kinematics** — the geometry of motion. With the discipline of units, uncertainty, and significant figures installed, you will spend the next chapter making position, velocity, and acceleration *precise* in the same way this chapter made measurement itself precise. Chapter 3 extends to two-dimensional motion (projectiles, angled trajectories), and Chapter 4 introduces *forces*, completing Newton's mechanics. Every numerical answer you produce in those chapters will lean on the habits this chapter installs.

There is a deeper arc you should be aware of. The book begins in the regime where classical physics is essentially exact — the everyday world of cars and balls and pulleys. As we move forward, we will eventually press on the boundaries of that regime and meet the conditions where classical physics breaks down: the very fast (Chapter 28: special relativity), the very small (Chapter 29: quantum mechanics), and the structure of matter at scales where neither classical nor quantum descriptions alone are adequate (Chapters 30-33). At each of those transitions, the work this chapter installed — caring about what your units mean, caring about what your uncertainties are — becomes more important, not less. The discipline scales.

---

**Tags:** measurement, SI-units, significant-figures, uncertainty, scientific-method

---

## AI Wayback Machine

**Ibn al-Haytham** wrote *Kitāb al-Manāẓir* (Book of Optics) around 1021 — establishing experimental method centuries before its European rediscovery. He insisted that light travels in straight lines, enters the eye rather than emanating from it, and that experiment must validate theory.

**Run this:**

```
Who was Ibn al-Haytham, and how does his work connect to the nature of science we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Ibn al-Haytham"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to describe one of Ibn al-Haytham's optical experiments in the *Book of Optics*.
- Ask it about how Ibn al-Haytham came to write the book during his decade under house arrest in Cairo.

What changes? What gets better? What gets worse?
