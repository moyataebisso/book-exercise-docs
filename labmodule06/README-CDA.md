# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-06-001 - Lab Module 06](https://github.com/orgs/programming-the-iot/projects/1#column-10488434).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: 

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
- 
- 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 

EOF.

## Wireshark/Tshark Packet Analysis Details

### Captured MQTT Packets from Test Run:

1. **CONNECT Request**
   - Message Type: Connect Command (1)
   - Client ID: constraineddevice001
   - Keep Alive: 60 seconds

2. **CONNACK Response**
   - Message Type: Connect Ack (2)
   - Return Code: Connection Accepted (0)

3. **SUBSCRIBE Request**
   - Message Type: Subscribe Request (8)
   - Topic: PIOT/ConstrainedDevice/MgmtStatusMsg
   - QoS: 0

4. **SUBACK Response**
   - Message Type: Subscribe Ack (9)
   - Granted QoS: 0

5. **PUBLISH Messages**
   - QoS 0: "QoS 0" - Single packet, no acknowledgment
   - QoS 1: "QoS 1" - PUBLISH + PUBACK
   - QoS 2: "QoS 2" - Full 4-way handshake

6. **UNSUBSCRIBE Request**
   - Message Type: Unsubscribe Request (10)
   - Topic: PIOT/ConstrainedDevice/MgmtStatusMsg

7. **UNSUBACK Response**
   - Message Type: Unsubscribe Ack (11)

Total packets captured: 28
Protocol verified: MQTT v3.1.1
