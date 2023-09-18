# Gateway Device Application (Connected Devices)

## Lab Module 01

## Description
### What does your implementation do?
A Gateway Device Application, or GDA, is a software application that acts as an intermediary between IoT devices (ie. constrained devices) and a cloud/edge-computing infrastructure. In particular, the GDA faciliates the communication and the exchange of data between the CDA and the cloud.

This lab focuses on getting the configuration environments correctly set up for the project, hence the implemenetation for the first iteration is simple in design. For this module, the GDA interfaces with a configuration utility named <b>ConfigUtil</b>. This utility wrapper (which is part of the Apache Commons configuration architecture) is used for managing the configuration settings within the application (app/system/environemt-specific configurations etc.).

### How does your implementation work?

The ConfigUtil class initializes by setting a configuration file name (can be set as a property or given the default name) and loads the configuration data from this file into an <b>INIConfiguration</b> object. The configuration settings are stored as properties, which are retrieved through various methods provided by the ConfigUtil class. It also includes methods to load and return credentials from seperate credential files.

In the GDA's constructor, the initialization process begins with a call to the <b>initConfig</b> method. This method is responsible for loading the configuration file, and it uses the ConfigUtil class to manage the configuration settings. Additionally, the parseArgs command is used to parse command line arguments, allowing for a custom configuration file name to override the default settings provided by ConfigUtil.

## Code Repository and Branch
Please click the link before to be directed to the GDA repository.

URL: https://github.com/Darren-C26/piot-java-components/tree/labmodule01

## UML Design Diagram(s)
![GDA Implementation UML](image-7.png)
<p style="text-align: center;">GDA Implementation UML</p>

## Unit Tests Executed
The unit tests executed for the <b>GDA</b> are listed below.
#### Required:
 - ConfigUtilTest
```
Sep. 17, 2023 10:34:55 P.M. programmingtheiot.common.ConfigUtil getCredentials
INFO: Successfully loaded credentials from file: ./src/test/java/programmingtheiot/part01/unit/common/DummyCredFile.props
```
#### Other Tests:
 - ResourceNameTest
 - SystemCpuUtilTaskTest
 - SystemMemUtilTaskTest

Test Execution Sample (Using Maven):
![ConfigUtilTest](image-2.png)
![ResourceNameTest](image-3.png)
![SystemCpuUtilTaskTest](image-4.png)
![SystemMemUtilTaskTest](image-5.png)

## Integration Tests Executed
The integration tests for the <b>GDA</b> are listed below.

#### Required:
 - GatewayDeviceAppTest
```
Sep. 17, 2023 10:33:15 P.M. programmingtheiot.gda.app.GatewayDeviceApp <init>
INFO: Initializing GDA...
Sep. 17, 2023 10:33:15 P.M. programmingtheiot.gda.app.GatewayDeviceApp parseArgs
INFO: No command line args to parse.
Sep. 17, 2023 10:33:15 P.M. programmingtheiot.gda.app.GatewayDeviceApp initConfig
INFO: Attempting to load configuration: Default.
Sep. 17, 2023 10:33:15 P.M. programmingtheiot.gda.app.GatewayDeviceApp startApp
INFO: Starting GDA...
Sep. 17, 2023 10:33:15 P.M. programmingtheiot.gda.app.GatewayDeviceApp startApp
INFO: GDA started successfully.
```

#### Other Tests:
 - SystemPerformanceManagerTest

Text Execution Sample (using Maven):
![GatewayDeviceAppTest](image.png)
![SystemPerformanceManagerTest](image-1.png)
