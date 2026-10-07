# MERLIN — Parameter-Free Discovery of Arbitrary-Length Time-Series Anomalies

> MVA (ENS Paris-Saclay) · Time-series course project (2022)
> **Team:** **Saifeddine Barkia**, Aymane Nohair

A Python re-implementation and study of **MERLIN** (Nakamura et al., ICDM 2020), an algorithm that finds anomalies (*discords*) of **every length** in large time series, without the user choosing a subsequence length.

## What's inside

- **From-scratch Python implementation** of DRAG and MERLIN, based on the paper's pseudo-code and the authors' MATLAB reference.
- **Extension:** generalised MERLIN to return the **top-k discords**, not only the top 1.
- **Experiments** on the paper's datasets: Yahoo A4 benchmark, ECG heartbeats, NYC taxi demand and a noisy sine signal (`data/`).
- **Report:** [`60.pdf`](./60.pdf). **Notebook:** [`60.ipynb`](./60.ipynb).

## Key idea

A *discord* is the subsequence that is farthest from its nearest non-overlapping neighbour. Classic discord search is very sensitive to its one parameter, the subsequence length. MERLIN removes that parameter: it searches all lengths efficiently, adapts the distance threshold automatically, and reuses the results for length L to find length L + 1 quickly.

**Stack:** Python · NumPy · Matplotlib · Jupyter
