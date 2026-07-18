# MAPF-LNS2


MAPF-LNS2: Fast Repairing for Multi-Agent Path Finding via Large Neighborhood Search


MAPF-LNS2 is an efficient algorithm for solving Multi-Agent Path Finding (MAPF). 
More details can be found in our paper at AAAI 2022 [1].

This software is an advanced version and a superset of MAPF-LNS (https://github.com/Jiaoyang-Li/MAPF-LNS); that is, it also contains Anytime Multi-Agent Path Finding via Large Neighborhood Search [2]. 

## Usage
The code requires the external libraries 
BOOST (https://www.boost.org/) and Eigen (https://eigen.tuxfamily.org/). 
Here is an easy way of installing the required libraries on Ubuntu:    
```shell script
sudo apt update
```
- Install the Eigen library (used for linear algebra computing)
    ```shell script
    sudo apt install libeigen3-dev
    ```
- Install the boost library 
    ```shell script
    sudo apt install libboost-all-dev
    ```
    
After you installed both libraries and downloaded the source code, 
go into the directory of the source code and compile it with CMake: 
```shell script
cmake -DCMAKE_BUILD_TYPE=RELEASE .
make
```

Then, you are able to run the code:
```
./lns -m random-32-32-20.map -a random-32-32-20-random-1.scen -o test -k 400 -t 300 --outputPaths=paths.txt 
```

- m: the map file from the MAPF benchmark
- a: the scenario file from the MAPF benchmark
- o: the output file name (no need for file extension)
- k: the number of agents
- t: the runtime limit
- outputPaths: the output file that contains the paths

You can find more details and explanations for all parameters with:
```
./lns --help
```
[2] Jiaoyang Li, Zhe Chen, Daniel Harabor, Peter J. Stuckey, Sven Koenig. 
Anytime Multi-Agent Path Finding via Large Neighborhood Search. 
In Proceedings of the International Joint Conference on Artificial Intelligence (IJCAI), pages 4127-4135, 2021.
