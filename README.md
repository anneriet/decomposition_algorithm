# Beyond Quantum Shannon: Circuit Construction for General n-Qubit Gates Based on Block ZXZ-Decomposition
This repository holds a Python notebook with an implementation of my decomposition algorithm. The full description can be found [in my published article](https://link.aps.org/doi/10.1103/PhysRevApplied.22.034019) (as well as on [arXiv](https://arxiv.org/abs/2403.13692)).

#### To use
The decomposition can be used to decompose general unitary matrices into quantum circuits. 
For an n-qubit unitary gate, the decomposition generates circuits with 22/48 4^n - 3/2 2^n + 5/3 CNOT gates, which is (4^(n−2)−1)/3 CNOT gates less than the previously best exact decomposition algorithm (quantum Shannon decomposition from Shende et al. (2006)).

To use, run the Python notebook in an environment with Qiskit, cmath and numpy. The code has been tested with Python 3.10 and Qiskit 0.44, but should also work with other Python and Qiskit versions (including Qiskit 1.0). 

The notebook uses some internal functions from the [Qiskit library](https://github.com/Qiskit/qiskit), it is mentioned in the markdown of the Python notebook which functions are (adapted) from Qiskit. 

### Paper abstract
This paper proposes a new optimized quantum block-_ZXZ_ decomposition method that results in more optimal quantum circuits than the quantum Shannon decomposition, wwhich was presented in 2005 by M. Möttönen, and J. J. Vartiainen \[in Trends in quantum computing research, edited by S. Shannon (Nova Science Publishers, 2006) Chap. 7, p. 149, arXiv:quant-ph/0504100\]. The decomposition is applied recursively to generic quantum gates, and can take advantage of existing and future small-circuit optimizations. Because our method uses only single-qubit gates and uniformly controlled rotation-Z gates, it can easily be adapted to use other types of multi-qubit gates. With the proposed decomposition, a general three-qubit gate can be decomposed using 19 CNOT gates (rather than 20). For general 𝑛-qubit gates, the proposed decomposition generates circuits that have 22/48 4^n - 3/2 2^n + 5/3  CNOT gates, which is less that the best-known exact decomposition algorithm by (4^(n−2)−1)/3 CNOT gates. 

### To cite
If you use this code, please cite the paper:
```
@article{PhysRevApplied.22.034019,
  title = {Beyond quantum Shannon decomposition: Circuit construction for $n$-qubit gates based on block-$ZXZ$ decomposition},
  author = {Krol, Anna M. and Al-Ars, Zaid},
  journal = {Phys. Rev. Appl.},
  volume = {22},
  issue = {3},
  pages = {034019},
  numpages = {7},
  year = {2024},
  month = {Sep},
  publisher = {American Physical Society},
  doi = {10.1103/PhysRevApplied.22.034019},
  url = {https://link.aps.org/doi/10.1103/PhysRevApplied.22.034019}
}
```

### License
[Apache License 2.0](https://github.com/anneriet/decomposition_algorithm/blob/main/LICENSE)


