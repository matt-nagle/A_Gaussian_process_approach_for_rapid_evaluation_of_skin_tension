# A Gaussian process approach for rapid evaluation of skin tension

This repository contains a sample of 10 virtual subjects and the machine learning pipeline (written in python) to accompany the paper:

Nagle, M. and Broderick, H. C. and Vedel, C. and Destrade, M. and Fop, M. and Ní Annaidh, A. (2024), **A Gaussian process approach for rapid evaluation of skin tension**. *Acta Biomaterialia* (currently in review).

The file ``sample_training_dataset.csv'' contains a sample of 10 subjects from the full training dataset. The variable E is the Young's modulus, rho is the density, beta controls the material model (ranging from -1, pure neo-Hookean to +1, extreme Mooney-Rivlin), lambda1 is the uniaxial pre-stretch applied to the skin, Avg S11 t=0 is the average stress in the direction of the applied uniaxial pre-stretch at the start of the wave propagation step (before the impact has been applied), the Supersonic Velocity is the speed of the supersonic shear wave, the Rayleigh Velocity is the speed of the Rayleigh wave and the Material Model identifies the material model used in the finite element simulation.

The file ``MN_Custom_Palette.py" defines the custom colour palette, figure dimensions, dpi and fontsizes used to make the publication figures.

The file ``Machine Learning Pipeline.ipynb'' contains the full machine learning pipeline: importing the training dataframe, normalising the variables, defining the blank slate Gaussian process regression model and corresponding kernel, training the GP model and evaluating performance.