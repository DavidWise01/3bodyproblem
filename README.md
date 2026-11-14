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
