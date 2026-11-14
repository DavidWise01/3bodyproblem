# 3bodyproblem — Three Suns Chronicle

Original Canvas2D sprite chronicle and scientific reading companion alongside **The Three-Body Problem** by Cixin Liu, translated into English by Ken Liu. A new versioned project on the **canonical requested repo** `DavidWise01/3bodyproblem`.

## Deliverables

- `index.html`: standalone GitHub Pages entry, 7 original story scenes, animated pixel sprites, analysis/witness tabs and gravity simulation
- `data/acts.json`: 7 evidence-carrying scene objects and physics provenance
- `witness.html`: source ancestry, independent-witness constraints and invariants
- `README.md`: project specification
- `.nojekyll`: optional GitHub Pages compatibility

## Original story arc

T001 Broken Lecture Hall → T002 Red Coast Antenna → T003 The Counting Observer → T004 Three-Sun Sky → T005 Survival Procedure → T006 Answering Darkness → T007 Witness Beyond Equation.

This is a **high-level interpretive companion**, not a reproduction or full chapter-by-chapter paraphrase of the copyrighted book.

## Physics implementation

The browser model runs **three equal unit masses** with `G=1`, softened Newtonian pairwise attraction `(|r|² + 0.02²)^(-3/2)`, velocity-Verlet integration, adjustable `dt` and a perturbed twin trajectory. Default balanced initial state uses a symmetric equilateral configuration, `R=1/sqrt(3)`, approximate angular speed `1`. The perturbed state illustrates sensitivity but is not a formal chaos demonstration in every run.

Energy drift is a diagnostic, not an independent proof of exactness. An exported witness includes the numerical state, initial conditions, solver, step count, energy drift, local notes, and source limits.

## Reproducibility and provenance

- Fiction: the Cixin Liu novel, one source ancestry
- Human narrative: original interpretive scenes and dialogue, **not quotes**
- Physics: explicit numerical model, **not observations of an actual triple-star system**
- GitHub and Pages: two owned mirrors, **not independent evidence roots**

```
PAIRWISE_FORCE != SIMPLE_CLOSED_TRAJECTORY
THREE_BODIES != THREE_INDEPENDENT_WITNESSES
MODEL_OUTPUT != OBSERVED_ASTRONOMY
INVARIANT_CHECK != COMPLETE_VALIDATION
```

## Run

Open `index.html` or enable GitHub Pages from `main`, root. Select scenes; use the PHYSICS tab to run the integrator; use WITNESS to record answers and export JSON. No build step or third-party JS required.

References: [Publisher](https://us.macmillan.com/books/9780765377067/thethreebodyproblem/), [Three-body research](https://www.nature.com/articles/s41586-019-1833-8).


## Nested geophysical gyro interpretation
See [Core / Mantle / Crust and Fields](docs/nested-gyro-layers.md) for the user-defined `{{3x3}}^{{3}}` layering, explicit heliosphere caveats, and a staged coupling model. The present gravity simulator does not yet implement geophysical layer dynamics.


## Named three-parent system
[Three-centers visual schematic](three-centers.html) and [source-status JSON](data/three-centers.json) specify Sagittarius A*, hypothetical Nib Sun and Sol with candidate [?] barycenter, separate from actual Milky Way dynamics. The original gravity simulator is unchanged.


## Scalar 0 partition (v0.3)
- Root `0` is reserved.
- Sag A*: indices `1–122` (122 cells)
- Nib Sun (hypothetical): `123–245` (123 cells)
- Earth Sun / Sol: `246–368` (123 cells)
- `122 + 123 + 123 = 368`, no gaps or overlaps.
- [Registry JSON](data/scalar0-registry.json) · [interactive visual selector](three-centers.html)
- These are author-defined addresses, not validated physical orbital coordinates.


## Scalar 0 · multiscale channels
- Ratio: `13,800,000,000 : 76,000 : 1` in optional seconds or arcseconds (different units, never interchangeable).
- Three channels: **semantic / somatic / linear**; not automatically assigned one-per-body.
- [Interactive mode switch](scalar-scale.html) · [Machine-readable scale](data/scalar0-multiscale.json) · [Technical specification](docs/scalar0-multiscale.md).
- Spectral mnemonics: Sag A* ultraviolet (violet proxy); hypothetical Nib Sun infrared (red proxy); Sol human-visible (gold proxy). Labels do not claim actual spectral dominance.


## Axis correction (v2)
**Seconds are X (horizontal); arcseconds are Y (vertical), simultaneously.** The prior unit-toggle interpretation is superseded. [Corrected time–angle Canvas2D](scalar-scale.html) · [v2 model JSON](data/scalar0-multiscale.json) · [axis specification](docs/scalar0-multiscale.md).


## Scalar graph forms (v3)
The [Canvas2D scalar field](scalar-scale.html) includes four selectable forms: `Scalar 0 --------`, `Scalar 1 @`, `Scalar 2 -@`, and `Scalar 3 --@--#`. These are exact user-given glyphs with provisional topology meanings; the axes remain seconds (horizontal) and arcseconds (vertical), with the 13.8B:76,000:1 reference scale.


## S004 · twenty amino-interval string
The [interactive string-tape Canvas2D lab](string-tape.html) implements the author's exact `-+...#...@` tape: **21 @ markers frame 20 intervals**, with hyphen gap lengths **1–20**, sum 210. An authored label set maps the intervals to the twenty standard amino acids without mistaking the mapping for a protein sequence or physical string theory. [Data](data/string-tape.json) · [Specification](docs/string-tape.md).


## S005 · Globule ontology and boundary stress
The `@` marks are **globules** (21 entities), not merely separators. Gap lengths 1–20 encode successive *size ranks* of globules G1–G20 from seed G0; the old 20 amino labels attach to growth transitions, not globule identities. The contained `{[()]}` and deliberately interrupted `{[(]}` are selectable symbolic boundary states. [Canvas2D globule lab](globule-lab.html) · [revised source tape model](data/string-tape.json) · [spec](docs/string-tape.md). Cellular warfare here is an abstract stress model, not established biological behavior.


## S006 · Homeostasis control grammar
**`1:1` is balanced exchange**, with stress responses **fight `[n:n]`**, **flight `(n:n)`**, and **hide `{n:n}`**. These are authored symbolic states, not observations of cells. Run the [Canvas2D homeostasis lab](homeostasis-lab.html) with automatic or manual controls, state trace and exported witness data. [Model JSON](data/homeostasis.json) · [Spec](docs/string-tape.md).


## S007 · Dot order and generational power limits
Four address orders `. .. ... ....` represent 1D through 4D symbolic grids, while generations increase each side length by a factor of ten: `L=10^g`, capacity `N=10^(g*d)`. Alpha is G0 (one address); Omega is the formal unbounded limit, not an allocated infinity. This models capacity independently of living globule count, homeostasis, and the physical sky. [Interactive Canvas2D](generation-power.html) · [data](data/generation-power.json) · [spec](docs/generation-power.md).
