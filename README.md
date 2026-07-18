# ORION Table I Reproduction

## Overview

This repository contains my reproduction of **Table I** from the paper:

> **ORION: Option-Regularized Deep Reinforcement Learning for Cooperative Multi-Agent Online Navigation**

The goal of this project is to reproduce the experimental results reported in the original paper and understand the underlying implementation.

---

## Project Files

| File/Folder | Description |
|-------------|-------------|
| `driver.py` | Trains the ORION model from scratch using the configured datasets and parameters.|
| `test_driver.py` | Runs evaluation to reproduce the results reported in Table I. |
| `agent.py` | Implements the ORION agent, including observation processing and action selection. |
| `env.py` | Simulates the multi-robot exploration environment and reward mechanism. |
| `test_worker.py` | Executes evaluation episodes in parallel during testing. |
| `parameter.py` | Stores all configurable hyperparameters and experiment settings. |
| `model/` | Contains the neural network architecture used by ORION. |
| `maps_GT/` | Stores ground-truth occupancy maps used by the simulator. |
| `maps_priori/` | Stores prior occupancy maps available before exploration begins. |
| `results/` | Contains training logs and evaluation outputs. |
| `reproduced_results/` | Stores reproduced experimental results for different team sizes. |
| `checkpoints/` | Contains pretrained model checkpoints used for evaluation (if available). |

---

## Repository Structure

```text
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
```


## Requirements

- Ubuntu 22.04
- Python 3.10
- PyTorch
- CUDA (optional)


## Installation

Clone the repository:

```bash
git clone https://github.com/KrishivSaini45-hub/ORION-Reproduction.git
cd ORION-Reproduction/ORION
```

### Create a virtual environment

```bash
python3 -m venv orion_env
source orion_env/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Datasets and Checkpoints
**Training datasets** are provided in:
- `maps_priori/`
- `maps_GT/`

**Evaluation datasets** are provided in:
- `maps_priori_test_new_{n}/`
- `maps_GT_test_new_{n}/`

where `{n}` denotes the number of agents in the team.

The training set consists of **simple maps with 3 agents only**.  
During evaluation, ORION scales to **larger teams (3, 4, 5, and 10 agents)** and **more complex environments** without additional training.



### Configure the Experiment

Modify `parameter.py` to set:
- Number of agents
- Checkpoint path
- Test dataset
- Evaluation parameters

### Run Table I Reproduction

```bash
python test_driver.py
```

### Train the ORION Model

```bash
python driver.py
```

---

## Reference

This reproduction is based on the official implementation released by the authors.

**Paper:**

> ORION: Option-Regularized Deep Reinforcement Learning for Cooperative Multi-Agent Online Navigation
