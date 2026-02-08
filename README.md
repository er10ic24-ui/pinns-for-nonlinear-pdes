# Physics-Informed Neural Networks for Nonlinear PDEs

## Overview
This repository presents numerical experiments using Physics-Informed Neural Networks (PINNs) to solve nonlinear partial differential equations. Two representative problems are studied:
	•	a semilinear elliptic equation, solved using a standard PINN formulation
	•	the viscous Burgers equation, solved using a self-adaptive PINN

The goal of this project is to demonstrate correct PINN formulation, training, and qualitative accuracy for both stationary and time-dependent PDEs.

## Problems and Methods

### Semilinear Elliptic Equation
	•	Stationary nonlinear elliptic problem
	•	Solved using a standard PINN
	•	Loss function incorporates:
	•	PDE residual
	•	boundary conditions

This notebook serves as a baseline PINN implementation.

### Viscous Burgers Equation
	•	Time-dependent nonlinear PDE with viscosity
	•	Solved using a self-adaptive PINN
	•	Adaptive loss weighting is employed to balance:
	•	PDE residual
	•	initial condition
	•	boundary conditions

The self-adaptive strategy improves training stability compared to a standard PINN.

### Reference Solution for the Viscous Burgers Equation
The reference solution for the viscous Burgers equation is obtained from the file
`burgers_shock.mat`, which is commonly used as a benchmark dataset. For completeness
and reproducibility, a spectral method for computing the reference solution is also
provided in the notebook.

## Repository Structure
```
.
├── notebooks/
│   ├── Semilinear_elliptic_example.ipynb
│   └── Viscous_Burgers_SAPINN.ipynb
├── burgers_shock.mat   
├── README.md
```
## Numerical Results
	•	Both notebooks include:
	•	solution visualizations
	•	comparisons with reference solutions
	•	relative error
	•	Results are intended to demonstrate qualitative correctness rather than optimal numerical accuracy.

All experiments are performed in single precision (float32) for computational efficiency.



## Notes
	•	PINNs generate their own training data via collocation points; no external datasets are required.
	•	This repository focuses on methodology and implementation rather than theoretical convergence guarantees.
	•	Higher precision (float64) may further reduce error but is not required for demonstrating the PINN framework.

## References 
	•	M. Raissi, P. Perdikaris, G. E. Karniadakis, Physics-Informed Neural Networks: A Deep Learning Framework for Solving Forward and Inverse Problems
		Involving Nonlinear Partial Di erential Equations, Journal of Computational Physics, 2019.
	•	LD McClenny, UM Braga-Neto, Self-adaptive physics-informed neural networks,  Journal of Computational Physics, 2023.
	•	J. Sirignano, K. Spiliopoulos, DGM: A deep learning algorithm for solving partial differential equations, Journal of Computational Physics, 2018.

## Scope

This repository is intended as a methodological demonstration of PINNs for nonlinear PDEs and as part of a broader portfolio in scientific machine learning and numerical analysis.
