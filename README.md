# GerAB_SMD
This repository contains the input files for steered molecular dynamics simulations using gromacs and plumed
for the systems indicated in the list below.
The simulations are performed for the GerAB protein in
a membrane containing three lipids, POPG, TMCL2 and POPE, the temperature is set to 298 K,
the concentration ions is [KCl] = 20 mM, and alanine is present in the L-form.

Force field parameters are provided.

One water molecule is selected to pull through GerAB during simulations. SMD parameters are provided in plumed.dat

MD parameter is provided in md.mdp

To run the simulations:

copy the force field parameters and the md.mdp file into the directory of the system.

cp forcefield/* md.mdp run_nr


To perform SMD run for 100 ns:

INPUT_FILE=run_nr

gmx mdrun -deffnm ${INPUT_FILE} -plumed plumed.dat -v

