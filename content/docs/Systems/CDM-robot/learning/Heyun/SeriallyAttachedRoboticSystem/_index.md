---
title: "SeriallyAttachedRoboticSystem Class Documentation"
---
Cleanup(): This method calls the disable() method to disable the motor.
Configure(const std::string &filename): This method accepts a filename as a parameter and calls the loadMotorConfiguration(filename) method to load the motor's configuration file.
resetTimingVariables(): This method resets timing-related variables, including setVelocityStartTime, setVelocityEndTime, moveVelocityStartTime, moveVelocityEndTime, stopStartTime, and stopEndTime.
Run(): This method first gets the current system time and resets timing-related variables. Then, it processes commands in the queue and updates the motor's status. If the motor is enabled, it calls the updateStatus() method to update the motor's status. If the motor is in homing mode, it calls the checkForceHoming() method to check force-controlled homing. If the motor is in setpoint mode, it moves the motor.
setPositionMode(): This method first calls the stop() method to stop the motor, then sets operationalMode to OMD_PROFILE_POSITION_MODE, and calls the VCS_SetOperationMode() method to set the motor's operation mode to position mode.
setVelocityMode(): This method first calls the stop() method to stop the motor, then sets operationalMode to OMD_PROFILE_VELOCITY_MODE, and calls the VCS_SetOperationMode() method to set the motor's operation mode to velocity mode.
getVelocityProfile(): This method calls the VCS_GetVelocityProfile() method to get the motor's velocity profile.
setVelocityProfile(): This method calls the VCS_SetVelocityProfile() method to set the motor's velocity profile.
getPositionProfile(): This method calls the VCS_GetPositionProfile() method to get the motor's position profile.
setPositionProfile(): This method first calculates the absolute value of the target velocity, then calls the VCS_SetPositionProfile() method to set the motor's position profile.
On this page, we see some methods of the maxonMotor class:
moveToAbsolutePosition() and moveToAbsolutePosition_raw(): Both of these methods are used to move the motor to an absolute position. They accept a position parameter and call the moveToPosition() or moveToPosition_raw() method to implement it.
moveToRelativePosition() and moveToRelativePosition_raw(): Both of these methods are used to move the motor to a relative position. They accept a position parameter and call the moveToPosition() or moveToPosition_raw() method to implement it.
moveToPosition() and moveToPosition_raw(): Both of these methods are used to move the motor to a specified position. They accept a position parameter, a boolean value indicating whether it is an absolute position, and a boolean value indicating whether to move immediately. Then, they call the VCS_MoveToPosition() method to implement it.
jogPlus(): This method first prints a message indicating that the motor is moving at a positive velocity. Then, it records the start time ofthe movement and calls the VCS_MoveWithVelocity() method to move the motor. Finally, it records the end time of the movement.
setMaxVelocity() and setMaxVelocity_raw(): Both of these methods are used to set the maximum speed of the motor. They accept a speed parameter and call the VCS_SetMaxProfileVelocity() method to implement it.
getMaxVelocity(): This method calls the VCS_GetMaxProfileVelocity() method to get the maximum speed of the motor.
setMaxAcceleration() and setMaxAcceleration_raw(): Both of these methods are used to set the maximum acceleration of the motor. They accept an acceleration parameter and call the VCS_SetMaxAcceleration() method to implement it.
getMaxAcceleration(): This method calls the VCS_GetMaxAcceleration() method to get the maximum acceleration of the motor.
setPositionMode(): This method first calls the stop() method to stop the motor, then sets operationalMode to OMD_PROFILE_POSITION_MODE, and calls the VCS_SetOperationMode() method to set the motor's operation mode to position mode.
setVelocity(), setVelocity_raw(), setVelocityPoint(), and setVelocityPoint_raw(): These methods are all used to set the speed of the motor. They accept a speed parameter and call the setPositionProfile() method to set the motor's position profile. These methods also record the start and end times of setting the speed.
getTargetVelocity_raw() and getTargetVelocity(): Both of these methods are used to get the target speed of the motor.
createInterface(): This method creates an interface and adds some data to the state table, including operationMode, enabled, position_raw, velocity_raw, velocityAverage_raw, position, velocity, velocityAverage, current, currentAverage, fault, time, targetReached, force, numCommandsProcessed, startTime, and endTime, etc.
setVelocity(), setVelocity_raw(), setVelocityPoint(), and setVelocityPoint_raw(): These methods are all used to set the speed of the motor. They accept a speed parameter and call the setPositionProfile() method to set the motor's position profile. These methods also record the start and end times of setting the speed.
getTargetVelocity_raw() and getTargetVelocity(): Both of these methods are used to get the target speed of the motor.
createInterface(): This method creates an interface and adds some data to the state table, including operationMode, enabled, position_raw, velocity_raw, velocityAverage_raw, position, velocity, velocityAverage, current, currentAverage, fault, time, targetReached, force, numCommandsProcessed, startTime, and endTime, etc.
The code on page 7 mainly includes the following parts:
maxonMotor::setVelocityMode() and maxonMotor::setPositionMode() functions: These two functions are used to set the operation mode of the motor to velocity mode and position mode, respectively. Before setting a new operation mode, the stop() function is called to stop the operation of the motor.
maxonMotor::getVelocityProfile() and maxonMotor::setVelocityProfile() functions: These two functions are used to get and set the velocity profile of the motor.
maxonMotor::getPositionProfile() and maxonMotor::setPositionProfile() functions: These two functions are used to get and set the position profile of the motor.
maxonMotor::moveToAbsolutePosition() function: This function is used to move the motor to a given absolute position.
maxonMotor::setMaxVelocity(), maxonMotor::getMaxVelocity(), maxonMotor::setMaxAcceleration(), and maxonMotor::getMaxAcceleration(), etc. These functions are used to set and get the maximum speed and maximum acceleration of the motor.

