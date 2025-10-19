Sliding Puzzle Solver
Implementation of A* and IDA* algorithms for solving the sliding puzzle problem (also known as the 15-puzzle or n-puzzle).
📋 Features

Two Algorithm Implementations:

A* (A-star) Algorithm
IDA* (Iterative Deepening A*) Algorithm


Multiple Heuristics:

Manhattan Distance
Hamming Distance


Flexible Board Sizes:

3x3 (8-puzzle)
4x4 (15-puzzle)
5x5 (24-puzzle)


Automatic Features:

Random solvable board generation
Solvability checking
Step-by-step solution visualization
Performance statistics



🚀 Usage
Basic Example
python# Solve a 3x3 puzzle with A* and Manhattan heuristic
solve_puzzle(size=3, algorithm='astar', heuristic='manhattan')

# Solve a 4x4 puzzle with IDA* and Hamming heuristic
solve_puzzle(size=4, algorithm='idastar', heuristic='hamming')
Parameters

size: Board size (3, 4, or 5)
algorithm: 'astar' or 'idastar'
heuristic: 'manhattan' or 'hamming'
initial_board: Custom initial configuration (None for random)
show_solution: Display step-by-step solution (True/False)

Custom Initial Board
python# Define custom 3x3 board (0 represents empty tile)
custom_board = [1, 2, 3, 4, 0, 5, 7, 8, 6]

# Solve custom board
solve_puzzle(size=3, initial_board=custom_board, algorithm='astar', heuristic='manhattan')
📊 Output Information
The solver provides:

Initial and goal states
Algorithm used and heuristic type
Number of nodes expanded
Solution length (number of moves)
Time elapsed
Step-by-step solution path with g, h, and f values

🧮 Algorithm Details
A* Algorithm

Uses priority queue to explore states
Evaluates states using f(n) = g(n) + h(n)
Guarantees optimal solution with admissible heuristic
More memory intensive but typically faster

IDA* Algorithm

Iterative deepening depth-first search
Uses less memory than A*
May revisit states multiple times
Better for larger puzzles with memory constraints

Heuristics
Manhattan Distance: Sum of horizontal and vertical distances of each tile from its goal position. Generally more informative.
Hamming Distance: Number of tiles in wrong positions. Simpler but less informative.
📦 Installation
Google Colab (Recommended)

Open Google Colab
Create new notebook
Copy the solver code into a cell
Run the cell

Local Installation
bash# Clone repository
git clone https://github.com/yourusername/sliding-puzzle-solver.git
cd sliding-puzzle-solver

# No additional dependencies required (uses only standard library)
python sliding_puzzle_solver.py
📝 Requirements

Python 3.7+
Standard library only (heapq, time, typing, random)

🎯 Examples
Example 1: Quick 3x3 Solve
pythonsolve_puzzle(size=3, algorithm='astar', heuristic='manhattan', show_solution=True)
Example 2: 4x4 with Statistics Only
pythonsolve_puzzle(size=4, algorithm='idastar', heuristic='hamming', show_solution=False)
Example 3: Custom Board
pythonboard = [5, 1, 3, 4, 2, 6, 7, 8, 0]
solve_puzzle(size=3, initial_board=board, algorithm='astar', heuristic='manhattan')
📚 References

Hart, P. E., Nilsson, N. J., & Raphael, B. (1968). A Formal Basis for the Heuristic Determination of Minimum Cost Paths. IEEE Transactions on Systems Science and Cybernetics.
Korf, R. E. (1985). Depth-First Iterative-Deepening: An Optimal Admissible Tree Search. Artificial Intelligence.
Red Blob Games - A* Pathfinding Tutorial

📄 License
This project is open source and available for educational purposes.
👤 Author
[Your Name]
🤝 Contributing
Contributions, issues, and feature requests are welcome!
