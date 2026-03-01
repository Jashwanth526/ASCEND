# OAK-D Stereo-Inertial VIO on Raspberry Pi 4 (ROS 2 Jazzy)

This repository contains the optimized configuration and calibration for running VINS-Fusion on a Raspberry Pi 4 using an OAK-D camera. 

## Key Technical Challenges Solved:
* **20-Degree Downward Tilt:** Handled via custom extrinsic calibration matrices ($T_{bc}$).
* **Pi 4 Optimization:** Solver time restricted to 35ms with reduced feature counts (60 pts) to maintain real-time 10Hz performance.
* **Rational Polynomial Distortion:** Applied factory-calibrated coefficients to raw image streams to eliminate "NaN" solver crashes.

## Hardware Setup
* **Camera:** OAK-D (7.5cm Baseline)
* **Compute:** Raspberry Pi 4 (8GB)
* **OS:** Ubuntu 24.04 (Noble) w/ ROS 2 Jazzy
