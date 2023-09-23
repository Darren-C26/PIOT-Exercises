# Constrained Device Application (Connected Devices)

## Lab Module 02

## Description

### What does your implementation do?
A Constrained Device Application, or CDA, is a software application that runs on a "constrained" (ie. resource-limited) device. The purpose of the CDA is to gather sensor data, control actuators, and communicate this information to other devices.

In the context of this project, the CDA is designed to collect temperature, humidity, and pressure data from sensors. However, as this is the first module, only shell implementations have been provided. The components that were observed for this module include the <b>ConstrainedDeviceApp</b> class and the <b>ConfigUtil</b> class. ConfigUtil is a configuration utility used to manage the configuration settings of the application.

### How does your implementation work?

The ConfigUtil class is used for managing configuration settings for the CDA. It can be initialized with a specified configuration file name (or will use the default one). It provides methods to retrieve configuration values, checks for the existence of keys and sections in the configuration file, and can load separate credential files. The CDA requires certain configuration settings to behave a certain way. Upon initializing, it will make a call to ConfigUtil for it to retrieve configuration parameters required for runtime.

## Code Repository and Branch
Please click the link before to be directed to the CDA repository.

URL: https://github.com/Darren-C26/piot-python-components/tree/labmodule02

## UML Design Diagram(s)

<p style="text-align: center;">CDA Implementation UML</p>

## Unit Tests Executed
The unit tests executed for the <b>CDA</b> are listed below. Sample test executions can be seen by clicking on the dropdown icon.

<details close>
<summary>ConfigUtilTest</summary>

```
Finding files... done.
Importing test modules ... done.

2023-09-22 20:42:58,167:ConfigUtilTest:INFO:Testing ConfigUtil class...
2023-09-22 20:42:58,168:ConfigUtil:INFO:Loading config: ./ValidTestConfig.props
2023-09-22 20:42:58,178:ConfigUtil:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2023-09-22 20:42:58,178:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x000002EA46358DC0>
----------------------------------------------------------------------
Ran 8 tests in 0.012s

OK (skipped=1)
```
</details>

<br>

<details close>
<summary>SystemCpuUtilTaskTest</summary>

```
Finding files... done.
Importing test modules ... done.

2023-09-22 21:27:45,167:SystemCpuUtilTaskTest:INFO:Testing SystemCpuUtilTask class...
2023-09-22 21:27:45,167:SystemCpuUtilTaskTest:INFO:CPU utilization: 0.0
----------------------------------------------------------------------
Ran 1 test in 0.001s

OK
```
</details>
<br>

<details close>
<summary>SystemMemUtilTaskTest</summary>

```
Finding files... done.
Importing test modules ... done.

2023-09-22 21:33:36,855:SystemMemUtilTaskTest:INFO:Testing SystemMemUtilTask class...
2023-09-22 21:33:36,863:SystemMemUtilTaskTest:INFO:Virtual memory utilization: 92.4
----------------------------------------------------------------------
Ran 1 test in 0.008s

OK
```
</details>

<br>

## Integration Tests Executed
The integration tests for the <b>CDA</b> are listed below.

<details close>
<summary>ConstrainedDeviceAppTest</summary>

