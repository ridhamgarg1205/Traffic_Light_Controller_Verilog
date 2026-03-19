# Traffic Light Controller (Verilog)

## Description

The given code defines a traffic light controller module in Verilog, which manages the states of traffic lights at an intersection.

---

## Features

### 1. Inputs and Outputs

- clk: Clock signal  
- rst: Reset signal  

Outputs:
- light_M1: Traffic light for Main Road 1  
- light_S: Traffic light for Side Road  
- light_MT: Traffic light for Main Road Turn  
- light_M2: Traffic light for Main Road 2  

Each output is a 3-bit signal representing the light color.

---

### 2. State Machine

- The controller operates as a Finite State Machine (FSM)  
- It consists of six states: S0 to S5  
- Timing is controlled using parameters:
  - sec7
  - sec5
  - sec2
  - sec3

These parameters define the duration of each state in clock cycles.

---

### 3. Behavior

- On the rising edge of the clock or reset, the FSM transitions between states  
- A counter increments with each clock cycle  
- State transitions occur based on predefined timing  

#### State Transitions:

- S0: Main Road 1 and Main Road 2 are Green, others are Red  
- S1: Main Road 1 is Green, Main Road 2 is Yellow, others are Red  
- S2: Main Road 1 and Main Road Turn are Green, others are Red  
- S3: Main Road 1 and Main Road Turn are Yellow, others are Red  
- S4: Side Road is Green, others are Red  
- S5: Side Road is Yellow, others are Red  

---

### 4. Output Logic

The outputs are updated based on the current state (ps).

Each state assigns specific color values:

- 3'b001 → Green  
- 3'b010 → Yellow  
- 3'b100 → Red  

---

## Summary

This module simulates a traffic light sequence at an intersection, ensuring smooth and organized traffic flow by controlling signals based on predefined timing and FSM state transitions.
