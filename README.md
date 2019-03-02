# CS7641-Randomized-Optimization
Georgia Tech CS 7641 - Randomized Optimization

Author: Kyle MacNeney

Author Email: kyle.macneney@gmail.com

Repository: https://github.com/eazymac25/cs7641-randomized-optimization

**NOTE: Written in markdown**

## Description
This contains optimization experiments for:
- Traveling Salesman Problem
- Continuous Peaks Problem
- Flip Flop Problem
Optimized via MIMIC, GA, SA, or RHC

And contains training a neural network against the [adult census dataset](https://www.kaggle.com/uciml/adult-census-income/kernels) using the following teqniques:
- Backpropagation
- Genetic Algorithm
- Randomized Hill Climbing
- Simulated Annealing

## Pre-requisites
1. Install Java version=9.0.1
2. Install latest [Jython](https://www.jython.org/)
3. Install Python 2.7
4. Install git
5. Depends on ABAGAIL (built as jar and included in repository) [ABAGAIL](https://github.com/pushkar/ABAGAIL)

## Installation Instructions
1. Clone or download repository
    ```bash
    git clone https://github.com/eazymac25/cs7641-randomized-optimization.git
    ```
2. Install all requirements listed in `requirements.txt`
    ```bash
    pip install -r requirements.txt
    ```
## Directory Structure
```
|-- problem-statement.txt
|-- requirements.txt (python requirements)
|-- README.md
|-- README.txt (text version because you asked)
|-- solution
    |-- copied_code (not hiding it -_- )
        |-- ABAGAIL
            |-- ABAGAIL.jar
            |-- src (all src files found from ABAGAIL repo)
        |-- data
            |-- loader.py (loads raw data into test/train/validate)
            |-- raw_census_data.csv
            |-- census_train.csv
            |-- census_train.csv
            |-- census_validate.csv
        |-- output
            |-- CONTPEAKS
                |-- experiment csv's
            |-- FLIPFLOP
                |-- experiment csv's
            |-- images
                |-- all graphs
            |-- NN_OUTPUT
                |-- Neural net output
            |-- TSP
                |-- tsp data
            |-- best_results.csv (best params for each experiment)
            |-- timing.csv (times for neural nets)
        |-- base.py (helper functions)
        |-- continuouspeaks.py
        |-- flipflop.py
        |-- tsp.py
        |-- NNBackprop.py
        |-- NNGA.py
        |-- NNRHC.py
        |-- NNSA.py
        |-- plotting.py (plotting helpers)
        |-- run_exeriment.py (probably do not need)
        |-- run_jython.py
```

## Running Experiments

First move into root of repository

### Load Data
```bash
python ./solution/copied_code/data/loader.py
```

### Run Optimization Experiments
**NOTE:** All will require jython.exe
1. Flip Flop
    ```bash
    jython ./solution/copied_code/flipflop.py
    ```
2. Continuous Peaks
    ```bash
    jython ./solution/copied_code/continuouspeak.py
    ```
3. Traveling Salesman
    ```bash
    jython ./solution/copied_code/tsp.py
    ```
    
### Run Neural Network Experiments
```bash
jython ./solution/copied_code/run_jython.py
```

### Plot All the Output
**NOTE:** This requires python.exe to run
```bash
python ./solution/copied_code/plotting.py
```