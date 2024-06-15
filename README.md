# Platooning_Truck

## Master-Slave Vehicle Simulation with CUDA





## Overview
The Master-Slave Vehicle Simulation project aims to model and control a system of multiple slave vehicles coordinated by a single master vehicle. This simulation utilizes CUDA for GPU acceleration and C++ multi-threading to efficiently manage and compute the behaviors of numerous vehicles.

## Objectives and Motivation
In the realm of autonomous vehicle research, simulating the interactions between a master vehicle and its associated slave vehicles is crucial for several reasons:

Coordination Testing: To understand how a master vehicle can control multiple slave vehicles in scenarios such as fleet management, traffic coordination, or convoy systems.
Performance Optimization: To leverage GPU acceleration with CUDA for real-time processing and computation of vehicle behaviors and positions, enhancing simulation speed and scalability.
Parallel Processing: To utilize multi-threading for handling various simulation tasks concurrently, thus improving computational efficiency and simulation realism.
## Scientific Contributions
## 1. GPU Acceleration with CUDA
CUDA (Compute Unified Device Architecture) enables direct access to the GPU’s parallel computing architecture, allowing for substantial performance improvements in data-intensive computations. In this project, CUDA is used to:

Efficiently Update Vehicle Locations: The CUDA kernel updateLocationKernel performs parallel updates of the slave vehicles' positions, leveraging the GPU to handle large datasets efficiently.
Handle Real-time Simulation: By offloading computationally heavy tasks to the GPU, the simulation can run in real-time, which is critical for interactive and responsive simulation environments.
## 2. Multi-threading in C++
The simulation leverages C++11’s threading capabilities to parallelize tasks across multiple CPU cores, thereby improving the handling of concurrent operations such as vehicle control commands and data synchronization. Multi-threading is used to:

Parallelize Simulation Iterations: Multiple threads run iterations of the simulation loop, updating vehicle states and executing control commands in parallel.
Synchronize GPU and CPU Operations: Ensures that CPU-side logic and GPU-side computations are properly coordinated, enhancing simulation accuracy and efficiency.
## 3. Dynamic Slave Vehicle Management
The master vehicle dynamically manages a fleet of slave vehicles, each of which can be controlled and updated based on simulation requirements. This dynamic approach allows:

Scalability: Easily add or remove slave vehicles during runtime, accommodating varying simulation scenarios.
Flexibility: Apply different control strategies to different sets of vehicles, allowing for heterogeneous vehicle behavior simulations.
# Conclusion
This project highlights the integration of GPU acceleration and multi-threading in simulating a coordinated vehicle system. It demonstrates the effective use of modern computational techniques to enhance simulation performance and realism, providing valuable insights for applications in autonomous vehicle research, fleet management, and traffic control systems.
