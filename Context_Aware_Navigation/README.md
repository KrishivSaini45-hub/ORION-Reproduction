## Run
### Files
* `parameters.py` - Training parameters.
* `driver.py` - Driver of training program, maintain & update the global network.
* `runner.py` - Wrapper of the local network.
* `worker.py` - Interact with the environment and collect episode experience.
* `model.py` - Define attention-based network.
* `env.py` - Autonomous navigation environments.
* `graph_generator.py` - Generate and update the partial robot belief.
* `node.py` - Initialize and update nodes in the partial robot belief.
* `sensor.py` - Simulate the sensor model of Lidar.
* `/model` - Trained model.
* `/DungeonMaps` - Training environments.
### Main Dependencies
* `python == 3.10.8`
* `pytorch == 1.12.0`
* `ray == 2.1.0`
* `scikit-image == 0.19.3`
* `scikit-learn == 1.2.0`
* `scipy == 1.9.3`
* `matplotlib == 3.6.2`
* `tensorboard == 2.11.0`
### Training
1. Set training parameters in `parameters.py`.
2. Run `python driver.py`
### Evaluation
1. Set test parameters in `test_parameters.py`.
2. Run `python test_driver.py`


