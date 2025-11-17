# Lane Keeping Assist (LKA) System - Model-Based Design.

[![MATLAB](https://img.shields.io/badge/MATLAB-R2023b-orange.svg)](https://www.mathworks.com/)
[![Simulink](https://img.shields.io/badge/Simulink-10.8-blue.svg)](https://www.mathworks.com/products/simulink.html)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Tests](https://img.shields.io/badge/Tests-In_Progress-yellow.svg)](tests/)
[![Coverage](https://img.shields.io/badge/Coverage-In_Progress-yellow.svg)](tests/)

## 📋 Project Overview

Advanced Driver Assistance System (ADAS) for lane keeping assistance, developed using 
**Model-Based Design (MBD)** methodology following automotive industry standards 
(**ISO 26262**, **SOTIF**). The system provides lateral control to maintain vehicle 
position within lane boundaries on highways.

**Key Features:**
- 🎯 Lane detection using computer vision (Hough transform)
- 🚗 Model Predictive Control (MPC) for optimal steering
- ⚠️ Comprehensive safety monitoring and fail-safe mechanisms
- 📊 Real-time performance: <50ms execution time target
- ✅ Automated V&V suite with comprehensive test coverage

---

## 🎯 Project Scope

**In Scope:**
- Highway driving at speeds 60-130 km/h
- Maintain vehicle position within ±0.3m of lane center with 95% reliability
- Handle straight roads and gentle curves (R>200m)
- Graceful deactivation on failures or driver override

**Out of Scope:**
- Sharp curves (<200m radius)
- Urban/city driving
- Construction zones with no lane markings
- Adverse weather (heavy rain, snow)
- Multi-lane changes

---

## 🏗️ System Architecture

The system follows a modular architecture with clear separation of concerns:

- **Perception Module**: Camera-based lane detection with confidence scoring
- **Control Module**: MPC-based lateral controller with feedforward
- **Safety Monitor**: Plausibility checks, fault detection, and fail-safe logic
- **State Machine**: Mode management (Stateflow) with safe transitions
- **Actuation**: Steering command limiting and rate control

---

## 📊 Success Criteria

| Metric | Requirement | Status |
|--------|-------------|--------|
| Lateral Tracking Error (RMS) | <0.1m | 🟡 In Progress |
| Max Lateral Error | <0.3m | 🟡 In Progress |
| Control Latency | <100ms | 🟡 In Progress |
| Driver Override Response | <50ms | 🟡 In Progress |
| Test Pass Rate | >95% | 🟡 In Progress |
| Code Coverage (Decision) | >85% | 🟡 In Progress |

---

## 🛠️ Technology Stack

**Development Environment:**
- MATLAB R2023b+
- Simulink & Stateflow
- Automated Driving Toolbox
- Model Predictive Control Toolbox
- Simulink Test & Coverage
- Embedded Coder

**Simulation:**
- IPG CarMaker 11.0 (primary)
- CARLA (fallback option)
- Vehicle Dynamics Blockset

**Standards & Methods:**
- ISO 26262 (ASIL-B approach)
- ISO 21448 (SOTIF)
- V-Model development process
- MAAB modeling guidelines

---

## 📁 Repository Structure

```
LKA-MBD-Project/
├── README.md
├── requirements/
│   ├── system_requirements.xlsx
│   ├── safety_analysis.xlsx
│   └── traceability_matrix.xlsx
├── design/
│   ├── architecture/
│   └── interface_definitions/
├── models/
│   ├── perception/
│   ├── control/
│   ├── safety_monitor/
│   ├── vehicle_dynamics/
│   └── integration/
├── tests/
│   ├── unit_tests/
│   ├── integration_tests/
│   └── system_tests/
├── scripts/
│   ├── test_automation/
│   └── data_analysis/
├── documentation/
│   ├── reports/
│   └── presentations/
└── results/
    ├── figures/
    └── videos/
```

---

## 🚀 Getting Started

### Prerequisites

1. **MATLAB R2023b or later** with the following toolboxes:
   - Simulink
   - Automated Driving Toolbox
   - Vehicle Dynamics Blockset
   - Simulink Test
   - Simulink Coder / Embedded Coder
   - Model Predictive Control Toolbox
   - Computer Vision Toolbox
   - Stateflow

2. **Simulator** (choose one):
   - IPG CarMaker 11.0+ (recommended)
   - CARLA 0.9.13+ (fallback)

### Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd LKA-MBD-Project
```

2. Open MATLAB and navigate to the project directory:
```matlab
cd('LKA-MBD-Project')
```

3. Run the setup script (to be created):
```matlab
setup_project.m
```

---

## 📖 Development Process

This project follows the **V-Model** development process:

1. **Phase 0**: Project Setup & Tooling
2. **Phase 1**: Requirements & Safety Engineering
3. **Phase 2**: System Architecture & Design
4. **Phase 3**: Model Implementation
5. **Phase 4**: Testing & Validation
6. **Phase 5**: Integration & System Testing
7. **Phase 6**: Documentation & Final Deliverables

See `documentation/` for detailed phase descriptions.

---

## 👥 Team Roles

- **Person 1**: Systems & Safety Engineer (Requirements, HARA, Safety Analysis)
- **Person 2**: Control & Algorithm Engineer (Architecture, Control Algorithms, Perception)
- **Person 3**: Test & Integration Engineer (CarMaker-Simulink Setup, V&V)

---

## 🧪 Testing

Run the test suite:

```matlab
% Model-in-the-Loop (MIL) Testing
Run_MIL_Tests.m

% Software-in-the-Loop (SIL) Testing
Run_SIL_Tests.m

% Integration Testing
Run_Integration_Tests.m

% System Testing
Run_System_Tests.m
```

---

## 📚 Documentation

- [Project Charter](documentation/Project_Charter.md)
- [System Requirements](requirements/system_requirements.xlsx)
- [Safety Analysis](requirements/safety_analysis.xlsx)
- [Architecture Design](design/architecture/)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Based on ISO 26262 and SOTIF standards
- Model-Based Design best practices
- Automotive ADAS development methodologies

---

## 📧 Contact

For questions or contributions, please open an issue or contact the project team.

---

**Status**: 🚧 Project in Active Development


