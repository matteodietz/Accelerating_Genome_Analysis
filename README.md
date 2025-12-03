# Accelerating Genome Analysis

**Author:** Matteo Dietz (as part of the SAFARI Research Group, ETH Zürich)

## Overview
This project benchmarks **in-storage file format conversion** to reduce I/O bottlenecks in genome analysis. By converting FastQ files to 2-bit binary encoding inside the SSD, we significantly reduce data movement and improve pipeline throughput.

## Structure
* `benchmarks/` – Shell scripts for reproducing I/O overhead tests.
* `docs/` – Methodology slides and PDF report.
* `results/` – Raw timing data.

## Key Results
Eliminating I/O overheads yielded the following speedups compared to standard FastQ processing:

| Mapper | SSD Type | Speedup |
| :--- | :--- | :--- |
| **GenCache / GEM (HW)** | SATA | **3.23x** |
| **GenCache (HW)** | PCIe Gen4 | **1.36x** |
| **Minimap2 (SW)** | SATA | **1.10x** |
