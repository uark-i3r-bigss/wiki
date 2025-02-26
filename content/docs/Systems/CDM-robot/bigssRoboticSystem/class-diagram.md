---
title: A Class Example Diagram
---

{{< mermaid >}}
classDiagram
    direction TB
    KinematicsObject <|-- RobotInterfaceObject
    mtsComponent <|-- RobotInterfaceObject
    mtsComponent <|-- SensorInterface
    class KinematicsObject{
        +prmKinematicsState kinematics_state
        +int num_joints
        +std::string name
        -prmStateJoint joint_state
        +GetNumberOfJoints() int
        +UpdateState() bool
        +InitializeKinematicsStateSize()
    }
    class RobotInterfaceObject{
        +vctFrm3 frame_offset_to_base
        +std::string interface_name
        +int num_joints
        +std::string base_frame_name
        +std::vector~SensorInterface*~ sensor_interfaces
        +std::vector~mtsInterfaceRequired*~ command_interfaces
        +std::vector~mtsFunctionWrite*~ command_functions
        +std::vector~mtsInterfaceRequired*~ read_interfaces
        +std::vector~mtsFunctionRead*~ read_functions  
        +prmPositionCartesianGet m_measured_cp
        +prmPositionCartesianGet m_base_offset_measured_cp
        MoveRobot(prmVelocityJointSet& command)
        UpdateSensors()
    }
    class SensorInterface{
        +std::string interface_name
        +prmSensorState sensor_state
        +std::vector~mtsInterfaceRequired*~ read_interfaces
        +std::vector~mtsFunctionRead*~ read_functions
        +Update() bool
    }
    click KinematicsObject href "https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/KinematicsObject.h"
    click RobotInterfaceObject href "https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/RobotInterfaceObject.h"
    click SensorInterface href "https://git.lcsr.jhu.edu/bigss/bigssRoboticSystem/-/blob/master/components/include/bigssRoboticSystem/SensorInterface.h"
{{< /mermaid >}}