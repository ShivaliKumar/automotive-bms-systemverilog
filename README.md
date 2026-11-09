# Automotive Battery Management System (BMS) – RTL Design & Verification

## Overview
This project implements a parameterized Automotive Battery Management System (BMS) using SystemVerilog. It monitors battery operating conditions, detects faults, and manages battery safety through an FSM-based control architecture.

## Features
- Parameterized 4-state Finite State Machine (FSM).
- Monitoring of overvoltage and undervoltage conditions.
- Detection of overcurrent and overtemperature.
- State of Charge (SOC) limit monitoring.
- ADC sensor validity checking.
- Fault latching and hysteresis-based recovery.
- Cell balancing based on voltage differences.

## Design Architecture
The design consists of two main components:

- **BMS Monitor:** Evaluates battery voltage, current, temperature, SOC, and sensor validity to generate fault signals.
- **BMS Controller:** Uses a 4-state FSM to control charging, normal operation, and fault handling.

## Verification Methodology
A SystemVerilog self-checking testbench was developed to verify the design using:

- Directed testing for fault conditions and threshold boundaries.
- Randomized stimulus to test different input combinations.
- SystemVerilog Assertions (SVA) for checking design properties.
- Functional coverage to evaluate verification completeness.

## Simulation Results

| Metric | Result |
|---|---:|
| Total checks | 648 |
| Passed | 648 |
| Failed | 0 |
| Overall functional coverage | 98.04% |
| FSM state/transition coverage | 88.89% |
| SVA assertions | 13 |

### Coverage Highlights
- 100% coverage for individual fault conditions.
- 100% coverage for individual input ranges.
- 100% coverage for output combinations.
- 77.78% coverage for cell voltage cross coverage.

## Repository Structure

```text
automotive-bms-systemverilog/
├── rtl/
│   └── design.sv
├── verification/
│   └── testbench.sv
└── README.md
```

## Tools & Technologies
- SystemVerilog
- RTL Design
- SystemVerilog Assertions (SVA)
- Functional Coverage
- Digital Design Verification

## Future Improvements
- Increase FSM transition coverage.
- Improve cross coverage for cell voltage combinations.
- Extend randomized testing to sequential operating scenarios.

## Author
**Shivali Kumar**

[GitHub Profile](https://github.com/ShivaliKumar)
