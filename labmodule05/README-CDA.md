# Constrained Device Application (Connected Devices)

## Lab Module 05


Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488387).

### Description

What does your implementation do?

This lab module implements comprehensive data management capabilities for the Constrained Device Application, establishing a robust foundation for data serialization and exchange. The implementation transforms raw sensor and actuator data into structured, serializable formats through two key components: the SystemPerformanceData container and the DataUtil serialization utility. SystemPerformanceManager now encapsulates CPU and memory metrics into SystemPerformanceData objects, providing organized telemetry that can be easily transmitted and stored. The DataUtil module enables bidirectional conversion between data objects and JSON, supporting all three primary data types (ActuatorData, SensorData, SystemPerformanceData) with proper timestamp preservation and type handling.

How does your implementation work?

The SystemPerformanceManager collects system metrics through CPU and memory utilization tasks, then packages these values into SystemPerformanceData containers that include location ID, timestamps, and performance metrics in a single object. This containerization simplifies data handling and transmission to listeners through the IDataMessageListener interface. The DataUtil module implements JSON serialization using Python's json library with a custom JsonDataEncoder that handles object-to-dictionary conversion. For deserialization, it reconstructs typed objects from JSON while preserving critical fields like timestamps by directly setting object attributes when necessary. The implementation handles edge cases such as missing fields, type ID initialization through constructors, and UTF-8 encoding options. All tests pass successfully, demonstrating proper round-trip conversion where objects can be serialized to JSON and reconstructed without data loss.

### Code Repository and Branch

URL: https://github.com/moyataebisso/cda-python-components/tree/labmodule05

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).

### Unit Tests Executed

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- DataUtilTest (all 6 test methods passing)

### Integration Tests Executed

- SystemPerformanceManagerTest
- SensorAdapterManagerTest
- ActuatorAdapterManagerTest
- DeviceDataManagerTest
- ConstrainedDeviceAppTest

EOF.
