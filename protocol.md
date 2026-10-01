# Protocol (pre-registered)

> Commit and push this file BEFORE claiming the Vecura token pack.
> Fill in every field. Do not change thresholds after seeing BioEmu results;
> if you must, add a dated "Amendment" section at the bottom and explain why.

## Research question
Starting from sequence alone, can BioEmu sample conformations in which the
switch-II pocket opens, and do molecules generated for that pocket resemble
known KRAS G12C inhibitors?

## Hypothesis
<!-- Your prediction, in your own words. Example structure:
BioEmu will sample open switch-II pocket conformations in about __% of G12C samples,
and this rate will be (higher / lower / similar) compared with wild-type. -->

## Target and sequences
- Protein: human KRAS (GTPase KRas), UniProt P01116 (RASK_HUMAN)
- Construct: G-domain, residues 1-169 (confirm range: ____)
- Variant of interest: G12C (glycine to cysteine at position 12)
- Control: wild-type KRAS
- Sequence files: structures/kras_wt_gdomain_1-169.fasta, structures/kras_g12c_gdomain_1-169.fasta
- Verified against UniProt FASTA on (date): ____

## Reference structures
| Role | PDB ID | Title / notes | Resolution | Verified (date) |
|------|--------|---------------|-----------|-----------------|
| Sotorasib-bound G12C | 6OIM | KRAS G12C covalently bound to AMG 510; contains GDP and Mg; construct has engineered mutations C51S, C80L, C118S | 1.65 A | ____ |
| Apo / GDP-bound G12C, no switch-II drug | ____ | | ____ | ____ |
| Wild-type KRAS, GDP-bound (control) | ____ | | ____ | ____ |

## Known inhibitors
- Source: ChEMBL (target: ____; filters: ____)
- Date downloaded: ____
- Number of molecules after RDKit parsing: ____
- File: inhibitors/____.csv

## Definition of "open" (set BEFORE running BioEmu)
- fpocket pocket volume near switch II, apo reference: ____ A^3
- fpocket pocket volume near switch II, 6OIM with drug removed: ____ A^3
- Threshold for "open" pocket volume: ____ A^3
- Switch-II position criterion (metric and cutoff, e.g. RMSD to bound reference over switch-II residues): ____
- A sample counts as "open" only if BOTH criteria are met.

## What counts as a negative finding
<!-- Example: "If fewer than __% of G12C samples meet the open criteria, and the rate does
not differ from wild-type, I will report that BioEmu does not sample the pocket from sequence." -->

## Planned analyses
- Weeks 1-2: structure comparison (RMSD, switch I/II), ensemble sampling and pocket volume
- Weeks 3-4: Pocket2Mol generation (open vs closed pockets), RDKit properties (validity,
  uniqueness, QED, Lipinski), Tanimoto similarity to known inhibitors
- Week 5: second-seed robustness check

## Known limitations (stated in advance)
- BioEmu works from sequence only and does not model the bound nucleotide (GDP).
- Real G12C drugs bind covalently; Pocket2Mol does not model covalent binding.
- All results are computational hypotheses, not validated chemistry.
- Candidates are unscored unless docking is added locally.

## Amendments
<!-- Date, what changed, why. -->
