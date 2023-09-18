# Constrained Device Application (Connected Devices)

## Lab Module 01

## Description
NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

### What does your implementation do?
A Constrained Device Application, or CDA, is a software application that runs on a "constrained" (ie. resource-limited) device. The purpose of the CDA is to gather sensor data, control actuators, and communicate this information to other devices.

This lab focuses on getting the configuration environments correctly set up for the project, hence the implemenetation for the first iteration is simple in design. For this module, the implementation interfaces with a configuration utility named <b>ConfigUtil</b>. This utility wrapper (which is part of the Apache Commons configuration architecture) is used for managing the configuration settings within the application (app/system/environemt-specific configurations etc.). In the context of this application, the 

### How does your implementation work?

## Code Repository and Branch
Please click the link before to be directed to the CDA repository.

URL: https://github.com/Darren-C26/piot-python-components/tree/labmodule01

## UML Design Diagram(s)
![CDA Implementation UML](image-6.png)
<p style="text-align: center;">CDA Implementation UML</p>

## Unit Tests Executed
The unit tests executed for the <b>CDA</b> are listed below.
 - ConfigUtilTest
```
Finding files... done.
Importing test modules ... done.

2023-09-17 20:48:42,691:ConfigUtilTest:INFO:Testing ConfigUtil class...
2023-09-17 20:48:42,692:ConfigUtil:INFO:Loading config: ./ValidTestConfig.props
2023-09-17 20:48:42,693:ConfigUtil:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2023-09-17 20:48:42,694:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x0000026078689330>
----------------------------------------------------------------------
Ran 8 tests in 0.003s

OK (skipped=1)
```
Test Execution Sample:

## Integration Tests Executed
The integration tests for the <b>CDA</b> are listed below.

 - GatewayDeviceAppTest

Text Execution Sample:
```
Finding files... done.
Importing test modules ... done.

2023-09-17 20:47:29,210:root:INFO:Testing ConstrainedDeviceApp class...
2023-09-17 20:47:29,210:root:INFO:Initializing CDA...
2023-09-17 20:47:29,210:root:INFO:Starting CDA...
2023-09-17 20:47:29,210:root:INFO:CDA started.
2023-09-17 20:47:29,210:root:INFO:CDA stopping...
2023-09-17 20:47:29,210:root:INFO:CDA stopped with exit code 0.
----------------------------------------------------------------------
Ran 1 test in 0.001s

OK
```