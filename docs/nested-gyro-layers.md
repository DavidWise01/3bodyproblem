# Three-body nested geophysical gyro model · v0.1

## User framing

Three gravitating bodies. For each body, track a rotating material interior — `core / mantle / crust` — and the surrounding charged / magnetized environment — `ionosphere / magnetosphere / stellar-wind environment`. Treat the layers as *coupled dynamical regions*, not nine literal mechanical rotors. This is an additive science-and-mnemonic model alongside the original Seven Suns scene/physics arcade.

## ASCII / nested schematic

```text
                   {{ THREE BODIES }}
                   A      B      C
                   |      |      |
               +---+------+------+-+
               |  EXTERNAL FIELD   |
               |  stellar wind /   |
               |  heliosphere*     |
               |  magnetosphere    |
               |  ionosphere       |
               +-------------------+
                   |      |      |
               +---+------+------+-+
               |  INTERNAL MATTER  |
               |  crust            |
               |  mantle           |
               |  core             |
               +-------------------+
                   |      |      |
                   +---{{i}}---+
                        |
            ROTATION / PRECESSION
                        |
             GRAVITY / TORQUE / MHD
                        |
               RECURSIVE ITERATION
```

*Heliosphere is a stellar-wind bubble formed by a star such as the Sun and encompasses the solar system, including planets. It is NOT an intrinsic shell of each planet. Ionosphere and magnetosphere are interacting, partially overlapping regions, not consistently concentric shells. A rocky body's crust/mantle/core vocabulary does not directly apply to a star (whose layers are differently named); atmospheres/magnetic fields may not be present for every body. Therefore each of three bodies gets a configurable set of layers, not a physically mandatory identical six-layer stack.*

## Simulation model contract / physical controls

1. Orbit of the bodies: `dr_i/dt = v_i`, `m_i dv_i/dt = sum(F_gravity) + sum(F_external)`. Keep gravity distinct from electromagnetic force.
2. Bulk spin of a body: `dL_i/dt = tau_external,i`. With nested compartments, `L_i = sum_k I_ik omega_ik` only under simplified aligned/principal-axis approximations; generally use tensors and frame transforms.
3. Layer exchange: an internal torque `tau_{a→b}` must have `tau_{b→a} = -tau_{a→b}`; sum total angular momentum across interior and external fields, including transport and external fluxes.
4. Dynamo: do not assume every core is conductive or actively generates a field; magnetic induction requires a separate parameterized dynamo/field model.
5. Ionosphere and magnetosphere: electrodynamic couplings and plasma flows can transfer momentum, with solar/stellar-wind forcing; this does not require or imply direct contact between three planetary magnetospheres.
6. Stellar-wind environment: heliosphere only for the star providing the stellar wind. For other stars use astrosphere (a stellar-wind bubble).
7. Numerics: start from three gravitational point-mass centers, add three rotating interior layers per applicable rocky planet, then add configurable exterior field regions. Maintain a clear switch for physical simulation vs geometric/mnemonic visualization.

## Model mapping for `{{3x3}}^{{3}}>1 x 3 bodies`

This syntax is preserved as the project-owner's recursive address notation. A *chosen implementation mapping* might treat 3 axes (x/y/z), 3 interior regions (core/mantle/crust), 3 exterior field/plasma regions (ionosphere/magnetosphere/stellar-wind environment), and 3 parent bodies. Do **not** equate the mathematical exponent with a proven count of distinct physical rotors: the tensor/address structure and the physical number of degrees of freedom are different things.

## Natural invariants

```text
LAYERED_REGION != RIGID_GYROSCOPE
HELIOSPHERE != PLANETARY_SHELL
IONOSPHERE != SEPARATE_NONOVERLAPPING_SHELL
INTERNAL_TORQUE != NET_EXTERNAL_TORQUE
GEOMETRIC_NESTING != VERIFIED_DYNAMIC_COUPLING
THREE_BODY_GRAVITY != THREE_BODY_MAGNETIC_CONTACT
```

## Status

This is the **concept/spec layer**. The current `index.html` still simulates three gravitational centers; it does **not** yet implement core–mantle coupling, induction equations or magnetohydrodynamic feedback. Future dynamics must be validated against established geophysics before labeling them physical results.


## v0.2 — Named parent systems and [?] reference center

A: **Sagittarius A***, observed supermassive black hole at the Milky Way center, approximately four million solar masses. Not a star or rocky body.

B: **Nib Sun**, user-proposed hypothetical star or substellar body; no astronomical detection or measured mass/orbit. NASA WISE places strong limits on a large local companion.

C: **Sol**, the observed Sun, whose galactic trajectory is due to the galaxy's distributed gravitational potential (not just Sagittarius A* alone).

The mathematical **restricted triple barycenter** `R=(mA*rA+mB*rB+mC*rC)/(mA+mB+mC)` is defined when masses/positions share one reference frame. It is not in general identical to the **Galactic dynamical center**, and a barycenter is not necessarily a gravitational source or a stable common orbital focus. The visual schematic `three-centers.html` uses arbitrary normalized weights [12,2,1] because no mass measurement exists for Nib Sun; it is not an ephemeris or N-body fit.

**Layer correction:** stellar internal structure (core/radiative/convective zones) is not crust/mantle/core. A black hole has no material rock layers. A heliosphere is a stellar-wind bubble, not each planet's external ring. Ionospheric/magnetospheric layers apply conditionally to appropriate bodies.

```
NIB_SUN != OBSERVED_OBJECT
TRIPLE_BARYCENTER != GALACTIC_DYNAMICAL_CENTER
BARYCENTER_EXISTS != STABLE_CIRCULAR_ORBIT
SCHEMATIC_MOTION != OBSERVED_ASTROMETRY
```


## v0.3 — Scalar 0 registry (author-specified)

```text
                      {{0}}
                        |
                ADDRESS REGISTRY
               /       |        \\
        A SAG A*      B NIB       C SOL
        001-122       123-245    246-368
          122           123        123
             \          |        /
                368 CELLS TOTAL
```

**Exact inclusive partition:** A = [1,122] (122 cells); B = [123,245] (123 cells); C = [246,368] (123 cells). 0 is reserved as a scalar reference, not included in the count. There are no omitted or overlapping indices. `122+123+123=368`.

The registry is authored symbolic geometry, not wavelength, celestial coordinates, mass or orbit. In particular, 0 is **not** itself evidence of a common gravitational center, and an assigned index does not confirm that Nib Sun exists. A mathematical barycenter remains a separate quantity derived from physical masses/positions.

JSON source: `data/scalar0-registry.json`. Interactive selector: `three-centers.html`.
