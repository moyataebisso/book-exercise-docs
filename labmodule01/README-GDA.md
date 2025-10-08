# Gateway Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-01-001 - Lab Module 01](https://github.com/orgs/programming-the-iot/projects/1#column-9974937).

### Description

The Gateway Device Application (GDA) provides the Java-based gateway infrastructure that will serve as the bridge between constrained devices and cloud services. This initial module establishes the core application framework, dependency management through Maven, and fundamental lifecycle operations. The implementation successfully demonstrates initialization, configuration loading, and proper application lifecycle management with appropriate logging and error handling.

The implementation leverages Java and Maven to create a robust gateway application where GatewayDeviceApp serves as the main class orchestrating all operations. The build process uses Maven to manage dependencies and create an executable JAR file with all dependencies included. Configuration is managed through the PiotConfig.props file, similar to the CDA, ensuring consistency across both applications. The application demonstrates successful compilation (after addressing Java version compatibility by excluding InfluxDB components), proper initialization sequences, and clean shutdown procedures with exit code 0.

### Code Repository and Branch

URL: https://github.com/moyataebisso/gda-java-components/tree/labmodule01

### UML Design Diagram(s)


### Unit Tests Executed

- ConfigUtilTest

### Integration Tests Executed

- GatewayDeviceAppTest

EOF.
