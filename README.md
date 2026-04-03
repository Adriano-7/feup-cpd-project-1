# CPU Performance Analysis

> **Project**
> <br />
> Course Unit: [Computação Paralela e Distribuída](https://sigarra.up.pt/feup/pt/ucurr_geral.ficha_uc_view?pv_ocorrencia_id=520333)
> <br />
> Course: Informatics and Computing Engineering
> <br />
> Faculty: **FEUP** (Faculty of Engineering of the University of Porto)
> <br />
> Report: [Full Project Report](./doc/report.pdf)
> <br />
> Project evaluation: **16**/20

---

## Project Goals

This project provides an analysis of the impact of various matrix multiplication algorithms on CPU performance. By implementing several variants in both **C++** and **Julia**, we explore how memory access patterns, cache efficiency, and multi-core parallelization strategies influence execution time.

## Technical Approach

### 1. Single-Core Variants
We implemented and tested three fundamental algorithms:
*   **Column Multiplication:** The conventional approach, useful as a baseline.
*   **Line Multiplication:** Reorders nested loops to optimize data locality, significantly reducing cache misses compared to the column-based approach.
*   **Block Multiplication:** Further optimizes memory management by processing sub-matrices, effectively staying within CPU cache capacities for larger datasets.

### 2. Multi-Core Variants (OpenMP)
We developed two parallel strategies to maximize throughput on multi-core systems:
*   **Implementation 1 (Outer Loop Parallelization):** Uses `#pragma omp parallel for` to distribute iterations of the outer loop across available threads.
*   **Implementation 2 (Nested Parallelism):** Establishes a parallel region and targets the innermost loop for parallel execution. Our analysis shows how this strategy, while sophisticated, experiences diminishing returns due to overhead on larger matrices.

## Performance Metrics

To ensure accuracy, we leveraged the **PAPI API** to track hardware performance counters.

| Metric | Purpose |
| :--- | :--- |
| **Execution Time** | Primary indicator of performance efficiency. |
| **L1/L2 Cache Misses** | Tracks cache locality and memory hierarchy efficiency. |
| **MFlops** | Measures computational throughput. |
| **Speedup/Efficiency** | Evaluates the scalability of our multi-core implementations. |

## Project Structure
*   `/src`: Contains the source code for the C++ and Julia implementations.
*   `/doc`: Contains the detailed performance results in CSV format and the final project report.

## Team
- **Adriano Machado** (up202105352)
- **André Rodrigues** (up202108721)
- **Daniel Dória** (up202108808)

---
*Course: 3LEIC10 | Group 11*
