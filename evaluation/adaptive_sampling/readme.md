# How to run adaptive sampling using two or multiple PhysNet models

1) Create (copy) an .xyz file containing the molecule/structure you want to predict. Ideally, this is an
optimized structure.
2) Run adaptive sampling (./adaptive_sampling_md.py -i opt_structure.xyz -o trajectoryname)
3) The python script saves structure visited in MD only if the standard deviation in energy between the two is
larger than a threshold (here Ethreshold = 0.0215 eV ~ 0.5kcal/mol)
4) Visualize the result with ase gui or vmd
5) From the .traj file containing the "less represented" structures, create new input files for molpro
6) Start new trainings with extended/improved data set
7) Repeat adaptive sampling procedure until convergence.
