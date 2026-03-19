# Traffic Light Controller using Verilog

This project implements a traffic light controller using Verilog HDL based on a Finite State Machine (FSM). It simulates the operation of traffic signals at an intersection and ensures proper sequencing between different directions.

## Features

- FSM-based design with 6 states  
- Clock-driven synchronous operation  
- Reset functionality  
- Timing control using a counter  
- Supports signals for M1, M2, S, and MT  

## Working

Each state represents a specific traffic condition. The controller transitions between states after fixed delays, allowing only one direction to have a green signal at a time to ensure safe operation.

## Simulation

The design is verified using a testbench and waveform analysis. The waveform shows correct state transitions and signal timing.

## Commands Used

```bash
iverilog -o sim testbench.v design.v
vvp sim
gtkwave trafficlight_tb.vcd
