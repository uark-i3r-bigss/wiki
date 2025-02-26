---
title: UR Driver
---

# Test with URSim eSeries

Install the [universalrobots/ursim_e-series](https://hub.docker.com/r/universalrobots/ursim_e-series) docker image, then run:

```bash
sudo docker run --rm -it --net host -e ROBOT_MODEL=UR10 universalrobots/ursim_e-series
```

To enable URCap External Control, mount the `/urcaps` folder to a folder containing the urcaps jar files, at start time:

```bash
sudo docker run --rm -it --net host -e ROBOT_MODEL=UR10 -v "/home/host_machine_username/urcaps:/urcaps" universalrobots/ursim_e-series
```

# Universal Robots ROS2 Driver

Follow the build instructions in the official [Universal Robots ROS2 Driver](https://github.com/UniversalRobots/Universal_Robots_ROS2_Driver) repository to install the driver.



