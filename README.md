# Accelerating Genome Analysis

**Author:** Matteo Dietz (SAFARI Research Group, ETH Zürich)

## Overview
[cite_start]This project benchmarks **in-storage file format conversion** to reduce I/O bottlenecks in genome analysis[cite: 14, 16]. [cite_start]By converting FastQ files to 2-bit binary encoding inside the SSD, we significantly reduce data movement and improve pipeline throughput[cite: 17, 108].

## Structure
* `benchmarks/` – Shell scripts for reproducing I/O overhead tests.
* `docs/` – Methodology slides and PDF report.
* `results/` – Raw timing data.

## Key Results
[cite_start]Eliminating I/O overheads yielded the following speedups compared to standard FastQ processing[cite: 18, 19, 211]:

| Mapper | SSD Type | Speedup |
| :--- | :--- | :--- |
| **GenCache / GEM (HW)** | SATA | **3.23x** |
| **GenCache (HW)** | PCIe Gen4 | **1.36x** |
| **Minimap2 (SW)** | SATA | **1.10x** |
