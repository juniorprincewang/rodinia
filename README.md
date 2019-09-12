# Rodinia Benchmark Suite 3.1


## Modifications
Please download the dataset from the [original package][data].
[data]: http://lava.cs.virginia.edu/Rodinia/download_links.htm

Make sure the Platform 0 is the one needed to be tested, and GPU is the
device 0 on this platform.

## Overview

The University of Virginia Rodinia Benchmark Suite is a collection of parallel programs which targets 
heterogeneous computing platforms with both multicore CPUs and GPUs.

## Usage

### Pakage Structure

rodinia/bin		: binary executables
rodinia/common	: common configuration file
rodinia/cuda	: source code for the CUDA implementations
rodinia/data	: input files
rodinia/openmp	: source code for the OpenMP implementations
rodinia/opencl	: source code for the OpenCL implementations

### Build Rodinia

Install the CUDA/OCL drivers, SDK and toolkit on your machine. 

Modify the rodinia/common/make.config file to change the settings of rodinia home directory and CUDA/OCL library paths.

To compile all the programs of the Rodinia benchmark suite, simply use the universal make file to compile all the programs, or go to each 
benchmark directory and make individual programs. 

### Run Rodinia

There is a 'run' file specifying the sample command to run each program.

## Rodinia wiki: 

http://lava.cs.virginia.edu/wiki/rodinia
