# ORION Reproduction Log

Research Paper:
ORION: Option-Regularized Deep Reinforcement Learning for Cooperative Multi-Agent Online Navigation

Researcher:
Krishiv Saini

Start Date:
1 July 2026

------------------------------------

Experiment 1
-------------
Goal:
Verify ORION testing pipeline.

Configuration:
| Test: 09_30_0.051
| Total test: 1
| Number of agents: 3
| Average max length: 485.98497075643724
| Std max length: 0.0
| Average min length: 437.27238841694407
| Std min length: 0.0
| Average mean distance: 456.64287381027793
| Std mean distance: 0.0
| Average explored rate: 0.7128145555014835
| Average success rate: 1.0
| Fail episode number: []
| Average total step: 59.0


Status:
PASS


------------------------------------

Experiment 2
------------

Goal:
Reproduce ORION results for 3 agents.

Configuration:
Test: 09_30_0.051
Total test: 5
Number of agents: 3
Checkpoint Episode: 49984

Results:
Average max length: 580.6306875465356
Std max length: 144.73036094695013

Average min length: 388.86487793026544
Std min length: 62.647012222287586

Average mean distance: 472.1316688068529
Std mean distance: 79.80995507635943

Average explored rate: 0.7317578609330968

Average success rate: 1.0

Fail episode number: []

Average total step: 71.0

Status:
PASS


Experiment 3

Agents: 3
NUM_TEST: 10

Average Max Distance: 505.06
Average Mean Distance: 427.22
Average Min Distance: 368.75
Average Total Steps: 61.7
Average Success Rate: 1.0

Observation:
Results are reasonably close to the paper but show higher travel distance and steps. Additional test episodes may reduce variance and improve agreement.




------------------------------------

Experiment 4
------------

Goal:
Reproduce Table I (3-Agent ORION Evaluation)

Configuration:
Checkpoint: 09_30_0.051
Agents: 3
NUM_TEST: 20
MAX_EPISODE_STEP: 128

Results:
Average Max Distance : 459.1932408918
Std Max Distance : 126.21979597034604

Average Min Distance : 338.11754011554484
Std Min Distance : 67.96478804992327

Average Mean Distance : 394.1915309447092
Std Mean Distance : 82.02981477345284

Average Explored Rate : 0.7031901078062377

Average Success Rate : 1.0

Average Total Step : 55.75

Comparison with Paper:
Paper Max Distance : 455.83 ± 108.51
Reproduced Max Distance : 459.19 ± 126.22

Paper Steps : 55.36
Reproduced Steps : 55.75

Observation:
The reproduced 3-agent evaluation closely matches the published ORION results. The reproduced Maximum Distance and Total Steps differ by less than 1% from the values reported in Table I.

Status:
PASS


| Metric            |         ORION Paper |   Reproduced Result |          Difference |  Status |
| ----------------- | ------------------: | ------------------: | ------------------: | :-----: |
| Max Distance (m)  | **455.83 ± 108.51** | **459.19 ± 126.22** | **+3.36 m (0.74%)** | ✅ Match |
| Mean Distance (m) |                   — |  **394.19 ± 82.03** |                   — |    —    |
| Min Distance (m)  |                   — |  **338.12 ± 67.96** |                   — |    —    |
| Explored Rate     |                   — |          **0.7032** |                   — |    —    |
| Success Rate      |            **100%** |            **100%** |              **0%** | ✅ Match |
| Total Steps       |           **55.36** |           **55.75** |   **+0.39 (0.70%)** | ✅ Match |




Experiment 5
------------

Date:
5 July 2026

Goal:
Prepare the Gazebo simulation environment for reproducing Table II.

Work completed:
✓ Cloned Multi-Robot-Exploration-Development-Environment
✓ Installed ROS2 Humble and Gazebo dependencies
✓ Fixed gazebo_dev package detection issue
✓ Created missing vehicle_simulator/log directory required by CMake
✓ Successfully compiled the workspace

Build Summary:
12 packages finished
0 packages failed
0 packages aborted

Status:
READY FOR TABLE II EXPERIMENTS
