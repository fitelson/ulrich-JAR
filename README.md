# Input Files for "Applying Saturation-Based Theorem Proving to Open Problems in Positive Implicational Logic"

This repository contains the TPTP input files accompanying the paper:

> Ulrich, D. and Fitelson, B. "Applying Saturation-Based Theorem Proving to Open Problems in Positive Implicational Logic." *Journal of Automated Reasoning*.

## Files

- **u1.p** -- Input file for refuting candidate u1 as a single axiom for positive (intuitionistic) implication.
- **u2.p** -- Input file for refuting candidate u2 as a single axiom for positive (intuitionistic) implication.
- **u3.p** -- Input file for refuting candidate u3 as a single axiom for positive (intuitionistic) implication.

## Usage

These files are intended for use with [Vampire](https://vprover.github.io/) (version 5.0.1). Each file can be run with the following command:

```
vampire --mode portfolio --schedule casc_sat --saturation_algorithm lrs <filename>.p
```

Vampire will generate a saturated set of clauses corresponding to a model on which the candidate axiom is a theorem but `i(P,P)` is not, thereby ruling out the candidate as a single axiom.

## Format

The files are in [TPTP](https://www.tptp.org/) (Thousands of Problems for Theorem Provers) format.
