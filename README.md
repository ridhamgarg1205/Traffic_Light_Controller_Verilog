# Traffic_Light_Controller_Verilog
FSM-based Traffic Light Controller in Verilog, demonstrating clock-driven state transitions and signal sequencing

This project implements a traffic light controller using Verilog HDL based on a finite state machine (FSM). It simulates the operation of traffic signals at an intersection and ensures proper sequencing between different directions.

Features:

* FSM-based design with 6 states
* Clock-driven synchronous operation
* Reset functionality
* Timing control using a counter
* Supports signals for M1, M2, S and MT

Working:
Each state represents a specific traffic condition. The controller transitions between states after fixed delays, allowing only one direction to have a green signal at a time to ensure safe operation.

Simulation:
The design is verified using a testbench and waveform analysis. The waveform shows correct state transitions and signal timing.

Commands used:
iverilog -o sim testbench.v design.v
vvp sim
gtkwave trafficlight_tb.vcd

This project demonstrates basic digital design concepts such as FSM implementation, timing control, and simulation using Verilog.
