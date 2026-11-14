# Scalar 0 · simultaneous coordinate field v2

## Correction to v1

**Seconds are horizontal; arcseconds are vertical.** They are not switchable unit alternatives. This is a two-dimensional time–angle graph with one common scalar origin `(0,0)`:

- Horizontal coordinate `x=t`, in seconds.
- Vertical coordinate `y=θ`, in arcseconds.
- Angular velocity `ω=dθ/dt`, in arcseconds per second; angular acceleration `d²θ/dt²`, in arcseconds per second squared.
- `13,800,000,000 : 76,000 : 1` supplies user-defined dimensionless scale markers on both axes, each in its own unit. Neither the x nor y scale is itself a measured stellar orbit.
- The default diagram uses logarithmic visual coordinates `log10(1+x)/log10(1+13.8e9)` independently on each axis to show all three reference marks. The underlying data are still in seconds and arcseconds, not log physical units.
- A simple adjustable illustrative trajectory uses `θ(t)=ωt`. It is not a fit to Sag A*, Nib Sun or Sol, and its slope appears curved under log visual scaling even though it is linear in true physical coordinates.
- Signed/negative angles, wraps and angular winding require separate handling in a later model. A full rotation is 1,296,000 arcseconds.

```text
             Y: ARCSECONDS
                   ^
                   |
 13,800,000,000 ----|
                   |
        76,000 -----|
                   |
             1 -----|
                   |
             0 -----+----------------> X: SECONDS
                   0  1   76,000   13.8B
```

The 368-address A/B/C partitions are semantic registry labels and are not equal to angular or temporal samples unless a mapping rule is later declared. `0` is a reference, not a fourth body.

The existing physics integrator on `index.html` uses separate dimensionless Cartesian spatial positions. This page is a **time–angle analysis plane**, not that spatial dynamics simulation.

## Invariants

```text
X_SECONDS != Y_ARCSECONDS
ONE_SECOND != ONE_ARCSECOND
ADDRESS != ANGULAR_POSITION
LOG_PLOT != LINEAR_PHYSICAL_MOTION
NIB_SUN != DETECTED_OBJECT
```
