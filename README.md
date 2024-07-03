# CPU Performance Analysis: Matrix Multiplication Algorithms

## Project Overview

This project analyzes the impact of various matrix multiplication algorithms on CPU performance, focusing on processing large datasets. The study is divided into two parts, evaluating performance metrics in both single-core and multi-core environments.

## Algorithms Implemented

### Single-Core Variants
1. Column Matrix Multiplication
2. Line Matrix Multiplication
3. Block Matrix Multiplication

### Multi-Core Variants
1. OpenMP Parallelized Line Multiplication (Outer loop parallelization)
2. OpenMP Parallelized Line Multiplication with Nested Parallelism

## Languages Used
- C++
- Julia

## Performance Metrics
- Execution Time
- Cache Misses (L1 and L2)
- MFlops (for multi-core variants)
- Speedup (for multi-core variants)
- Efficiency (for multi-core variants)

## Key Findings

1. Line matrix multiplication consistently outperforms column matrix multiplication in terms of execution time and cache efficiency.
2. Block matrix multiplication shows superior performance compared to line multiplication, especially for larger matrices.
3. Parallel implementations demonstrate improved performance over sequential counterparts, with varying efficacy between different parallelization strategies.

## Tools Used
- PAPI API for gathering CPU performance metrics
- OpenMP for parallelization

## Project Team
- Adriano Machado (up202105352@up.pt)
- André Rodrigues (up202108721@up.pt)
- Daniel Dória (up202108808@up.pt)

## Course Information
- Course: Informatics and Computing Engineering
- Institution: FEUP
- Class: 3LEIC10
- Group: 11

## Conclusions

This project highlights the critical role of memory management in program efficiency. It demonstrates how optimizing data access patterns and understanding hardware configurations can significantly enhance performance, even without relying on parallel computing.

For more detailed information, please refer to the full project [report](docs/report.pdf).