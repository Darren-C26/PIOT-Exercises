# Gateway Device Application (Connected Devices)

## Lab Module 02

## Description
### What does your implementation do?
A Gateway Device Application, or GDA, is a software application that acts as an intermediary between IoT devices (ie. constrained devices) and a cloud/edge-computing infrastructure. In particular, the GDA faciliates the communication and the exchange of data between the CDA and the cloud.

This lab focuses on getting the configuration environments correctly set up for the project, hence the implemenetation for the first iteration is simple in design. For this module, the GDA interfaces with a configuration utility named <b>ConfigUtil</b>. This utility wrapper (which is part of the Apache Commons configuration architecture) is used for managing the configuration settings within the application (app/system/environemt-specific configurations etc.).

### How does your implementation work?

The ConfigUtil class initializes by setting a configuration file name (can be set as a property or given the default name) and loads the configuration data from this file into an <b>INIConfiguration</b> object. The configuration settings are stored as properties, which are retrieved through various methods provided by the ConfigUtil class. It also includes methods to load and return credentials from seperate credential files.

In the GDA's constructor, the initialization process begins with a call to the <b>initConfig</b> method. This method is responsible for loading the configuration file, and it uses the ConfigUtil class to manage the configuration settings. Additionally, the parseArgs command is used to parse command line arguments, allowing for a custom configuration file name to override the default settings provided by ConfigUtil.

## Code Repository and Branch
Please click the link before to be directed to the GDA repository.

URL: https://github.com/Darren-C26/piot-java-components/tree/labmodule02

## UML Design Diagram(s)

<p style="text-align: center;">GDA Implementation UML</p>

## Unit Tests Executed
The unit tests executed for the <b>GDA</b> are listed below. Sample test executions can be seen by clicking on the dropdown icon.

#### Required:

<details close>
<summary>ConfigUtilTest</summary>

```
Sep. 22, 2023 7:02:11 P.M. programmingtheiot.common.ConfigUtil getCredentials
INFO: Successfully loaded credentials from file: ./src/test/java/programmingtheiot/part01/unit/common/DummyCredFile.props
```
</details>
<br>

<details close>
<summary>SystemCpuUtilTaskTest</summary>

```
Sep. 22, 2023 7:56:50 P.M. programmingtheiot.part01.unit.system.SystemCpuUtilTaskTest testGetTelemetryValue
INFO: Test 1: CPU Util not supported on this OS: -1.0
Sep. 22, 2023 7:56:50 P.M. programmingtheiot.part01.unit.system.SystemCpuUtilTaskTest testGetTelemetryValue
INFO: Test 2: CPU Util not supported on this OS: -1.0
Sep. 22, 2023 7:56:50 P.M. programmingtheiot.part01.unit.system.SystemCpuUtilTaskTest testGetTelemetryValue
INFO: Test 3: CPU Util not supported on this OS: -1.0
Sep. 22, 2023 7:56:50 P.M. programmingtheiot.part01.unit.system.SystemCpuUtilTaskTest testGetTelemetryValue
INFO: Test 4: CPU Util not supported on this OS: -1.0
Sep. 22, 2023 7:56:50 P.M. programmingtheiot.part01.unit.system.SystemCpuUtilTaskTest testGetTelemetryValue
INFO: Test 5: CPU Util not supported on this OS: -1.0
```
</details>
<br>

<details close>
<summary>SystemMemUtilTaskTest</summary>

```
Sep. 22, 2023 8:03:37 P.M. programmingtheiot.part01.unit.system.SystemMemUtilTaskTest testGetTelemetryValue
INFO: Test 1: Memory Util: 0.19753087
Sep. 22, 2023 8:03:37 P.M. programmingtheiot.part01.unit.system.SystemMemUtilTaskTest testGetTelemetryValue
INFO: Test 2: Memory Util: 0.19753087
Sep. 22, 2023 8:03:37 P.M. programmingtheiot.part01.unit.system.SystemMemUtilTaskTest testGetTelemetryValue
INFO: Test 3: Memory Util: 0.19753087
Sep. 22, 2023 8:03:37 P.M. programmingtheiot.part01.unit.system.SystemMemUtilTaskTest testGetTelemetryValue
INFO: Test 4: Memory Util: 0.19753087
Sep. 22, 2023 8:03:37 P.M. programmingtheiot.part01.unit.system.SystemMemUtilTaskTest testGetTelemetryValue
INFO: Test 5: Memory Util: 0.19753087
```
</details>
<br>

#### Other Tests:
 - ResourceNameTest


## Integration Tests Executed
The integration tests for the <b>GDA</b> are listed below. Sample test executions can be seen by clicking on the dropdown icon.

<details close>
<summary>GatewayDeviceAppTest</summary>

```
Sep. 22, 2023 8:29:43 P.M. programmingtheiot.gda.app.GatewayDeviceApp <init>
INFO: Initializing GDA...
Sep. 22, 2023 8:29:43 P.M. programmingtheiot.gda.app.GatewayDeviceApp startApp
INFO: Starting GDA...
Sep. 22, 2023 8:29:43 P.M. programmingtheiot.gda.system.SystemPerformanceManager startManager
INFO: SystemPerformanceManager is starting...
Sep. 22, 2023 8:29:43 P.M. programmingtheiot.gda.app.GatewayDeviceApp startApp
INFO: GDA started successfully.
Sep. 22, 2023 8:29:44 P.M. programmingtheiot.gda.system.SystemPerformanceManager handleTelemetry
INFO: CPU utilization: -1.0, Mem utilization: 0.34567901
Sep. 22, 2023 8:30:44 P.M. programmingtheiot.gda.system.SystemPerformanceManager handleTelemetry
INFO: CPU utilization: -1.0, Mem utilization: 0.34567901
Sep. 22, 2023 8:30:48 P.M. programmingtheiot.gda.app.GatewayDeviceApp stopApp
INFO: Stopping GDA...
Sep. 22, 2023 8:30:48 P.M. programmingtheiot.gda.system.SystemPerformanceManager stopManager
INFO: SystemPerformanceManager is stopped.
Sep. 22, 2023 8:30:48 P.M. programmingtheiot.gda.app.GatewayDeviceApp stopApp
INFO: GDA stopped successfully with exit code 0.
```
</details>

<br>

<details close>
<summary>SystemPerformanceManagerTest</summary>

```
Sep. 22, 2023 7:29:30 P.M. programmingtheiot.gda.system.SystemPerformanceManager startManager
INFO: SystemPerformanceManager is starting...
Sep. 22, 2023 7:29:36 P.M. programmingtheiot.gda.system.SystemPerformanceManager stopManager
INFO: SystemPerformanceManager is stopped.
```
</details>