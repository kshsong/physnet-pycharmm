# How to calculate out of sample performance of a PhysNet model


1) Choose your best model and copy it to the ../models_clPhOH folder.
2) copy your input file (containing the hyperparameters of PhysNet) to the current path and add your dataset to the dataset folder.
3) make sure the predict_testset.py contains the correct file paths to checkpoint files (line 70)
4) adapt name of the file to which the NN and ref energies are saved to.
5) execute the file as for training an NN (./predict_testset.py @run_clphoh*.inp)
