# Physics +1: Classical Mechanics

**Author:** Nik Bear Brown
**Series:** Physics +1 (Volume 1)
**Publisher:** Bear Brown, LLC
**Status:** Draft

---

## About this book

*Classical mechanics as the physics you can verify against lived experience.* This is the foundation volume of the Physics +1 series: throw a ball, watch the trajectory, check the simulation. The book starts from kinematics — position, velocity, acceleration — and earns its way to rotational dynamics, fluid flow, and wave behavior. Every concept is forced to be specific before it is used, every mechanism explained from first principles, every analogy tested for whether it illuminates or merely decorates.

The +1 layer is interactive: D3 simulations are paired with each chapter — a position–velocity–acceleration live plotter, a free-body-diagram builder, a 1D collision sandbox, a figure-skater angular-momentum simulator, a Bernoulli flow visualizer. The simulations are the bridge between equation and intuition; the prose makes the machinery visible.

Audience: first-year physics students and curious autodidacts comfortable with high-school algebra and elementary calculus. The 19 source chapters in `chapters/` cover the standard classical-mechanics sequence (drawn from OpenStax College Physics and University Physics); `outline.md` proposes a curated 14-chapter subset for the published volume.

## How this directory is organized

```
book.md              ← one-sentence pitch, argument, gap, reader, high-level outline (planning)
outline.md           ← working TOC with D3 simulation notes per chapter
vision.md            ← Tic TOC Phase 1: vision and positioning
architecture.md      ← Tic TOC Phase 2: learning architecture
chapters-spec.md     ← Tic TOC Phase 3: per-chapter specifications
risks.md             ← Tic TOC Phase 4: scope, comparables, adoption risks
pantry/              ← scratch storage for fragments and snippets
chapters/            ← drafts (this is where the book lives)
images/              ← figures and hero images per chapter
styles/              ← Kindle-bound CSS (shared base + book-specific overrides)
build.sh             ← compile the EPUB
graphs.sh            ← process figure-placeholder comments into images/tables
```

## Detailed Table of Contents

### Front Matter

| File | Section |
|------|---------|
| `chapters/00-frontmatter.md` | Title page, copyright, dedication, preface |
| `chapters/00b-introduction.md` | Book-level introduction (template placeholder) |

### Chapters

| # | File | Title |
|---|------|-------|
| 1 | `chapters/01-introduction-the-nature-of-science-and-physics.md` | The Nature of Science and Physics |
| 2 | `chapters/02-what-is-physics.md` | What is Physics? |
| 3 | `chapters/03-kinematics.md` | Kinematics |
| 4 | `chapters/04-motion-in-one-dimension.md` | Motion in One Dimension |
| 5 | `chapters/05-two-dimensional-kinematics.md` | Two-Dimensional Kinematics |
| 6 | `chapters/06-dynamics-force-and-newton-s-laws-of-motion.md` | Dynamics: Force and Newton's Laws of Motion |
| 7 | `chapters/07-further-applications-of-newton-s-laws-friction-drag-and-elasticity.md` | Further Applications of Newton's Laws: Friction, Drag, and Elasticity |
| 8 | `chapters/08-uniform-circular-motion-and-gravitation.md` | Uniform Circular Motion and Gravitation |
| 9 | `chapters/09-work-energy-and-energy-resources.md` | Work, Energy, and Energy Resources |
| 10 | `chapters/10-linear-momentum-and-collisions.md` | Linear Momentum and Collisions |
| 11 | `chapters/11-momentum.md` | Momentum: The Physics of Collision |
| 12 | `chapters/12-statics-and-torque.md` | Statics and Torque |
| 13 | `chapters/13-rotational-motion-and-angular-momentum.md` | Rotational Motion and Angular Momentum |
| 14 | `chapters/14-fluid-statics.md` | Fluid Statics |
| 15 | `chapters/15-fluid-dynamics-and-its-biological-and-medical-applications.md` | Fluid Dynamics and Its Biological and Medical Applications |
| 16 | `chapters/16-waves-and-their-properties.md` | Waves and Their Properties |
| 17 | `chapters/17-sound.md` | Sound: Pressure Waves and Perception |
| 18 | `chapters/18-oscillatory-motion-and-waves.md` | Oscillatory Motion and Waves |
| 19 | `chapters/19-physics-of-hearing.md` | Physics of Hearing |

### Back Matter

| File | Section |
|------|---------|
| `chapters/99-back-matter.md` | Acknowledgments, About the Author, References, Index |

## Notes on the chapter set

Several pairs cover the same topic from different source textbooks (e.g., ch. 3 *Kinematics* and ch. 4 *Motion in One Dimension*; ch. 10 *Linear Momentum and Collisions* and ch. 11 *Momentum*). They are kept as parallel drafts for now — the curated published outline (see `outline.md`) collapses each pair to a single chapter.

## Build

```bash
./build.sh
```

Output lands in `output/` (gitignored).

## Figures

```bash
./graphs.sh
```

Processes `<!-- → [TYPE: description] -->` comments throughout the chapters:
tabular figures become classed markdown tables; non-tabular figures become
placeholder images in `images/`, ready to replace; CSS log appends to
`styles/kindle-book.css` on each run.

## Publish

Upload `output/physics-plus-one-classical-mechanics.epub` to [KDP](https://kdp.amazon.com).
