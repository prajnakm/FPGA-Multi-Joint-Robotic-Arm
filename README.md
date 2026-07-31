# FPGA-Multi-Joint-Robotic-Arm
An FPGA-based robotic arm control system implemented using Verilog HDL on the Nexys-4 FPGA Development Board for real-time control of DC motors, DC geared motors, and SG5010 servo motors through Pulse Width Modulation (PWM).

# Overview
This project presents the design, implementation, and hardware validation of an FPGA-based Multi-Joint Robotic Arm using Verilog HDL. The project follows a systematic approach, beginning with PWM generation and verification, followed by speed control of DC and DC geared motors, and finally extending to the position control of three SG5010 servo motors integrated into a robotic arm.
Unlike many robotic arm implementations that directly focus on servo control, this project first investigates the behavior of different motor types under FPGA-generated PWM signals. This experimental approach provides a better understanding of motor characteristics before implementing coordinated robotic arm movement.
The robotic arm consists of three joints (Shoulder, Elbow, and Wrist) and is controlled using a Finite State Machine (FSM) implemented entirely in hardware.

# Project Objectives
Design a PWM generator using Verilog HDL.
Verify PWM generation using onboard LEDs.
Study the relationship between PWM duty cycle and DC motor speed.
Compare the characteristics of DC and DC geared motors.
Experimentally calibrate SG5010 servo motors.
Develop a three-joint robotic arm.
Implement coordinated motion using a Finite State Machine.
Demonstrate deterministic real-time motor control using FPGA.

# Hardware Used
Nexys-4 FPGA Development Board,
Xilinx Vivado Design Suite,
Verilog HDL,
L293D Dual H-Bridge Motor Driver,
Conventional DC Motor,
DC Geared Motor,
SG5010 Servo Motors (Shoulder, Elbow and Wrist),
External 6 V Power Supply,
Breadboard and Connecting Wires.

# Software Used
Xilinx Vivado,
Verilog HDL,
XDC Constraints File,

# Project Workflow
PWM Generator--->LED Verification--->DC Motor Speed Control--->DC Geared Motor Analysis--->Servo Motor Calibration--->Three-Joint Robotic Arm--->Finite State Machine Control

# Features
FPGA-based hardware implementation
Parallel processing architecture
PWM generation using Verilog HDL
DC motor speed control
Geared DC motor analysis
Servo motor position control
Three independent servo channels
FSM-based motion sequencing
Real-time robotic arm control

# Motion Sequence
The robotic arm follows a predefined sequence:
HOME
   │
   ▼
Move Shoulder
   │
   ▼
Move Elbow + Wrist
   │
   ▼
Hold Position
   │
   ▼
Return Home

The shoulder joint moves first, followed by simultaneous movement of the elbow and wrist before the arm returns to its home position.
