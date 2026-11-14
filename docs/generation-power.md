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
