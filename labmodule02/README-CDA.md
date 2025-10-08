# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

The Lab Module 02 implementation adds system performance monitoring capabilities to the Constrained Device Application. The solution implements a SystemPerformanceManager that coordinates the collection of CPU and memory utilization metrics at regular 30-second intervals. This is achieved through a modular architecture where BaseSystemUtilTask serves as an abstract base class, with SystemCpuUtilTask and SystemMemUtilTask as concrete implementations that use the psutil library to gather system metrics. The performance manager uses APScheduler to handle the periodic data collection, ensuring metrics are gathered consistently without blocking the main application thread.

The implementation integrates seamlessly with the existing ConstrainedDeviceApp structure from Lab Module 01. When the CDA starts, it initializes and starts the SystemPerformanceManager, which begins scheduling telemetry collection jobs. The manager logs CPU and memory utilization percentages to provide visibility into system resource usage. This foundational telemetry system establishes the pattern for future sensor data collection that will be added in subsequent lab modules, demonstrating how the CDA can monitor both system health and environmental conditions.

### Code Repository and Branch

URL: https://github.com/moyataebisso/cda-python-components/tree/labmodule02

### UML Design Diagram(s)

[To be provided per course requirements]

### Unit Tests Executed

- test_SystemCpuUtilTask
- test_SystemMemUtilTask
- test_ConfigUtilDefault
- test_ConfigUtilCustom

### Integration Tests Executed

- test_ConstrainedDeviceApp
- Manual verification of SystemPerformanceManager logging CPU/Memory metrics every 30 seconds

EOF.
