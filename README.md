# KRAS G12C Pocket Discovery

Can AI find the hidden switch-II pocket of KRAS G12C from sequence alone, and do
molecules generated for that pocket resemble known inhibitors?

**Status:** Week 0 (setup and pre-registration)

## Research question
Starting from sequence alone, can BioEmu sample conformations in which the switch-II
pocket opens, and do molecules generated for that pocket resemble known KRAS G12C
inhibitors?

## Tools
| Tool | Where it was run | Version / date |
|------|------------------|----------------|
| Chai-1 | Vecura | |
| BioEmu | Vecura | |
| PROPKA 3 | Vecura | |
| Pocket2Mol | Vecura | |
| RDKit, MDTraj, fpocket | Local | |

## How to reproduce
1. `conda env create -f environment.yml` then `conda activate kras-g12c`
2. Install fpocket (and optionally AutoDock Vina) as noted in `environment.yml`
3. See `protocol.md` for thresholds and file sources
4. Run scripts in `scripts/` in the order listed here (to be filled in as they are written)

## Key results
_To be added._

## Limitations
- BioEmu works from sequence only and does not model the bound nucleotide (GDP).
- Real G12C drugs bind covalently; Pocket2Mol does not model that.
- Everything here is a computational hypothesis, not validated chemistry.

## Data and licensing notes
- ChEMBL data has its own terms; this repo references the source and filters rather than
  re-publishing the full dataset.
- Outputs from Vecura are not redistributed here unless its terms allow it.
- The models used (BioEmu, Pocket2Mol, etc.) are hosted on Vecura; their code and weights
  are not copied into this repo.

## Acknowledgments and citations
_To be added._
