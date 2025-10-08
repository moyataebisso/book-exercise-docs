# Lab Module 03 - Data Simulation

## Overview
This lab module implements data simulation capabilities for the Constrained Device App (CDA), creating a foundation for generating sensor telemetry and actuator responses without requiring physical hardware.

## Implementation Summary

### Components Implemented

#### 1. Data Simulators (`programmingtheiot/cda/sim/`)
- **TemperatureSensorSimTask**: Generates simulated temperature readings between 15-25°C
- **HumiditySensorSimTask**: Generates simulated humidity readings between 35-45%
- **PressureSensorSimTask**: Generates simulated pressure readings between 990-1010 hPa
- **HvacActuatorSimTask**: Simulates HVAC system responses to commands
- **HumidifierActuatorSimTask**: Simulates humidifier responses to commands

#### 2. System Managers (`programmingtheiot/cda/system/`)
- **SensorAdapterManager**: Orchestrates all sensor simulators with configurable polling intervals
- **ActuatorAdapterManager**: Manages actuator simulators and command processing
- **DeviceDataManager**: Central coordinator for data flow between sensors and actuators

#### 3. Core Application (`programmingtheiot/cda/app/`)
- **ConstrainedDeviceApp**: Main entry point, initializes and manages the DeviceDataManager

### Key Features
- Configurable simulation parameters via PiotConfig.props
- Automatic HVAC triggering based on temperature thresholds (18°C - 20°C)
- 5-second polling cycle for sensor data generation
- Prevention of duplicate actuator commands

### Configuration Settings
```properties
# Sensor simulation ranges
tempSimFloor = 15.0
tempSimCeiling = 25.0
humiditySimFloor = 35.0
humiditySimCeiling = 45.0
pressureSimFloor = 990.0
pressureSimCeiling = 1010.0

# Actuator trigger thresholds
handleTempChangeOnDevice = True
triggerHvacTempFloor = 18.0
triggerHvacTempCeiling = 20.0

# System settings
pollCycleSecs = 5
enableSensing = False  # Set to True for testing
Test Results

All unit tests for simulators passing
Integration tests for managers functioning correctly
Application successfully generates data at configured intervals
HVAC actuator properly responds to temperature threshold crossings

Challenges and Solutions

ConfigConst naming: Fixed mismatch between ENABLE_HANDLE_TEMP_CHANGE_ON_DEVICE_KEY and HANDLE_TEMP_CHANGE_ON_DEVICE_KEY
SystemPerformanceManager interface: Added missing setDataMessageListener method
Data flow: Implemented proper listener pattern for communication between components

Learning Outcomes

Understanding of simulation vs emulation in IoT development
Implementation of observer pattern for data messaging
Configuration-driven development approach
Testing strategies for simulated environments
