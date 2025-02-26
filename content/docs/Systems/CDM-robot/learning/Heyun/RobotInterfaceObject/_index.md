---
title: "RobotInterfaceObject Class Documentation"

---

## Overview

The `RobotInterfaceObject` is a C++ class authored by Henry Phalen. It inherits from the `KinematicsObject` and `mtsComponent` classes and provides functionality to interface with a robot. The class can update sensors, initiate robot movements, and handle interfaces for reading and writing commands.

The corresponding source files are:
- Header file: [RobotInterfaceObject.h](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/RobotInterfaceObject.h)
- Source file: [RobotInterfaceObject.cpp](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/code/RobotInterfaceObject.cpp)

The class utilizes other libraries, including `cisstVector`, `cisstMultiTask/mtsComponent`, `bigssRoboticSystem/KinematicsObject`, `cisstMultiTask/mtsInterfaceRequired`, `cisstMultiTask/mtsFunctionWrite`, `bigssRoboticSystem/SensorInterface`, `cisstParameterTypes/prmVelocityJointSet`, and `cisstParameterTypes/prmPositionCartesianGet`.

## Class Definition

### Variables

- `frame_offset_to_base`: An instance of `vctFrm3` representing the offset to the base frame.
- `interface_name`: A string that stores the name of the RobotInterfaceObject instance.
- `num_joints`: An integer representing the number of joints.
- `base_frame_name`: A string storing the base frame's name.
- `sensor_interfaces`: A vector storing pointers to `SensorInterface` objects. (?)
- `command_interfaces`: A vector storing pointers to `mtsInterfaceRequired` objects, used for command interfaces. (?)
- `command_functions`: A vector storing pointers to `mtsFunctionWrite` objects, used for command functions. (?)
- `read_interfaces`: A vector storing pointers to `mtsInterfaceRequired` objects, used for read interfaces. (?)
- `read_functions`: A vector storing pointers to `mtsFunctionRead` objects, used for read functions. (?)
- `m_measured_cp`: An instance of `prmPositionCartesianGet`, representing the Cartesian position.
- `m_base_offset_measured_cp`: An instance of `prmPositionCartesianGet`, representing the base offset Cartesian position.

### Functions

- **Constructor `RobotInterfaceObject(const vctFrm3& frame_offset_to_base=vctFrm3(), const std::string& interface_name="RobotInterfaceObject", int num_joints=0, const std::string& base_frame_name="base")`:** This is the constructor function that initializes a `RobotInterfaceObject` instance with an optional frame offset to the base, interface name, number of joints, and base frame name.
- **Destructor `~RobotInterfaceObject()`:** This is the destructor function for the `RobotInterfaceObject` class.
- **Function `MoveRobot(prmVelocityJointSet& command)`:** A virtual function for robot movement. It takes as input a `prmVelocityJointSet` command. (?)
- **Function `UpdateSensors()`:** This function iterates through all the sensor interfaces and updates them.

## Dependencies

The `RobotInterfaceObject` class relies on the following external files:

- `cisstVector`: A library for vector operations.
- `cisstMultiTask/mtsComponent`: A library for the multitask component.
- `bigssRoboticSystem/KinematicsObject`: A library providing a base definition for kinematic states.
- `cisstMultiTask/mtsInterfaceRequired`: A library for required interface in the multitask component.
- `cisstMultiTask/mtsFunctionWrite`: A library for write function in the multitask component.
- `bigssRoboticSystem/SensorInterface`: A library for the sensor interface.
- `cisstParameterTypes/prmVelocityJointSet`: A library for managing the velocity of joints.
- `cisstParameterTypes/prmPositionCartesianGet`: A library for getting the Cartesian position.
