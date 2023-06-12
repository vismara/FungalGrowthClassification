# Fungal Growth Classification

'fungalGrowthClassification' is an automated R code used to perform Machine Learning (ML) experiments and their automated analysis, including plots and tables. Thus, this repository includes all the necessary files to reproduce our paper *``Classification of the growth level of fungal colonies in solid medium: a machine learning approach''*.

## Repository Structure

This repository is structured as follows:
- **data/**: contains all the datasets generated to execute the ML experiments;
- **R/**: contains some useful R scripts that automate some behavior or extract statistics. There is also a configuration file in it;
- **results/**: contains all the generated results (in .RData objects, text files, or tables);
- **plots/**: contains the papers' figures generated by the exploratory data analysis or the results' automated analysis;
- **scripts/**: contains some scripts we designed to perform experiments (preprocessing images, and so on);
- **test/**: some programming tests

## General Instructions

There are three main and important files:

- **01_ExploratoryAnalysis.R**: perform the Exploratory Data Analysis (EDA) in the generated datasets;
- **02_MLExperimentsMLR.R**: perform classification experiments running several algorithms in different learning tasks, checking different properties available in the dataset;
- **03_generateCVFoldsForDeepLearning.R**: generates automatically the training and testing folds to run Deep Learning baselines;
- **04_deepLearningExperiments.ipynb**: it executes Deep Learning algorithms, with the original images and training/testing folds generated by script number 03, using Keras, TensorFlow and jupyter notebook.
- **05_ResultsAnalysis.R**: perform the automated analysis of the results obtained by the task above;

You can run all three scripts separately, but there is a *natural* dependency between scripts according their numbers: 01_,02_, 03_, 04_ and 05_. For example: the automated analysis (05_) will only generate figures if ML experiments (02_) have had executed; otherwise, it will fail.

## Running the code

To run the complete analisys execute the bash script file named "run" located in the code folder.

Maybe some relative paths need to be edited in order to find the correct place where the images are. 

## Contact

- Edgar de Souza Vismara (edgarvismara@utfpr.edu.br), Federal Technology University - Paraná (UTFPR) - Dois Vizinhos - PR, Brazil.
- Rafael Gomes Mantovani (rgmantovani@gmail.com), Federal Technology University - Paraná (UTFPR) - Apucarana - PR, Brazil.
