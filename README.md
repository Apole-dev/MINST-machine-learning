# Handwritten Digit Recognition (C++)

![Status](https://img.shields.io/badge/status-learning-blue)
![Language](https://img.shields.io/badge/language-C++-blue)
![Build](https://img.shields.io/badge/build-CMake-orange)
![Dataset](https://img.shields.io/badge/dataset-MNIST-lightgrey)

This project explores handwritten digit recognition using basic machine learning algorithms written from scratch in C++.

It is not a finished system. It is a learning-focused implementation.

## Overview

The system reads raw dataset files (MNIST format), processes them, and applies a classification algorithm.

Main components:

- Data: Represents a single data sample (image + label)
- DataHub: Handles dataset loading and association
- KNN: Implements k-nearest neighbors classification

## Dataset

- MNIST handwritten digit dataset
- Binary IDX file format
- Image and label files are manually parsed

## Implemented Algorithm

### K-Nearest Neighbors (KNN)

- Distance-based classification
- Uses dataset loaded through DataHub
- Example usage:
  - `K = 3`
  - Finds nearest samples and predicts label

## Project Structure


/Data
- Data representation and parsing

/Data Hub
- Dataset loading and management

/KNN Algorithm
- KNN implementation

/archive
- Dataset files (MNIST)

/main.cpp
- Entry point


## How It Works

1. Load dataset paths (train + test)
2. Parse IDX files into memory
3. Associate images with labels
4. Run KNN on test data
5. Predict labels based on nearest neighbors

## Notes

- Written for learning purposes
- Hardcoded dataset paths (needs refactor)
- No optimization for large datasets
- Error handling is minimal

## Known Issues

- Some unstable behavior during dataset parsing
- No validation for corrupted files
- Performance drops with large input size

## TODO

- Remove hardcoded paths (make configurable)
- Improve parsing robustness
- Add dataset normalization
- Optimize KNN (distance calculation, memory usage)
- Add accuracy evaluation (confusion matrix, metrics)

## Build

```bash
mkdir build
cd build
cmake ..
make
Run
```
Make sure dataset paths are correctly set inside main.cpp.

## Why This Project

The goal is to understand:

- How raw data is handled in ML systems
- How simple algorithms like KNN actually work internally
- Memory and performance constraints in low-level implementations
