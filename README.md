<div align="center">
  <img src="https://github.com/GitPhar/Quantum_Sudoku/blob/main/9d9ef8f0463d78c0567834e85b1acd78.webp" alt="Quantum Sudoku Logo" width="800" style="margin-left:'auto' margin-right:'auto' display:'block'"/>
  <br>
  <br>
  <h1>Quantum_Sudoku</h1>
</div>
<p align="center">
  <a href="https://github.com/GitPhar/Quantum_Sudoku/blob/main/LICENSE">
    <img alt="GitHub License" src="https://img.shields.io/github/license/GitPhar/Quantum_Sudoku">
  </a>
  <a href="https://github.com/GitPhar/Quantum_Sudoku/releases">
    <img alt="GitHub release" src="https://img.shields.io/github/release/GitPhar/Quantum_Sudoku.svg">
  </a>
  <a href="https://arxiv.org/pdf/2402.00838.pdf">
    <img alt="Paper URL" src="https://img.shields.io/badge/arxiv-2402.00838-blue">
  </a>
</p>

Quantum_Sudoku is an innovative project aimed at leveraging quantum annealing techniques to solve Sudoku puzzles quickly and efficiently. Utilizing the D-Wave Quantum Annealer, this project explores the potential of quantum computing in solving complex combinatorial problems.

## Key Features

- **Quantum Annealing**: The core technique involves quantum annealing, a quantum algorithm designed for solving optimization problems by finding the global minimum of a function.
- **D-Wave Quantum Annealer**: The project utilizes the D-Wave Quantum Annealer, a cutting-edge quantum computing device specifically designed for quantum annealing processes.
- **Sudoku Solver**: The primary application is solving Sudoku puzzles, a classic example of a constraint satisfaction problem that requires significant computational resources when approached with classical algorithms.

## Project Goals

1. **Develop a Quantum Sudoku Solver**: Implement a Sudoku solver that utilizes quantum annealing to find solutions rapidly.
2. **Benchmarking**: Compare the performance of the quantum-based solver against traditional Sudoku solving algorithms.
3. **Optimization**: Explore various techniques to optimize the mapping of Sudoku problems to the D-Wave architecture.
4. **Scalability**: Investigate the scalability of the solution and its applicability to other combinatorial optimization problems.

## Technical Approach

1. **Problem Representation**: Represent Sudoku puzzles as a quadratic unconstrained binary optimization (QUBO) problem suitable for quantum annealing.
2. **Embedding on D-Wave**: Develop an efficient embedding of the QUBO problem onto the D-Wave hardware, ensuring optimal use of available qubits and connectivity.
3. **Quantum Annealing Execution**: Execute the quantum annealing process on the D-Wave Quantum Annealer to solve the Sudoku puzzles.
4. **Result Analysis**: Analyze the solutions provided by the quantum annealer, validate their correctness, and measure the time taken compared to classical methods.

## Tools and Technologies

- **D-Wave Quantum Annealer**: The primary quantum computing hardware used for this project.
- **Python**: The main programming language for developing the Sudoku solver and interfacing with the D-Wave API.
- **D-Wave Ocean SDK**: A software development kit provided by D-Wave for interacting with their quantum annealers.
- **NumPy and SciPy**: Libraries for numerical computations and optimizations.

## Expected Outcomes

- **Functional Quantum Sudoku Solver**: A fully functional Sudoku solver utilizing quantum annealing.
- **Performance Insights**: Detailed insights into the performance benefits and limitations of quantum annealing for Sudoku puzzles.
- **Research Contributions**: Contributions to the field of quantum computing and combinatorial optimization through published research findings.

## Future Directions

- **Expand Problem Scope**: Apply quantum annealing techniques to other types of combinatorial optimization problems.
- **Hybrid Solutions**: Develop hybrid quantum-classical algorithms to leverage the strengths of both computing paradigms.
- **Community Collaboration**: Engage with the quantum computing community to share findings, collaborate on further research, and enhance the project's capabilities.

## Conclusion

Quantum_Sudoku aims to push the boundaries of what's possible with quantum computing by solving one of the most popular and challenging puzzles. By utilizing the D-Wave Quantum Annealer, this project seeks to demonstrate the practical applications of quantum annealing in solving real-world problems efficiently.

## Getting Started

### Prerequisites

To run this project, you need the following:

- Access to a D-Wave Quantum Annealer.
- Python 3.x installed on your machine.
- D-Wave Ocean SDK installed. You can install it using pip:
  ```bash
  pip install dwave-ocean-sdk
  ```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/GitPhar/Quantum_Sudoku.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Quantum_Sudoku
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Prepare your Sudoku puzzle input in the required format.
2. Run the Sudoku solver script:
   ```bash
   python sudoku_solver.py
   ```
3. The solution will be displayed in the console and saved to an output file.

### Example

Here is an example of how to use the Quantum Sudoku Solver:

```python
from dwave.system import DWaveSampler, EmbeddingComposite
import numpy as np

# Define your Sudoku puzzle here
sudoku_puzzle = [
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    [0, 9, 8, 0, 0, 0, 0, 6, 0],
    [8, 0, 0, 0, 6, 0, 0, 0, 3],
    [4, 0, 0, 8, 0, 3, 0, 0, 1],
    [7, 0, 0, 0, 2, 0, 0, 0, 6],
    [0, 6, 0, 0, 0, 0, 2, 8, 0],
    [0, 0, 0, 4, 1, 9, 0, 0, 5],
    [0, 0, 0, 0, 8, 0, 0, 7, 9]
]

# Initialize the D-Wave sampler
sampler = EmbeddingComposite(DWaveSampler())

# Convert the Sudoku puzzle to QUBO format and solve using the D-Wave sampler
# (Implementation details would be in the sudoku_solver.py script)

print("Solved Sudoku:")
print(np.array(sudoku_solution))
```

## Contributing

We welcome contributions to the Quantum_Sudoku project. If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

We would like to thank D-Wave Systems for providing the quantum annealing technology and tools that make this project possible.

---

Feel free to reach out if you have any questions or need further assistance. Happy solving!
