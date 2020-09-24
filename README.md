# VQE_for_a_General_4X4_Hermitian_Matrix
My VQE code, built using Qiskit, that solves for the lowest eigenvalue of a General 4X4 Hermitian matrix

This is part of a task required for the "qosf QC Mentorship program". I chose to do Task 4, which require we build a VQE eigensolver from scratch for a given matrix. I decided to extend this to all Hermitian 4X4 Matrices.

## GUIDE:

This is done using Jupyter Notebook, so please run the cells in order. It is also preferable that one run the last cell too for aesthetics, it formats the notebook quite nicely.

## Aim of this code:
Our goal is to find the lowest eigenvalue of a given matrix. In terms of quantum hardware, this translates to the lowest energy $E_0$ of some Hamiltonian.
### 
## Steps:
#### 
### Quantum Part:
#### 
1. Translating the matrix into a qubit operator making it accessible to our quantum hardware
#### 
2. The quantum Bulding the ansatz circuit with some controllable parameters, which generates a tunable trial wavefunction on which we can apply our given qubit operator as a Hamiltonian. The ansatz circuit needs to be flexible enough to gain access to most of the N-qubit (in this case 2 qubit) Hilbert state space.
#### 
3. Measuring the expectation value of every pauli product term in the qubit operator (representing the Hamiltonian). This yields the energy of every term in the Hamiltonian, and we add them all up to generate the energy of the given trial state (ansatz) which we setup using a unique list of parameters.
#### 
### Classical part:
### 
3. Fine tune the ansatz circuit to find the lowest possible energy of this Hamiltonian. This is the classical optimization part, and is achievable through classical optimization techniques aimed at fine tuning the parameters of the ansatz. This step generates a modified ansatz circuit bringing us a step closer to the optimized trial wavefunction which approximates the ground state of the Hamiltonian.
#### 
On obtainig the ground state energy, we have ourselves the lowest eigenvalue of the Hamiltonian, which corresponds to the lowest eigenvalue of its matrix. 



