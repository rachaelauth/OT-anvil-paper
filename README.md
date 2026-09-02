# OT-anvil-paper

Code and analysis notebooks accompanying the paper:

> **Overshooting Top Characteristics Across Anvil Life Cycles**
> R. M. Auth, K. M. Bedka, J. W. Cooney, S. W. Freeman, and S. C. van den Heever
> *JGR: Atmospheres*, 2026.

This repository contains the analysis pipeline used to identify, track, and characterize overshooting tops (OTs) and their associated anvil clouds, and to reproduce the figures presented in the paper.

DOI: 10.5281/zenodo.22261669

## Repository contents

| File | Description |
|---|---|
| `tobac_for_OT_anvil_paper_final.ipynb` | Runs the [tobac](https://tobac.readthedocs.io/) workflow defined in Figure 2 to detect and track overshooting tops and anvils from the input dataset. |
| `meso_counts_OT_anvil_paper.ipynb` | Computes mesosector geographic location counts, plots these counts and tracked OT counts to create Figure 1. |
| `OT_anvil_paper_figures_final.ipynb` | Runs analysis on tobac output from tobac_for_OT_anvil_paper_final.ipynb and generates Figures 4-7 used in the paper. |

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Data

This project uses output obtained from running the software availible at https://github.com/nasa/svrstormsig.

Data are not included in this repository due to size. To reproduce the analysis:

1. Download v3.2 of the ML OT detection software from https://github.com/nasa/svrstormsig/commit/85b8efe60f08f3233e9803a9346fbc3ce8d1ecea.
2. Run 1. using settings defined in Section 2.1 of the paper.
3. Update file paths in each notebook to point to your local data.

## Usage

Run the notebooks in the following order:

1. **`tobac_for_OT_anvil_paper_final.ipynb`** — detects and tracks OT/anvil features.
2. **`meso_counts_OT_anvil_paper.ipynb`** — counts mesosector locations and plots them with OT counts.
3. **`OT_anvil_paper_figures_final.ipynb`** — produces the paper's figures from the above outputs.

## License


## Contact

Rachael Auth — rauth@colostate.edu
