This repository contains the full pipeline for generating numerical simulations to particle-laden flows as used in the research paper 'A comparative study of dynamic models for gravity-driven particle-laden flows', published at Applied Mathematics Letters, 2025 (see https://authors.elsevier.com/c/1kaYY3BGwfPgHq).

The original code was written using Jupyter Notebook and can be found in particle-laden-flow/notebook-code. Each file is written to allow contiguous execution.

The pipeline contains three parts:

Part 1 generates the numerical conservation law fluxes from solutions to the equilibrium equations (8) and (11) in the paper. It is used to create Figure 2.
File: particle-laden-flow/notebook-code/equilibrium-ode-solver.ipynb

Part 2 solves the conservation law system (12) and stores the computed liquid and particle front data used for Part 3.
File: particle-laden-flow/notebook-code/conservation-law-pde-solver.ipynb

Part 3 plots the numerical simulations of fluid fronts against experimental data as in Figure 4 of the paper.
File: particle-laden-flow/notebook-code/plot-generator.ipynb
 

Python packages and modules required:
NumPy (https://numpy.org), Matplotlib (https://matplotlib.org), Matplotlib-label-lines (https://zenodo.org/records/7428071, see also https://github.com/cphyc/matplotlib-label-lines), tqdm (https://tqdm.github.io/), and SciPy (https://scipy.org/)

This code was developed by Wing Pok Lee, Jonathan Woo, Luke Triplett, and Yifan Gu with assistance from Hong Kiat Tan.

If you use our code for academic research, we would appreciate it if you could cite our paper:

```bibtex
@article{lee2025comparative,
  title={A comparative study of dynamic models for gravity-driven particle-laden flows},
  author={Lee, Wing Pok and Woo, Jonathan D and Triplett, Luke F and Gu, Yifan and Burnett, Sarah C and Ding, Lingyun and Bertozzi, Andrea L},
  journal={Applied Mathematics Letters},
  pages={109480},
  year={2025},
  publisher={Elsevier}
}
