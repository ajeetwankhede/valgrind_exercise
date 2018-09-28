## Overview

To explore the valgrind tool to improve code quality during development and testing.

# Identify bugs

Two bugs were indentified using valgrind tool in the repository. The output of valgrind is stored in 'valgrind_errors.txt' file.
1. Bug 1: Conditional jump or move depends on uninitialised value(s)
   Source: main.cpp:9
2. Bug 2:  44 (24 direct, 20 indirect) bytes in 1 blocks are definitely lost in loss record 2 of 3
   Source: AnalogSensor::Read() (AnalogSensor.cpp:16)
   
# Fixed the bugs

Bug 1 fix: Initialize the bool terminator = 1;
Bug 2 fix: Used smart pointer.

The ouput of valgrind after fixing the bug is stored in 'valgrind_fixed.txt' file.

# Valgrind as a function and memory profiler:

A screenshot of the profiler output is stored in 'function and memory profiler.png'. 

## Standard install via command-line
```
git clone --recursive https://github.com/ajeetwankhede/valgrind_exercise
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run tests: ./test/cpp-test
Run program: ./app/shell-app
```
