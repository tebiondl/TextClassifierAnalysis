# Purpose
This repository contains all the code used for my Master's Thesis entitled "Analyzing the boundary between neuronal and non-neuronal text classifiers". The thesis can be accessed in this link (https://oa.upm.es/83409/).
In this repository you will find all the tests and experiments I made with different classic and neuronal text classifiers to find the boundary between neuronal and non-neuronal models.

# Reproduce the Experiments

To reproduce the experiments made with this code first of all you need to download the datasets from Zenodo.

## Get the datasets
Original DBpedia dataset -> https://zenodo.org/doi/10.5281/zenodo.12773814
Derived datasets made by me -> https://zenodo.org/doi/10.5281/zenodo.12783743

You can download one of them, but if you only download the original dataset, you have to create the derived datasets using the code in the notebook "ProcessRawFiles.ipynb" to create the base dataset, and for the rest of the derived datasets, use the code in notebooks "DivideDataset.ipynb" and "CropUpDown.ipynb" changing the parameters to your liking.

If you downloaded the derived datasets, that step will be already done. You need to create a folder called "FinalDataset" and move these datasets there.

## Train the models

Now that you have the datasets ready, you just need to open any model notebook -> "XLNet.ipynb", "BERT.ipynb" or "ClassicModels.ipynb", change the filename variable with the name of any of the datasets and the model will train with that dataset.

# Extras and Utilities

Be careful with XLNet because it uses a lot of RAM and GPU.

If you want to plot the results, you can see the results inside "Results/ModelResults.csv", and the last column "Dataset" is the name of the experiment, so for example the name "nosub". If you want to plot the results of the experiment "nosub", go to the "CreateGraphs.ipynb" and change the "dataset_name" variable to whichever experiment you want.

The Utilities notebook is explained in a coment in every cell.

To see all the relevant information of any dataset, use the "AnalysisDataset.ipynb", enter the name of the dataset file and then you will see all the info.
