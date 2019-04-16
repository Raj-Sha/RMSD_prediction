# RMSD_prediction
Predicting protein 3D structures without crystalization has been a challenging problem. Chemical, physical, and biological properties are the determinants of protein folding under specific solvent environments. A lot of problems involves in predicting a protein's native structure such as secondary structure arrangment and misfolding tertiary structures because the protein is not folded in solvent conditions. This research helps to determine whether the predicted proteins are structurally similar to the native, folded proteins based on six experimental factors. The Root Mean Square Deviation (RMSD) is the squareroot of the sum of all distance's changes between matched pairs of  𝐶𝛼  in two superimposed protein sequences.

𝑅𝑀𝑆𝐷=∑𝑁𝑖=1(𝑝𝑖−𝑞𝑖)2𝑁⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯√ 
where  𝑝𝑖,𝑞𝑖  are coordinate positions of matched pairs of  𝐶𝛼  in the modelled protein, and its native one, respectively.

There are six physical and chemical properties1 that can be used to predict the RMSD of a protein.
Total surface area (Area): the total surface area of a protein that is exposed to the solvent after the protein is fully folded. The surface area of a protein is dependent on the amino acids which ultimately bury the hydrophobic core.

Euclidean Distance (ED):  𝐶𝛼 's positions were restricted when interacting with neighborhood  𝐶𝛼  in a folded protein 2 . The sum of distance between each pair of  𝐶𝛼  in a single protein is computed as ED.

Total empirical energy (Energy): The sum of electrostatic force, Vander Waals, and hydrophobic force.

Secondary Structure Penalty (SS): it is measured from secondary structure sequence. It is computed as the absolute difference between secondary structures based on coordinates and the probability for the same class structures.

Pair number (PN): the total number of aliphatic, hydrophobic residue pairs in the protein structure.

Residue Length (RL): the total number of  𝐶𝛽  carborns in the structure

The RMSD is computed using Python, instead of using R from the previous research 1 . The goal is to classify RMSD values into one of five categories, 1, 2, 3, 4, or 5Å. We apply Machine Learning from Sklearn library with support from Pandas, Seaborn, Numpy, and Matplotlib libraries. 4 models are used: Neural Network, Linear Model Classification, K Neighbor Classification, and Randomforest, to analyze the dataset. The model that computes the highest accuracy is optimized using GridSearch to tune specific parameters for that model. Finally, the tuned model is tested with confusion matrix, k fold validation and my own k fold validation.
