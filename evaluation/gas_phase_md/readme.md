# How to run gas phase simulations using a PhysNet model

1) Create (copy) an .xyz file containing the molecule/structure you want to run MD simulations with. Ideally, this is
a good initial guess of an optimized structure (the structure will be optimized at the beginning of the simulation).
2) Run MD simulation (./md_simulation.py -i opt_structure.xyz -o trajectoryname) [all optional command line arguments
can be changed from the command line, too.] The script can be used to run NVE or NVT simulations by changing the default
value of --mdtype or running (e.g. for NVE simulations) ./md_simulation.py -i opt_structure.xyz -o trajectoryname --mdtype NVE.
3) The python script runs an optimization, an equilibration (for which no snapshots are saved) and a production run
(for which snapshots are saved in an interval) and saves the trajectory in the .traj file format.
4) Visualize the result with ase gui or vmd
