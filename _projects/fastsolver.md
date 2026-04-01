---
title: "FastSolver: High-Performance Linear Algebra"
description: "GPU-accelerated library for solving large sparse linear systems with applications in scientific computing."
github: "https://github.com/example/fast-solver"
language: C++/CUDA
status: Active
tags: [numerical-methods, gpu, sparse-matrices]
---

## Overview

FastSolver is a high-performance library for solving sparse linear systems on GPU hardware. It provides significant speedups over CPU-based solvers while maintaining numerical accuracy.

## Key Features

- **GPU acceleration**: NVIDIA CUDA and AMD HIP support
- **Sparse formats**: COO, CSR, ELL format support
- **Preconditioners**: Jacobi, incomplete Cholesky, and AMG preconditioners
- **Iterative solvers**: CG, BiCG, GMRES, and LSQR methods
- **Mixed precision**: Float32 and Float64 support for memory efficiency

## Performance

Achieves 50-100x speedup over CPU solvers on modern GPUs for large problems (>1M unknowns).

## Building

```bash
git clone https://github.com/example/fast-solver.git
cd fast-solver
mkdir build && cd build
cmake -DENABLE_CUDA=ON ..
make
make install
```

## Example Usage

```cpp
#include <fastsolver/solver.h>

// Load sparse matrix in CSR format
auto matrix = fastsolver::load_csr_matrix("matrix.mtx");
auto rhs = fastsolver::load_vector("rhs.txt");

// Solve with GPU acceleration
fastsolver::CGSolver solver;
auto solution = solver.solve(matrix, rhs);
```

## Research Applications

- Finite element simulations
- Computational fluid dynamics
- Structural mechanics
- Electromagnetics
