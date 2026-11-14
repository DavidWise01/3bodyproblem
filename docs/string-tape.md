# S004 · exact ASCII interval tape and twenty amino-acid mnemonic

## Source tape (verbatim)

```text
-+---------------#-------------@-@--@---@----@-----@------@-------@--------@---------@----------@-----------@------------@-------------@--------------@---------------@----------------@-----------------@------------------@-------------------@--------------------@
```

The literal was supplied by the author and is the sole canonical source. Length 262 characters. The leading prefix is `-+---------------#-------------`; it includes minus, plus and hash operators, followed by the first `@`. The complete tape has 21 `@` marker characters. The 20 **intervals between adjacent @ markers** have exactly `1,2,3,...,20` hyphens, for `210` total inside these intervals.

## Exact address algorithm

Scan left-to-right. Preserve every character. Capture zero-based offsets of all `@`. Interval i spans marker at `at[i-1]` to `at[i]` inclusive; gap length = `at[i]-at[i-1]-1`. Verify count=20 and lengths=1..20. The leading root operator `-+---------------#-------------` is not an amino interval. The final `@` terminates interval 20 rather than creating a twenty-first amino-acid slot.

## Mnemonic amino mapping (authoring choice, not biochemical decoding)

1. Alanine (A), hyphen gap 1
2. Arginine (R), hyphen gap 2
3. Asparagine (N), hyphen gap 3
4. Aspartic acid (D), hyphen gap 4
5. Cysteine (C), hyphen gap 5
6. Glutamine (Q), hyphen gap 6
7. Glutamic acid (E), hyphen gap 7
8. Glycine (G), hyphen gap 8
9. Histidine (H), hyphen gap 9
10. Isoleucine (I), hyphen gap 10
11. Leucine (L), hyphen gap 11
12. Lysine (K), hyphen gap 12
13. Methionine (M), hyphen gap 13
14. Phenylalanine (F), hyphen gap 14
15. Proline (P), hyphen gap 15
16. Serine (S), hyphen gap 16
17. Threonine (T), hyphen gap 17
18. Tryptophan (W), hyphen gap 18
19. Tyrosine (Y), hyphen gap 19
20. Valine (V), hyphen gap 20

The set of twenty standard proteinogenic amino acids is used as a **labeling alphabet** in a conventional listing order chosen for this representation. No genetic codons, peptide bonds, actual residues, secondary structure, dynamical field equations or experimental proof of string theory are implied by matching the number twenty. Selenocysteine and pyrrolysine are additional genetically encoded amino acids in some organisms; the standard textbook twenty is the mapping used here.

## Physical and coordinate boundary

Existing Scalar 0 graph: x=time in seconds; y=angle in arcseconds, with shared reference 13.8B:76,000:1. The tape's discrete ordinal is a *third, independent index*, not automatically seconds, degrees, protein position, or an orbit. No physical transform connecting those spaces is assumed.

```text
21 @ boundaries -> 20 intervals
SUM(1..20) = 210
ONE-LETTER-LABEL != PROTEIN-SEQUENCE
SYMBOLIC-STRING != PHYSICAL-STRING-THEORY
OBSERVED_BIOCHEMISTRY != NUMERICAL_COINCIDENCE
```

## Files

- `data/string-tape.json`: exact literal and parser output
- `string-tape.html`: sprite-animated Canvas2D reader and user-selected amino intervals
- `docs/string-tape.md`: interpretation contract and caveats


## S005 — correction: the @ are globules

The author's intended ontology is that **each `@` is one globule**. The exact tape therefore has **21 globules**, the first a size-rank-zero seed and the following twenty globules assigned nominal ranks 1 through 20 according to the length of the immediately preceding hyphen run. Those hyphen runs are **size-growth measures**, not merely empty distances. This size assignment is an explicit authored convention that lets the growing ladder be tested without altering the literal source string. The 20 standard-amino-acid labels of S004 become mnemonics for the **twenty size transitions**, not literal contents of the globules.

```text
-+---------------#-------------@ - @ -- @ --- @ ... -------------------- @
                               G0  G1   G2     G3                          G20
                               0   1    2      3                           20
                              SEED         GROWTH SIZE RANK
```

## Boundary grammar: containment versus interruption

- `{[()]}` = fully paired nested boundaries, **contained** in the authored symbolism (brace, box, toroidal parenthesis).
- `{[(]}` = **unbalanced** string: the `(` is not closed before the `]` and `}`; it symbolizes a breached/interrupted containment state rather than a valid nested balanced grammar.
- A computer parser must not pretend both are equally balanced; it should preserve the literal damaged form as evidence of the interruption.
- **Cellular warfare** is modeled as a symbolic contest between applied pressure and boundary integrity: `contained → pressured → breached → recovered`. This is an abstract state machine, not a depiction of actual cells attacking, protein folding, or validated microbiology.

```text
@ = GLOBULE
--- = SIZE OPERATOR / THREE UNITS
{{ i }} = OBSERVE
{[()]} = CONTAINED
{[(]} = INTERRUPTED / BREACHED
SIZE_RANK != PHYSICAL_RADIUS_WITHOUT_UNIT
MORPHOLOGY != PROVEN_BIOLOGY
```

Explore the [animated globule and boundary lab](../globule-lab.html), based on the exact [string-tape JSON](../data/string-tape.json).


## S006 — Homeostatic response grammar (correction)

The author defines **homeostasis as `1:1`**. Stress may select one of three distinct behaviors: **fight `[n:n]`**, **flight `(n:n)`**, and **hide `{n:n}`**. Here n:n represents a symbolic variable-scale interaction of two sides; there is no observed organism count or physically calibrated exchange ratio. The earlier `{[()]}` and `{[(]}` expressions remain morphology/boundary-state encodings, not replacements for this behavioral grammar.

```text
                     1:1
                      |
                 OBSERVE STRESS
                      |
                  SELECT STATE
                     /|\\
               [n:n] (n:n) {n:n}
               FIGHT FLIGHT HIDE
                     \\|/
                MEASURE RESPONSE
                      |
                 BALANCE? -> 1:1
```

**Proposed deterministic toy model:** energy, boundary integrity, exposure, separation and pressure use normalized 0..100 scores. The controller can choose automatically or be overridden. Fight spends energy defending, flight spends energy separating, hide spends less energy reducing exposure, and unpressured balance tends to recover reserve. No emergent decision or experiment is claimed; these dynamics are authored rules designed to be inspected and challenged.

**Non-equivalence:** maintaining homeostasis does not imply inactivity, and allocating 1:1 does not imply an experimentally measured concentration or energy flow. Restore of a score does not imply restored organism viability.

- [Animated Homeostasis Lab](../homeostasis-lab.html)
- [Versioned model](../data/homeostasis.json)

```text
HOMEOSTASIS != INACTIVITY
FIGHT != FLIGHT != HIDE
NOTATION != BIOLOGICAL_VALIDATION
ENERGY_COST != FREE_RECOVERY
```
