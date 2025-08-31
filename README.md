# GROMACS Pipeline for Solar Cell Hole Transport Layer

This repository contains a GROMACS-based workflow for simulating the hole transport layer in perovskite solar cells, focusing on **spiro, TBMP, and TFSI** molecules.

> **Note:**  
> - GitHub has a 100 MB file size limit, so large files are provided as `.zip`.  
> - The included setup uses an older `gmx_mpi` version of GROMACS. For best performance and compatibility, it is recommended to use the latest version of GROMACS, especially with the **GAFF force field** for H-type layers.  

---

## Pipeline Overview

1. **Generate simulation parameter files**
   ```bash
   ./make_mdp.sh


type in smiles molecules in get_acpype.sh
./get_acpype.sh


python3 rename_packmol_input.py folder1 folder2 folder3


./prepare_gromacs_input.sh


sbatch run_nvt_npt_temperature_timer.slurm
or sbatch run_nvt_npt_annealing.slurm


plotter.py


optional:
check_itp_charges.py
estimate_density.py

run_index.slurm if names are not 3 letters everywhere SPI exc...

