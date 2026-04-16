# emerging-technologies
# Deutsch–Jozsa Algorithm: Quantum vs Classical Computing

Exploring quantum advantage through a complete implementation of the Deutsch–Jozsa algorithm using Qiskit.

## What This Project Does

This repository walks through the Deutsch–Jozsa problem step by step, starting with classical Boolean functions and ending with a fully working quantum circuit that solves the same problem in a single query. Along the way I implement classical oracles, quantum oracles, Deutsch's single-input algorithm, and finally the full Deutsch–Jozsa algorithm for four-bit functions — then compare the quantum and classical approaches directly.

## The Journey

### Problem 1: Generating Random Boolean Functions
Built a function that randomly generates either a constant or balanced four-bit Boolean function. Constant functions always return the same value, while balanced functions return True for exactly half of all possible inputs. These serve as the test cases for everything that follows.

### Problem 2: Classical Testing
Implemented a classical algorithm to determine whether a function is constant or balanced. In the worst case, you need to query more than half the inputs to be 100% certain — for four-bit functions that means up to 9 queries out of 16 possible inputs.

### Problem 3: Quantum Oracles
Built quantum oracles for all four single-input Boolean functions used in Deutsch's algorithm. Each oracle encodes a classical function as a reversible quantum operation using the standard phase kickback structure.

### Problem 4: Deutsch's Algorithm
Implemented Deutsch's algorithm in Qiskit — the simplest quantum algorithm that outperforms any classical approach. It determines whether a single-input function is constant or balanced using just one oracle query, compared to two classically.

### Problem 5: Scaling to Deutsch–Jozsa
Generalised the approach to four-bit functions. The Deutsch–Jozsa algorithm solves the same problem with a single oracle query regardless of how many input bits the function takes — a gap that grows exponentially with input size classically.

## Running the Code

### GitHub Codespaces
This project was built using GitHub Codespaces:

1. Fork or clone this repository
2. Click the green "Code" button → "Codespaces" → "Create codespace on main"
3. Wait for the environment to load
4. Open `problems.ipynb` in the Codespaces Jupyter interface
5. Run all cells in order from top to bottom

### Local Setup
```bash
git clone https://github.com/mohelmahi02/emerging-technologies
cd emerging-technologies
pip install -r requirements.txt
jupyter notebook problems.ipynb
```

## What I Learned

Implementing these algorithms from scratch made the quantum advantage feel real rather than abstract. Classically, determining a function's type requires querying it multiple times — but the quantum circuit uses superposition and interference to extract a global property of the function in a single step. The Deutsch–Jozsa algorithm is often called a toy problem, but it genuinely demonstrates something that no classical algorithm can match.

**Course**: Emerging Technologies  
**Institution**: ATU Galway