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
