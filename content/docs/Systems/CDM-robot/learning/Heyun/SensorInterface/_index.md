---
title: "SensorInterface Class Documentation"

---

## Overview

The `SensorInterface` is a C++ class authored by Henry Phalen. It is a derivative of the `mtsComponent` class and offers functionality to interact with a sensor system. The class is capable of updating sensor interfaces.

The corresponding source files are:
- Header file: [SensorInterface.h](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/RobotInterfaceObject.h)
- Source file: [SensorInterface.cpp](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/code/RobotInterfaceObject.cpp)

The `SensorInterface` class utilizes several libraries, including:

- `cisstVector`: A library for vector operations.
- `cisstMultiTask/mtsComponent`: A library for the multitask component.
- `sawConstraintController/prmSensorState`: A library defining the sensor state.
- `cisstMultiTask/mtsInterfaceRequired`: A library for required interface in the multitask component.
- `cisstMultiTask/mtsFunctionRead`: A library for read function in the multitask component.

## Class Definition

### Variables

- `interface_name`: A string storing the name of the `SensorInterface` instance.
- `sensor_state`: An instance of `prmSensorState`, representing the state of the sensor.
- `read_interfaces`: A vector storing pointers to `mtsInterfaceRequired` objects, used for read interfaces. (?)
- `read_functions`: A vector storing pointers to `mtsFunctionRead` objects, used for read functions. (?)

### Functions

- **Constructor `SensorInterface(const std::string& interface_name="SensorInterface")`**: This function initializes a `SensorInterface` instance with an optional interface name. It sets the name of the `mtsComponent` to be the given `interface_name`.
- **Destructor `~SensorInterface()`**: This function destroys the `SensorInterface` instance.
- **Function `Update()`**: A virtual function that updates the sensor interface. Its specific functionality might depend on the implementation in a derived class. (?)
