# RW441 Assignment 3: Incremental Class Learning

This repository contains the code and supporting results for my RW441 Assignment 3 on incremental class learning for imbalanced multiclass classification.

The study compares a conventional feedforward neural network with an incremental learning approach in which classes are introduced from the least frequent to the most frequent. Model complexity is increased when the current architecture begins to underfit.

## Datasets

Three multiclass datasets from the UCI Machine Learning Repository were used:

- Dry Bean
- Steel Plates Faults
- Statlog Landsat Satellite

The datasets are publicly available from UCI and are therefore not redistributed in this repository.

## Method

The conventional model is trained on all classes from the beginning.

The incremental model starts with the two least frequent classes. Additional classes are introduced one at a time, and hidden neurons are added when validation performance indicates that additional model capacity is required.

The models were implemented using PyTorch.

## Evaluation

Performance was evaluated using:

- Accuracy
- Classification error
- Macro F1-score
- Balanced accuracy

Final experiments were repeated using random seeds 42, 123, and 456.

## Repository contents

`incremental_class_learning.ipynb` contains the full experimental workflow, including:

- Dataset loading and inspection
- Preprocessing
- Train, validation and test splitting
- Baseline neural-network selection
- Incremental class learning
- Hidden-layer growth
- Final testing
- Comparison of the two approaches

The `results/` folder contains the CSV files produced during the experiments.

## Author

Nicolaas Rossouw  
Stellenbosch University  
Student number: 26445298