```
Finding files... done.
Importing test modules ... done.

2023-09-22 20:44:04,019:root:INFO:Testing ConstrainedDeviceApp class...
2023-09-22 20:44:04,019:root:INFO:Initializing CDA...
2023-09-22 20:44:04,019:root:INFO:Loading config: ../../../../../../../config/PiotConfig.props
2023-09-22 20:44:04,027:root:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2023-09-22 20:44:04,028:root:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x000001EED861A380>
2023-09-22 20:44:04,028:tzlocal:DEBUG:Looking up time zone info from registry
2023-09-22 20:44:04,053:apscheduler.scheduler:INFO:Adding job tentatively -- it will be properly scheduled when the scheduler starts
2023-09-22 20:44:04,054:root:INFO:Starting CDA...
2023-09-22 20:44:04,054:root:INFO:Starting SystemPerformanceManager...
2023-09-22 20:44:04,056:apscheduler.scheduler:INFO:Added job "SystemPerformanceManager.handleTelemetry" to job store "default"
2023-09-22 20:44:04,056:apscheduler.scheduler:INFO:Scheduler started
2023-09-22 20:44:04,057:apscheduler.scheduler:DEBUG:Looking for jobs to run
2023-09-22 20:44:04,057:apscheduler.scheduler:DEBUG:Next wakeup is due at 2023-09-22 20:44:09.053672-04:00 (in 4.995731 seconds)
2023-09-22 20:44:04,057:root:INFO:Started SystemPerformanceManager.
2023-09-22 20:44:04,057:root:INFO:CDA started.
2023-09-22 20:44:04,057:root:INFO:CDA stopping...
2023-09-22 20:44:04,057:root:INFO:Stopping SystemPerformanceManager...
2023-09-22 20:44:04,057:apscheduler.scheduler:INFO:Scheduler has been shut down
2023-09-22 20:44:04,058:apscheduler.scheduler:DEBUG:Looking for jobs to run
2023-09-22 20:44:04,058:apscheduler.scheduler:DEBUG:No jobs; waiting until a job is added
2023-09-22 20:44:04,058:root:INFO:Stopped SystemPerformanceManager.
2023-09-22 20:44:04,058:root:INFO:CDA stopped with exit code 0.
----------------------------------------------------------------------
Ran 1 test in 0.039s

OK
```

</details>
<br>

<details close>
<summary>SystemPerformanceManagerTest</summary>

```
Finding files... done.
Importing test modules ... done.

2023-09-22 21:22:00,333:SystemPerformanceManagerTest:INFO:Testing SystemPerformanceManager class...
2023-09-22 21:22:00,333:ConfigUtil:INFO:Loading config: ../../../../../../../config/PiotConfig.props
2023-09-22 21:22:00,334:ConfigUtil:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2023-09-22 21:22:00,334:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x00000232D455B880>
2023-09-22 21:22:00,334:win32:DEBUG:Looking up time zone info from registry
2023-09-22 21:22:00,343:base:INFO:Adding job tentatively -- it will be properly scheduled when the scheduler starts
2023-09-22 21:22:00,343:SystemPerformanceManager:INFO:Starting SystemPerformanceManager...
2023-09-22 21:22:00,345:base:INFO:Added job "SystemPerformanceManager.handleTelemetry" to job store "default"
2023-09-22 21:22:00,345:base:INFO:Scheduler started
2023-09-22 21:22:00,345:base:DEBUG:Looking for jobs to run
2023-09-22 21:22:00,346:SystemPerformanceManager:INFO:Started SystemPerformanceManager.
2023-09-22 21:22:00,346:base:DEBUG:Next wakeup is due at 2023-09-22 21:22:05.343262-04:00 (in 4.996998 seconds)
2023-09-22 21:22:05,357:base:DEBUG:Looking for jobs to run
2023-09-22 21:22:05,358:base:INFO:Running job "SystemPerformanceManager.handleTelemetry (trigger: interval[0:00:05], next run at: 2023-09-22 21:22:05 EDT)" (scheduled at 2023-09-22 21:22:05.343262-04:00)
2023-09-22 21:22:05,359:SystemPerformanceManager:DEBUG:CPU utilization is 14.6 percent, and memory utilization is None percent.
2023-09-22 21:22:05,359:base:INFO:Job "SystemPerformanceManager.handleTelemetry (trigger: interval[0:00:05], next run at: 2023-09-22 21:22:05 EDT)" executed successfully
2023-09-22 21:22:05,360:base:DEBUG:Next wakeup is due at 2023-09-22 21:22:10.343262-04:00 (in 4.982601 seconds)
2023-09-22 21:22:06,349:SystemPerformanceManager:INFO:Stopping SystemPerformanceManager...
2023-09-22 21:22:06,350:base:INFO:Scheduler has been shut down
2023-09-22 21:22:06,350:base:DEBUG:Looking for jobs to run
2023-09-22 21:22:06,350:base:DEBUG:No jobs; waiting until a job is added
2023-09-22 21:22:06,350:SystemPerformanceManager:INFO:Stopped SystemPerformanceManager.
----------------------------------------------------------------------
Ran 1 test in 6.018s

OK
```

</details>