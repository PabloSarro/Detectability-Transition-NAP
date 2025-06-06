# Network Alignment Project – Functions and Plot Generation

This repository contains supporting code and data for my thesis project on **network alignment and its detectability phase transitions**. The repository is structured into modular components to facilitate the reproducibility of the results presented in the thesis.

---

## 📁 Repository Structure

- `functions.ipynb` / `functions.py`:  
  This file contains **all the core functions** used throughout the project. The functions are organized into three categories:
  
  - **Used Functions**:  
    These are the main functions used in the experimental pipeline (e.g., graph generation, posterior computation, MCMC sampling, etc.).

  - **Plotting Functions**:  
    Utility functions used to generate all figures included in the thesis, including statistical visualizations, phase transition diagrams, and performance comparisons.

  - **Auxiliary Functions**:  
    Helper utilities that assist the main procedures (e.g., renaming, reindexing, formatting, noise addition).

- `executions.ipynb` / `executions.py`:  
  This script/notebook **calls the main and plotting functions** from `functions` to generate the figures included in the thesis. Each code block typically corresponds to a specific figure or experimental result.

- `results_*.csv`:  
  These files contain the **raw results** from various experimental runs. The naming convention follows the format:  results_<noise_level>_<run>.csv

  For example, `results_0.25_1.csv` contains the first run with noise level `f = 0.25`.

---

## 📊 Usage and Reproducibility

To reproduce the plots and results from the thesis:

1. Ensure all required packages are installed (see [Dependencies](#dependencies)).
2. Open and run the code in `executions.ipynb` or execute `executions.py`.
3. Make sure that the corresponding `.csv` result files are present in the same directory.

You can also modify the functions in `functions.ipynb` to experiment with new parameter values, different posterior distributions, or alternative sampling strategies (e.g., with or without parallel tempering).

---

## 🧩 Dependencies

This project was built using Python 3. The main required libraries are:

- `numpy`
- `pandas`
- `matplotlib`
- `networkx`
- `scipy`
- `csv`
- `os`

All libraries are standard scientific Python packages.
