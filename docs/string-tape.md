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
