# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

The Lab Module 02 implementation adds system performance monitoring capabilities to the Gateway Device Application using Java's built-in management extensions. The solution implements a SystemPerformanceManager that coordinates CPU and memory monitoring through a scheduled executor service running at 30-second intervals. The architecture follows an object-oriented design with BaseSystemUtilTask as an abstract class that defines the telemetry collection contract, while SystemCpuUtilTask and SystemMemUtilTask provide concrete implementations using Java Management Extensions (JMX) to access system metrics through the OperatingSystemMXBean and MemoryMXBean interfaces.

The implementation integrates with the GatewayDeviceApp by following the same lifecycle pattern as the CDA. The SystemPerformanceManager is instantiated during application initialization and started when the GDA starts, using a ScheduledExecutorService to handle periodic execution without blocking. The system logs CPU utilization as a percentage of process load and memory utilization based on JVM heap usage. This telemetry framework establishes the foundation for the gateway's role in aggregating and processing data from multiple constrained devices, demonstrating how the GDA can monitor its own health while managing data from edge devices.

### Code Repository and Branch

URL: https://github.com/moyataebisso/gda-java-components/tree/labmodule02

### UML Design Diagram(s)

[To be provided per course requirements]

### Unit Tests Executed

- ConfigUtilTest
- SystemCpuUtilTaskTest (if available)
- SystemMemUtilTaskTest (if available)

### Integration Tests Executed

- GatewayDeviceAppTest
- Manual verification of SystemPerformanceManager logging CPU/Memory metrics every 30 seconds

EOF.
