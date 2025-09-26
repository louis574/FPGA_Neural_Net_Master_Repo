# FPGA_Neural_Net_Master_Repo

This repository is the **master hub** for a project of mine where I developed a framework that enables training and deployment of configurable, high-performance, ultra-low-latency neural networks on FPGA hardware.  
It links together all parts of the workflow: quantization-aware training, parameter export, SystemVerilog accelerator design, and a demonstration use case in low-resolution face detection.  

The framework is designed for **continuous data processing**, and has an adapted version with DVP integration for processing high-speed video, frame by frame.  
The framework allows users to balance **accuracy, inference speed, and resource utilization** by adjusting network configuration and fixed point width & format, enabling efficient adaptation to different neural network applications and FPGA platforms.  


---

## 🚀 Project Overview
- **Goal:** Provide a complete, reusable workflow for deploying optimised neural networks on FPGA hardware.  
- **Approach:**  
  1. Train networks with quantisation-aware techniques, with configurable network structures and fixed point formats to balance accuracy with FPGA implementation.  
  2. Export parameters in a fixed-point representation suitable for hardware.  
  3. Deploy on FPGA via a modular SystemVerilog accelerator.  
- **Outcome:** Demonstrated **high-accuracy** and **ultra-low-latency** frame-by-frame inference on video input with different neural network models, meetin performance goals and also showing adaptability and configurability of the framework. The designs were fully synthesizable in Vivado, met timing and pin assignment constraints, and remained comfortably within the resource budget of a mid-range FPGA (Xilinx Artix-7 100T).
- **Results:** (Artix-7 100T)
    1. **MNIST:** 92.1% accuracy (8-bit, q1.7), ~175ns inference, 4k LUTs (6.77%), 0 DSPs.
    2. **Low-res face detection:** 88% accuracy (12-bit, q3.9), ~775ns inference, 28k LUTs (45%),
    184 DSPs (76%); trained on custom dataset, robust to lighting, angles, expressions, ethnicities and backgrounds.
---

## 🌟 Vision
My vision for this framework is to enable real-time AI video processing in embedded and edge environments, leveraging the high performance, configurability, and power efficiency of FPGAs.
It has strong potential in robotics and other autonomous systems, where ultra-low-latency perception and efficient computation are critical.
Next, I aim to deploy this framework in autonomous robotics applications, harnessing its real-time, low-latency capabilities.

## 📂 Repositories
- [🧠 Quantisation-Aware Training & Parameter Export](https://github.com/louis574/Quantisation-aware-training-for-FPGA)  

- [⚡ FPGA Neural Net Accelerator (SystemVerilog)](https://github.com/louis574/FPGANeuralNet)   

- [👁️ Face Detection Demo - with dataset preparation](https://github.com/louis574/Face-detection-example)  
 



