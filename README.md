Gromacs pipeline for solar cell hole transport layer using spiro, tbmp, tfsi.

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