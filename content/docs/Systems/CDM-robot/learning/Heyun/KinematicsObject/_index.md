---
title: "KinematicsObject Class Documentation"
---

## Overview

The `KinematicsObject` is a C++ class authored by Henry Phalen, which provides a base definition for kinematic states, such as joints, positions, velocities, and more. This class is crucial in the design of robotic systems that need to track and manage kinematic states for different joints.

The corresponding source files are:
- Header file: [KinematicsObject.h](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/KinematicsObject.h)
- Source file: [KinematicsObject.cpp](https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/code/KinematicsObject.cpp)

The class utilizes other libraries, including `cisstVector`, `sawConstraintController/prmKinematicsState`, and `cisstParameterTypes/prmStateJoint`.

## Class Definition

Here's an outline of the `KinematicsObject` class:

### Variables

- `kinematics_state`: An instance of `prmKinematicsState`, used to store the state of kinematics.
- `num_joints`: An integer representing the number of joints.
- `name`: A string that stores the name of the KinematicsObject instance.

### Functions

- `KinematicsObject`: This is the constructor function that initializes a `KinematicsObject` instance. It accepts two optional parameters - a string `name` (default: "KinematicsObject"), and an integer `num_joints` (default: 0).
- `~KinematicsObject`: This is the destructor function for the `KinematicsObject` class.
- `GetNumberOfJoints`: This function returns the number of joints. It does not require any input parameters.
- `UpdateState`: A pure virtual function that needs to be overridden in any derived classes. This function allows for states to change and does not have any input or output.
- `InitializeKinematicsStateSize`: This function initializes the kinematic state variables (including joint state position, velocity, and effort) and sets their initial values to zero.

## Dependencies

The `KinematicsObject` class relies on the following external files:

- `cisstVector`: A library for vector operations.
- `sawConstraintController/prmKinematicsState`: A library for managing the state of kinematics.
- `cisstParameterTypes/prmStateJoint`: A library for managing the state of joints.

