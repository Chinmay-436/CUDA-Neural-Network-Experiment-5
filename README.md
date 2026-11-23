# Experiment 5: Neural Network Layers in CUDA

## Objective
To implement neural network layers using CUDA and compare CPU and GPU performance.

## Hardware
- GPU: NVIDIA GeForce RTX 5060 Ti
- CUDA Toolkit: 13.0

## Network Architecture
- Input Layer: 256 x 128
- Hidden Layer: 256 x 64
- Output Layer: 256 x 10

## CUDA Kernels
1. Matrix Multiplication with Bias
2. ReLU Activation
3. Sigmoid Activation

## Implementation
The program performs a two-layer neural network forward pass.
It compares CPU and GPU outputs and measures execution time.

## Execution

Compile:
```bash
nvcc -O2 neural_network.cu -o neural_network.exe

@'
# Experiment 5: Neural Network Layers in CUDA

## Objective
To implement neural network layers using CUDA and compare CPU and GPU performance.

## Hardware
- GPU: NVIDIA GeForce RTX 5060 Ti
- CUDA Toolkit: 13.0

## Network Architecture
- Input Layer: 256 x 128
- Hidden Layer: 256 x 64
- Output Layer: 256 x 10

## CUDA Kernels
1. Matrix Multiplication with Bias
2. ReLU Activation
3. Sigmoid Activation

## Implementation
The program performs a two-layer neural network forward pass.
It compares CPU and GPU outputs and measures execution time.

## Execution

Compile: `nvcc -O2 neural_network.cu -o neural_network.exe`

Run: `neural_network.exe`

## Experimental Results

| Parameter | Result |
|---|---:|
| CPU Compute Time | 0.701650 ms |
| GPU Kernel Time | 0.025837 ms |
| GPU End-to-End Time | 0.129535 ms |
| GPU Kernel Speedup | 27.16x |
| GPU End-to-End Speedup | 5.42x |
| Maximum Output Difference | 0.000000 |

## Speedup Calculations

GPU Kernel Speedup = CPU Time / GPU Kernel Time

= 0.701650 / 0.025837 = 27.16x

GPU End-to-End Speedup = CPU Time / GPU End-to-End Time

= 0.701650 / 0.129535 = 5.42x

## Verification
- Matrix Multiplication: PASSED
- ReLU: PASSED
- Sigmoid: PASSED
- CPU and GPU Outputs: MATCH (within tolerance)

## Conclusion
The neural network forward pass was successfully implemented using CUDA.
GPU execution was faster than CPU execution for this experiment.
