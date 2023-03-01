# Digital-analog Variational Quantum Eigensolver

Womanium Hackathon 2022 Salada Bowl team project

*A challenge provided by IQM Quantum Computers*

This repository contains solution artifacts submitted by Salada Bowl team for the Womanium hackathon 2022.

## 1.Team Name - Salada Bowl

## 2. Team Members
* Atsushi Ueda (Discord id - aueda#6800, Github id - darts)
* Prashant Sharma (Discord id - sharmap#7046, Github id - nanophile)
* Nihir Chadderwala (Discord id - Jafi#8361, Github id - nihirc)
* Razeen Shuja (Discord id - Razeen#8475, Github id - Razeen-ud-din)
* Luis Ayala (Discord id - Luis Gerardo Ayala B.#3006, Github id - LuGerAyala)
* Saba Bozpolat (Discord id - saba#6364, Github id - sbbzplt)

## 3. Pitch Presenter - Saba Bozpolat

## 4. Digital-analog Variational Quantum Eigensolver --> by IQM
https://github.com/iqm-finland/iqm-academy-womanium-hackathon-DAQC-VQE

## 5. Summary
 [Taken from the IQM challenge github and modified by A.U and P.S]
 
  An important task in quantum chemistry and condensed matter physics is to find the ground state energy of the system in question. From the computational point of view, this corresponds to solving the minimal eigenvalue of the Hamiltonian of the system. The Variational Quantum Eigensolver algorithm (VQE) is one way to estimate this minimal eigenvalue that can be executed on a near-term intermediate-scale quantum computation (NISQ) device.
  
  ![digital_full](https://user-images.githubusercontent.com/101638759/186098060-52121615-3a61-4216-bd27-6150ee9a6599.png)


  It is a variational eigensolver, the parameters of which are used to construct a trial quantum state by quantum circuits. These parameterized quantum circuits are called ansatz and consist of several quantum gates, as shown in the figure. The created trial state $\ket{\psi(\vec{\theta)}}$ is then used to measure the expectation value of the Hamiltonian $E(\vec{\theta})$ as 
$$E(\vec{\theta})=\frac{\bra{\psi(\vec{\theta})}\hat{H}\ket{\psi(\vec{\theta})}}{\langle\psi(\vec{\theta})|\psi(\vec{\theta})\rangle}.$$
The parameters $\vec{\theta}$ are iteratively optimized so that $E(\vec{\theta})$ takes the lower value until it converges. In previous studies, this type of VQEs is shown to correctly find the ground state energy of several molecules under noise-free conditions with sufficient numbers of digital gates in the ansatz(digital VQE).

However, in the NISQ era the noise introduced by gates is a problem, and digital-VQEs are no exception. To tackle this problem, A. Parra-Rodriguez et al. introduced the notion of Digital-Analog Quantum Computing (DAQC) that allows us to reduce the number of gates needed to perform quantum algorithms. It combines digital single qubit gates with analog multi-qubit blocks. VQE is one of the algorithms, where DAQC has the potential to be “more hardware efficient” and thus allow for better ground state energy estimation than purely digital quantum computing in the NISQ era. \
  In this paper, we introduce a new type of VQE ansatz called digital-analog variational quantum eigensolver(DA-VQE) based on digital-analog quantum computing. We show that, for certain digital quantum circuits, we can construct the exactly equivalent digital-analog circuits with fewer gates. Adopting these circuits as the ansatz allows us to compare the performance of DA-VQEs and digital-VQEs. As a result, our simulation on qiskit indicates that DA-VQE indeed outperform digital-VQE under noisy conditions.\
  Moreover, we propose a new application of VQE, quantum machine learning. While the VQE has been successful in quantum chemistry as a quantum algorithm, the applications to the other fields have been limited. We demonstrate that the complex entangled nature of the ground-state wave function is capable of encoding information and of being used as a prediction model. As our VQE-based machine learning can classify both classical and quantum train data, we believe that it will be a new playground for quantum computing.

## 6. File description

### DA_VQE.py (Module)
Python module that has necessary functions such as loading molecule data and exact eigensolvers.

### Digital_Analog_VQE.ipynb(main result) 
Digitai_Analog_VQE(Ising).ipynb

Implementation and Application of digital-analog VQEs to Quantum Chemistry. (H2, LiH, BeH2)

### DA_VQE_LiH.ipynb(Atomic distance optimization)
Optimal interatomic distance is investigated by using digital-analog VQE developped in “Digital_Analog_VQE.ipynb."

### VQE_compare.ipynb(comparison)
Comparison of digital-analog VQEs with digital VQEs with/without noise. The equivalence of digital and analog gates and the difference in performance are demonstrated.

### Machine_learning_with_DAVQE.ipynb(VQE-based algorithm of machine learning)
datasetA.npy and datasetB.npy 

VQE-based supervised machine learning algorithm that we developped. “datasetA.npy" and “datasetB.npy” are the train data of distinct probabilistic distributions, and in the main file, we creat a quantum-machine-learning prediciton model.

### DA_VQE_qiskit_ml.ipynb(Comparison of various optimizations)
The convergence of the energy depending on different choices of optimizers are discussed.

### Presentation.pdf
Contains presentation deck

### manuscript.pdf
Directly sent to Stefan Seegerer.
