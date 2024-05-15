# Beyond Quantum Shannon: Circuit Construction for General n-Qubit Gates Based on Block ZXZ-Decomposition
This repository holds a Python notebook with my implemented decomposition algorithm, which is published (here)[https://arxiv.org/abs/2403.13692].

#### To use
The decomposition can be used to decompose unitary matrices into a quantum circuit. 
For an n-qubit unitary gate, the decomposition generates circuits with 22/48 4^n - 3/2 2^n + 5/3 CNOT gates, which is (4^(n−2)−1)/3 CNOT gates less than the previously best exact decomposition algorithm (quantum Shannon decomposition from Shende et al. (2006)).

To use, run the python notebook in an environment with Qiskit, cmath and numpy. The code has been tested with Python 3.10 and Qiskit 0.44, but should also work with other Python and Qiskit versions (including Qiskit 1.0). I have used (and/or adapted) some functions from the (Qiskit library)[https://github.com/Qiskit/qiskit], it is mentioned in the markdown of the Python notebook which functions are (adapted) from Qiskit. 

### Paper abstract
The paper proposes a new optimized quantum block-ZXZ decomposition method [7,8,10] that results in more optimal quantum circuits than the quantum Shannon decomposition (QSD)[27], which was introduced in 2006 by Shende et al. The decomposition is applied recursively to generic quantum gates, and can take advantage of existing and future small-circuit optimizations. Because our method uses only one-qubit gates and uniformly controlled rotation-Z gates, it can easily be adapted to use other types of multi-qubit gates. With the proposed decomposition, a general 3-qubit gate can be decomposed using 19 CNOT gates (rather than 20). For general n-qubit gates, the proposed decomposition generates circuits that have 22/48 4^n - 3/2 2^n + 5/3  CNOT gates, which is less that the best known exact decomposition algorithm by (4^(n−2)−1)/3 CNOT gates. 

### To cite
If you use this code, please cite the paper:
`
@misc{krol2024quantum,
      title={Beyond Quantum Shannon: Circuit Construction for General n-Qubit Gates Based on Block ZXZ-Decomposition}, 
      author={Anna M. Krol and Zaid Al-Ars},
      year={2024},
      eprint={2403.13692},
      archivePrefix={arXiv},
      primaryClass={quant-ph}
}`

### License
(Apache License 2.0)[https://github.com/anneriet/decomposition_algorithm/blob/main/LICENSE]


