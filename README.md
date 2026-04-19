# BIM-Perturbed-Production-Planning-MILP-

This project is a replication and extension of the BIM production planning problem with perturbed data, originally presented in the AMPL MO-book:

https://ampl.com/mo-book/notebooks/03/bim-perturbed.html

The goal of this project is to demonstrate a solid understanding of:
Linear Programming (LP)
Mixed-Integer Linear Programming (MILP)
Mathematical modeling in AMPL
Sensitivity of optimal solutions to parameter perturbations
Integer vs fractional decision-making in optimization

# Problem Description
A production company manufactures two types of microchips under limited resources (silicon, germanium, plastic, and copper). Due to a 1% material loss (perturbation effect), the copper constraint is adjusted, leading to a modified linear optimization model. The decision variables represent:
x1 : number of logic chips produced
x2: number of memory chips produced
The objective is to: Maximize total profit while respecting resource constraints.

Linear Programming Model (Relaxed Form)

Maximize:12x1 +9x2
	​Subject to: Silicon: x1 ≤1000
  Germanium: x2≤1500
  Plastic: x1+x2≤1750
  Copper (perturbed): 4.04x1+2.02x2≤4800
  x1,x2>=0
  
# Mixed-Integer Linear Programming (MILP)

To reflect real-world production constraints (integer chips only):
  x1,x2∈Z≥0

# Project Insight
The LP relaxation produces a fractional solution:
(x1,x2)≈(626.238,1123.762)
However, real production requires integer decisions, so solving the MILP gives:
(x1,x2)=(626,1124)
This highlights an important MILP concept: The LP relaxation solution is not always feasible or optimal for the integer problem.



	​

	​

≥0
