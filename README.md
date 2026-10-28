# Microcontroller-Lab03: Buttons, Switches and Traffic Light Control

## Course Information

**Course:** Microprocessors-Microcontrollers (CO3009)  
**Laboratory:** Lab 03 - Buttons/Switches

## Overview

This repository contains the implementation of Lab 03 for the
Microprocessors-Microcontrollers course.

The projects are developed using an **STM32 microcontroller**,
**STM32CubeIDE**, and **Proteus**.

The laboratory focuses on digital button inputs, pull-up resistors,
switch debouncing, timer interrupts, finite state machines (FSMs),
seven-segment displays, and a configurable traffic light system.

The main application is a crossroads traffic light controller with
three push buttons for mode selection, time adjustment, and confirmation.

## Objectives

The main objectives are:

- Create and organize C source files and header files in an STM32 project.
- Read digital button inputs and apply software debouncing.
- Use a periodic timer interrupt for button sampling and timing tasks.
- Design and implement finite state machines for input processing.
- Control traffic light LEDs and seven-segment displays.
- Switch between normal operation and three time-configuration modes.
- Adjust and save the red, amber, and green light durations using buttons.
- Preserve timing behavior when the timer interrupt period is changed.

## Laboratory Exercises

### Exercise 1: Sketch an FSM

Design a finite state machine (FSM) describing the operation of the traffic
light controller, including normal mode, configuration modes, and button actions.

### Exercise 2: Proteus Schematic

Draw the Proteus schematic for the crossroads traffic light system with
12 LEDs, four seven-segment displays, and three control buttons.

### Exercise 3: Create STM32 Project

Create an STM32 project matching the GPIO connections in the Proteus schematic.
Configure a periodic timer interrupt of approximately 10 ms.

### Exercise 4: Modify Timer Parameters

Organize the timing parameters so that changing the interrupt period
(e.g., from 10 ms to 1 ms or 100 ms) does not change the intended application
behavior, such as an LED blinking at 2 Hz.

### Exercise 5: Button Debouncing

Create input-reading and output-display modules, implement software button
debouncing, and use the first button to cycle through the four operating modes.

### Exercise 6: Display Operating Modes

Display the selected mode using seven-segment displays and blink the
corresponding traffic light LEDs in each configuration mode.

### Exercise 7: Red Light Duration

In Mode 2, use the second button to increase the red light duration and
the third button to confirm the value. The adjustable duration is from
1 to 99, and the red LEDs blink at 2 Hz.

### Exercise 8: Amber Light Duration

In Mode 3, use the second button to increase the amber light duration and
the third button to confirm the value. The amber LEDs blink at 2 Hz.

### Exercise 9: Green Light Duration

In Mode 4, use the second button to increase the green light duration and
the third button to confirm the value. The green LEDs blink at 2 Hz.

### Exercise 10: Complete Traffic Light System

Integrate all previous exercises into one project. Demonstrate the required
features in a video, prepare an exercise-by-exercise report, and submit
the report and source code through BKeL.

## Timer Configuration

The laboratory uses a periodic timer interrupt for button reading and
application timing.

- Reference timer: `TIM2`
- Target interrupt period: approximately `10 ms`
- Corresponding interrupt frequency: approximately `100 Hz`
- Configuration-mode LED blinking frequency: `2 Hz`
- Timing logic must remain consistent if the interrupt period changes
  to `1 ms` or `100 ms`.

The exact prescaler and counter period depend on the configured STM32
timer clock and are not fixed in the laboratory specification.

## Development Environment

### Hardware

- STM32 microcontroller
- 12 traffic light LEDs: 4 red, 4 amber, and 4 green
- Four seven-segment displays (two for each road)
- Three push buttons for mode selection, value adjustment, and confirmation
- Pull-up resistors for reliable digital button inputs

### Software Tools

- STM32CubeIDE
- Proteus Simulation Software
- STM32 HAL Library

## Repository Structure

```text
Microcontroller-Lab03
│
├── Proteus_Lab3
│   └── (Proteus schematic and simulation files)
│
├── STM32_Lab3
│   └── (STM32CubeIDE project and source files)
│
└── README.md
```

## Key Concepts

- Digital GPIO input and output
- Pull-up resistors and active-low buttons
- Mechanical switch bouncing and software debouncing
- Timer interrupts and periodic button sampling
- Finite state machine (FSM)
- Modular input reading and output processing
- Seven-segment display control
- Traffic light mode selection
- Configurable red, amber, and green light durations
- Timer-independent blinking behavior

## Simulation

The traffic light application is designed for simulation in Proteus.

The repository is organized to include:

- STM32CubeIDE project and source code
- Proteus circuit schematics
- Button reading and debouncing logic
- FSM-based traffic light control
- Seven-segment mode and duration display
- Configurable traffic light timing

## Author

**Le Hien Vinh**
