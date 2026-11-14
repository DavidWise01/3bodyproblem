# S007 · Generational power limits / dot-cubed geometry

The authored notation is `.`, `..`, `...`, `....`. Treat dot count as **number of independent addressing axes** (1D, 2D, 3D, 4D), and generation `g` as the power-of-ten linear resolution per axis. This is a proposed symbolic addressing interpretation, not a physical proof of four spatial dimensions.

```text
Alpha: G0 → 1 × 1 ... across any D
G1 → 10 × 10 × ... (D times)
G2 → 100 × 100 × ... (D times)
G3 → 1000 × 1000 × ... (D times)
...
Omega: limit as g tends to infinity; no physically instantiated infinity
```

## Formal count

`L_g = 10^g` addresses per axis, `N(g,d) = L_g^d = 10^(g*d)` capacity. For a fixed order, one new generation multiplies capacity by `10^d` (10, 100, 1000, or 10000). For fixed generation, one more dot multiplies capacity by `10^g`.

| Generation | . 1D | .. 2D | ... 3D | .... 4D |
|---|---:|---:|---:|---:|
| G0 | 1 | 1 | 1 | 1 |
| G1 | 10 | 100 | 1,000 | 10,000 |
| G2 | 100 | 10,000 | 1,000,000 | 100,000,000 |
| G3 | 1,000 | 1,000,000 | 1,000,000,000 | 1,000,000,000,000 |

## Address lineage, occupancy and computational boundary

The hierarchy is **generation nesting**, not a claim that every potential address is alive. Maintain the parent address and child generation in records. Preserve existing addresses when expanding the resolution; do not silently reinterpret old coordinate IDs. An occupied-cell count is a separate value from total address capacity. Generate sparse projections and bounded samples (at most 600 points), never the full billion-cell lattice merely to draw it.

Globule `@` size rank 0–20 and response tokens `1:1` / `[n:n]` / `(n:n)` / `{n:n}` remain independent attributes of actual cells. A dotted dimension is not a cell, an amino acid, or a gravitational source. Space/time axes (seconds horizontal, arcseconds vertical) are a separately defined coordinate representation; the new addressing axes have no direct transform to those units until explicitly supplied.

```text
ADDRESS_CAPACITY != ACTIVE_POPULATION
HIGHER_GENERATION != AUTONOMOUS_GROWTH
DOT_COUNT != VERIFIED_PHYSICAL_DIMENSION
PARENT_REFERENCE != NEW_INDEPENDENT_WITNESS
FINITE_GRID != ACTUAL_INFINITY
```

Use [Generational Power Canvas](../generation-power.html) and [JSON](../data/generation-power.json).


## S008 — Generational power by engulfing nine peers

**Correction:** The power increase is not merely a larger empty grid. The user specifies an **engulfment promotion operator**: start with one `1×1` alpha unit and **eat nine peer units** to obtain ten total. The resulting aggregate is **promoted to the `10×10` power class**. The `10×10` label is a two-axis *address capacity* (100 possible slots), not a claim that ten source cells created one hundred units of physical mass. Therefore promotion can be consistent with conservation accounting.

```text
  1 seed  + 9 peers  = 10 peer-equivalent units
        \\     |     /
            ENGULF
               |
            PROMOTE
               |
     G1 / 10×10 ADDRESS CLASS
               |
    source mass equivalents = 10
    potential address slots = 100
```

To continue a **strict equal-rank merge** rule, one G1 unit plus nine other G1 units yields G2 (100×100). It then contains the equivalent of 100 G0 seeds, rather than just 19. Similarly G3 contains 1,000 base seeds. This is a *chosen recursive formalization*; if rank promotion instead uses nine raw G0 units at every level, that is a different accumulation law and must be given a different operator.

| Rank | Self + peers at this step | Underlying G0 equivalents | Square-power address capacity |
|---|---|---:|---:|
| G0 | 1 seed | 1 | 1 |
| G1 | 1 G0 + 9 G0 | 10 | 100 |
| G2 | 1 G1 + 9 G1 | 100 | 10,000 |
| G3 | 1 G2 + 9 G2 | 1,000 | 1,000,000 |

