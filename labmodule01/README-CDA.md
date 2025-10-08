# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-01-001 - Lab Module 01](https://github.com/orgs/programming-the-iot/projects/1#column-9974937).

### Description

The Constrained Device Application (CDA) establishes the foundational Python-based IoT framework for edge devices. In this initial module, the implementation focuses on setting up the core application structure, configuration management system, and basic lifecycle operations. The application successfully initializes, loads configuration parameters from PiotConfig.props, and demonstrates proper startup and shutdown procedures with appropriate logging throughout the process.

The implementation works by utilizing a modular architecture where ConstrainedDeviceApp.py serves as the main entry point that orchestrates the application lifecycle. ConfigUtil handles the loading and parsing of configuration files from the config directory, providing a centralized way to manage application settings. The application runs within a Python virtual environment to ensure dependency isolation and uses the logging framework to provide visibility into application state transitions. The current implementation demonstrates successful initialization, configuration loading, and graceful shutdown capabilities.

### Code Repository and Branch

URL: https://github.com/moyataebisso/cda-python-components/tree/labmodule01

### UML Design Diagram(s)


### Unit Tests Executed

- test_ConfigUtilDefault
- test_ConfigUtilCustom

### Integration Tests Executed

- test_ConstrainedDeviceApp

EOF.
