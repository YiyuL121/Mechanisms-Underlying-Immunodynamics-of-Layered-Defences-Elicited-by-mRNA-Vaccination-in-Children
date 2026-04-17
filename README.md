# Mechanisms-Underlying-Immunodynamics-of-Layered-Defences-Elicited-by-mRNA-Vaccination-in-Children


### Overview
This repository contains supporting files for the results reported in "Mechanisms-Underlying-Immunodynamics-of-Layered-Defences-Elicited-by-mRNA-Vaccination-in-Children"


### Features
   - Feature 1: simulate biomarker trajectories based on Monolix output: Anti-S-IgG, nAbs, S+MBC, IFN-g and IL2
   - Feature 2: Survival analysis: Cox-PH model with time-varying covariate 
   - Feature 3: Estimation of the protection duration of children with hybrid immunity


## Data Availability

### Provided in `data/`
Monolix fitting output used to regenerate simulated trajectories:
| File | Description |
|---|---|
| `populationParameters_{igg,nab,mbc,ifng}.txt` | Population-level parameters |
| `estimatedIndividualParameters_{igg,nab,mbc,ifng}.txt` | Empirical Bayes estimates |
| `simulatedIndividualParameters_{igg,nab,mbc,ifng}.txt` | Conditional simulations |

### Not publicly released
The following inputs contain participant-level information and are therefore **not** shipped with this repository. Access may be requested from the corresponding author under a data-use agreement:
- Biomarker raw data (`*_raw.csv` for IgG, nAb, MBC, IFN-g, IL-2)
- Individual immunity-event metadata (`immu_detail_individuals.csv`,`immu_detail_individuals_reinf.csv`, `inf_info.csv`)
- Monolix project files (`*.mlxtran`) required by script (7)

Scripts that depend on these inputs are clearly flagged; the rest of the pipeline can be re-run end-to-end from the provided Monolix output.

## Requirements
- **R** >= 4.2
- R packages: `deSolve`, `ggplot2`, `dplyr`, `tidyr`, `purrr`, `MASS`,
  `survival`, `survex`, `randomForestSRC`, `lubridate`, `GGally`,
  `patchwork`, `scales`
- *(script 7 only)* **Monolix 2024R1** plus `lixoftConnectors` and `Rsmlx`

