# VQE_for_a_General_4X4_Hermitian_Matrix
My VQE code, built using Qiskit, that solves for the lowest eigenvalue of a General 4X4 Hermitian matrix

## GUIDE:

Optimal viewing is achieved if the reader downloads the code themselves and views it on their PC. The Github viewer seems to not be the best sorry :') 

This is done using Jupyter Notebook, so please run the cells in order. It is also preferable that one run the last cell too for aesthetics, it formats the notebook quite nicely.

## Aim of this code:
Our goal is to find the lowest eigenvalue of a given matrix. In terms of quantum hardware, this translates to the lowest energy E_0 of some Hamiltonian.
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

# KEY RESULTS :

The Qubit String of the matrix given in the task:  
  
![Qubit string](https://github.com/Hish-am/VQE_for_a_General_4X4_Hermitian_Matrix/blob/master/Sneak%20peek%20at%20results/Qubit_string.JPG)  

The Circuit Ansatz with 8 paramterization angles:  

![Ansatz](https://github.com/Hish-am/VQE_for_a_General_4X4_Hermitian_Matrix/blob/master/Sneak%20peek%20at%20results/ansatz_circuit.JPG)  

The Final result after optimization to get the lowest eigenvalue of the matrix, which should be -1:  

![Lowest Eigenvalue](https://github.com/Hish-am/VQE_for_a_General_4X4_Hermitian_Matrix/blob/master/Sneak%20peek%20at%20results/Lowest_Eigenvalue.JPG)  







