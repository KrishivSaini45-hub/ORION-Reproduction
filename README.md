# ORION Table I Reproduction

## Overview

This repository contains my reproduction of **Table I** from the paper:

> **ORION: Option-Regularized Deep Reinforcement Learning for Cooperative Multi-Agent Online Navigation**

The goal of this project is to reproduce the experimental results reported in the original paper and understand the underlying implementation.

---

## Features

- Reproduced the evaluation pipeline for Table I
- Verified the official implementation
- Investigated the ORION architecture
- Documented implementation details
- Prepared the ROS2 setup required for Table II

---

## Repository Structure
ORION/
│
├── agent.py
├── driver.py
├── env.py
├── test_driver.py
├── test_worker.py
├── parameter.py
├── model/
├── maps_GT/
├── maps_priori/
├── reproduced_results/
├── results/
└── README.md


---

## Environment

- Ubuntu 22.04
- Python 3.10
- PyTorch
- NumPy

---

## Installation

```bash
git clone https://github.com/KrishivSaini45-hub/ORION-Reproduction.git
cd ORION-Reproduction
pip install -r requirements.txt


## Running Evaluation
python test_driver.py

## Results

🚧 This section will be updated after completing the final evaluation and analysis.

## Future Work
Complete detailed analysis of Table I
Reproduce Table II
Compare reproduced metrics with the original paper
Perform additional statistical evaluation

## Acknowledgements
This project is based on the official ORION implementation provided by the original authors.

Paper:
ORION: Option-Regularized Deep Reinforcement Learning for Cooperative Multi-Agent Online Navigation