The prior `.`, `..`, `...`, `....` dimensional-order addressing remains independent. It governs how **potential addresses** grow for a given promoted generation. A globule's ability to eat, fight, flee, hide, retain, or recover remains a separate response state, not a consequence of its address class.

```text
ABSORPTION != DIGESTION
TEN_CONTRIBUTORS != ONE_HUNDRED_MASS_UNITS
POWER_CLASS != OCCUPIED_ADDRESSES
PROMOTION != GUARANTEED_HOMEOSTASIS
```

Interactive demonstration: [Engulfment Promotion](../generation-engulf.html).


## S009 correction — Highlander: nine MORE at each generation

This section supersedes the S008 **equal-rank merger** rule. In the user's Highlander-style model, one continuing `@` survivor absorbs nine additional rank-zero peer-equivalents to advance from G0 to G1. After that, the **same original survivor must eat nine more** to advance from G1 to G2. There is no requirement to acquire nine G1 peers, and no separate G2 successor replaces the survivor.

At completed generation `g`:

```text
additional units absorbed = 9 * g
survivor unit + absorbed = 1 + 9 * g
power-class side length = 10 ^ g
2D address envelope = 10 ^ (2*g)
```

| Generation | New kills this tier | Cumulative absorbed | Total underlying units | Power envelope |
|---|---:|---:|---:|---|
| G0 | 0 | 0 | 1 | 1×1 |
| G1 | 9 | 9 | 10 | 10×10 |
| G2 | 9 more | 18 | 19 | 100×100 |
| G3 | 9 more | 27 | 28 | 1000×1000 |
| G4 | 9 more | 36 | 37 | 10000×10000 |

The difference between **power class**, **accumulated units**, **physical mass** and **occupancy** remains explicit. Symbolic absorbed-unit accounting neither proves conservation of biological biomass under digestion nor supplies an energy budget.

A monotonically appended event log should record each absorption with the current survivor identity and generation. Promotion occurs only after the ninth new absorption in that tier. This is a deterministic toy rule, not an assertion that organisms literally operate by this mechanism.

**S009 invariant:** `SAME_SURVIVOR + NINE_NEW_PEERS -> NEXT_POWER`.


## S010 — Perception, unequal power, and the freedom not to fight

**Correction:** A globule's generational power changes its *perception and decision context*, not merely the radius of its rendering. For example, an entity ranked `10×10` may recognize a `100×100` opponent as a severe asymmetric risk and elect to flee, hide, or remain homeostatic instead of fighting. Conversely, a `100×100` entity need not chase smaller peers if the energy, risk and effort outweigh the expected reward.

```text
  @ 10×10  →  OBSERVE  →  @ 100×100
                  |
          ESTIMATE POWER / RISK
                  |
          EVALUATE MOTIVATION
                  |
    1:1 | [n:n] | (n:n) | {n:n}
  BALANCE  FIGHT   FLIGHT   HIDE
                  |
          OPTIONAL INTERACTION
```

Keep two different meanings of power accumulation apart:

1. **S009 promotion** uses **nine additional ordinary peers per rank**; generation G2 has 18 total absorbed ordinary peer-equivalents. Power envelope changes according to `10^g × 10^g`.
2. **Aggregation of 100 equal-sized units** starting with one `10×10` requires **99 additional `10×10` units**. That is not the S009 promotion rule and is not automatically chosen merely because it is mathematically possible.

The controller in `perception-lab.html` is a transparent illustrative decision aid with adjustable opponent rank, energy and appetite for growth. Its output is a **proposed policy**; actual organisms, predation, mitochondrial endosymbiosis and physical strength ratios are not validated by the address scale. In particular, the 10× linear-side or 100× address-capacity disparity does not prove a 10× or 100× combat advantage.

**Invariant:** `CAPABILITY != MOTIVATION != CHOICE` and `PERCEPTION != PERFECT INFORMATION`.
