# Variational Autoencoder

This repository contains the necessary scripts to convert specifically formatted Root files to binary hdf5 files for training, as well as Jupyter notebooks to train a basic VAE architecture and analyse its performance with the relevant datasets. Please view the environment.yml file to download the relevant python libraries to load all the project contents (including tensorflow). 

## Preparing the Training/Testing Data

To prepare the initial data, one should use the *convert_to_h5.py* script. The syntax necessary to run it is as follows: 

'''
python convert_to_h5.py --input-file *INPUT ROOT FILE NAME* -- output-file *PICK YOUR FAVOURITE OUTPUT FILE NAME.hdf5* 
'''

Note that this script expects that the root file analysed has a tree name with the relevant region data called 'l1UpgradeEmuTree/L1UpgradeTree'. If this directory is not within the ROOT file and does not contain the TTrees *'vRegionEt','vRegionEta','vRegionPhi'*, then it will need to be modified. 

## Training and Testing the Network

The notebook *ZeroBias_VAE.ipynb* contains all the steps necessary to initialise, train and test a basic VAE on pre-prepared training/testing hdf5 datasets. 

## Plotting the Data

We have also included another plotting script *VAE_Plotting_Script.ipynb* to plot the resulting training and testing data (in particular, the loss values) from the original network.  