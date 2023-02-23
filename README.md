# QHackOpenHackathon
The Entangled Cats repository for 2023 QHack Challenge

Our idea is to look at the BeH2 molecule, (which requires 12 qubits to evolve (considering a frozen core on Be, although this number can be brought even further down by freezing more orbitals (so far, we believe the minimum to be 8 qubits)) and obtain the ground state energy using VQE (possibly adapt-VQE) first on the IBM Power up.  from the codding challenges (which gives access to 7 qubits) through circuit knitting and entanglement forging. This will allow us to compare these 2 new techniques. Then we want to compare the result with the evolution on a QPU with more than 12 qubits, and see if these 2 techniques have a meaningful impact on the calculated ground state energy, or no. To implement circuit knitting and entanglement forging we are using the Circuit Knitting Toolbox (https://qiskit-extensions.github.io/circuit-knitting-toolbox/index.html) and following these articles:  https://arxiv.org/abs/2205.00016, https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.3.010309, https://arxiv.org/abs/2205.00933. If the results are positive this could pave the way for obtaining ground state energies of more complex molecules like CO2 in current NISQ.

As a last step, we plan to loop through the VQE using the different qubit mappers available on qiskit (currently using JordanWignerMapper) and see how the different maps affect the introduction of errors. Error mitigation techniques available on qiskit runtime will be used, and as a final touch we intend to see if a simple VQE after a CNOT can be used to predict errors and correct them.

Done so Far:
Molecule is defined;
Analitical solution obtained;
Ideal simulation run (error 0.2 %);

To do:
Noisy simulation;
Circuit Knitting;
Entanglement Forging;
VQE Error correction;
