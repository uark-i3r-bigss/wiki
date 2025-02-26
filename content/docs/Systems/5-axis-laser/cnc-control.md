---
title: CNC Control
weight: 1
---

Firmware
--------

*   [grbl-Mega-5X](https://github.com/fra589/grbl-Mega-5X), 5/6 Axis Grbl written in optimized C that runs on an Arduino Mega2560
    *   My fork: [liushuya7/grbl-Mega-5X](https://github.com/liushuya7/grbl-Mega-5X)
*   [grblHAL](https://github.com/grblHAL), [high performance motion control for CNC](https://www.grbl.org/what-is-grblhal)
    *   [grblHAL driver for ST STM32F4xx](https://github.com/grblHAL/STM32F4xx) (Nucleo-64, Blackpill)
    *   [grblHAL-teensy-4.x](https://github.com/phil-barrett/grblHAL-teensy-4.x), GRBL Breakout Boards for Teensy 4.x
        *   [Teensy 4.1 based 5 Axis CNC Controller](https://hackaday.io/project/175209-teensy-41-cnc-controller)
*   [grbl32](https://github.com/thomast777/grbl32), a [6-Axis 32-bit CNC Controller](http://tomsrobotics.com/product/grbl32-6-axis-cnc-controller-g6f4-500khz/) based on STM32F407
    *   [jacobmcollier/grbl32](https://github.com/jacobmcollier/grbl32)
*   [Marlin 3D Printer Firmware](https://marlinfw.org/) \[[Github](https://github.com/MarlinFirmware/Marlin)\] → supports SAMD51P20A Cortex-M4 Adafruit Grand Central M4
*   [g2core](https://github.com/synthetos/g2), a 9 axes (XYZABC+UVW) motion control firmware running on **Arduino Due**
    *   [g2Core-Documentation](https://github.com/Rajpratik71/g2Core-Documentation)
    *   [Motate](https://github.com/synthetos/Motate/wiki), a bare-metal framework for multiple processor architectures
    *   [node-g2core-api](https://github.com/synthetos/node-g2core-api/tree/node-12-refactor)
        *   $ npm install [https://github.com/synthetos/node-g2core-api.git](https://github.com/synthetos/node-g2core-api.git)#node-12-refactor --save
    *   Pin Mapping Tabel
        *   [Arduino Due](https://www.arduino.cc/en/Hacking/PinMappingSAM3X)
        *   [Arduino Mega 2560](https://www.arduino.cc/en/Hacking/PinMapping2560)
*   [uCNC](https://forum.v1engineering.com/t/cnc/14495), [A universal CNC firmware for microcontrollers](https://github.com/Paciente8159/uCNC)
*   [Adafruit Grand Central M4 Express](https://learn.adafruit.com/adafruit-grand-central)
    *   [Adafruit CircuitPython Libraries](https://circuitpython.readthedocs.io/projects/bundle/en/latest/drivers.html)
*   [Gcode Documentation - Marline](https://marlinfw.org/meta/gcode/)

GUI
---

*   [Universal Gcode Sender](https://winder.github.io/ugs_website/)
*   [**cn5X++**](https://github.com/fra589/cn5X), a 5/6 axis Grbl GUI for grbl-Mega-5X capabilities implemented in Python
    *   My fork: [liushuya7/grbl\_ros2\_gui](https://github.com/liushuya7/grbl_ros2_gui) (requires ROS2)
*   [LaserWeb4](https://laserweb.yurl.ch/), generating GCODE from DXF/SVG/JPG/PNG files for Lasers machine
*   [SimpleGCodeSender](https://github.com/Kelvintronic/SimpleGCodeSender), an extremely simple serial sender written in C++

CAD/CAM
-------

*   [**COMPAS**](https://compas.dev/), provides data structures, geometry processing, [robotic fabrication](https://gramaziokohler.github.io/compas_fab/latest/) w/ CAD Integration
    *   [compas API](https://compas.dev/compas/latest/api/compas.html)
    *   [compas\_fab API](https://gramaziokohler.github.io/compas_fab/latest/reference.html)
        *   [campas\_fab workshop TU Munich 20.11.2020](https://github.com/gramaziokohler/workshop_munich_2020)
*   [OpenCAMLib](https://github.com/aewallin/opencamlib), a C++ library with python bindings for creating 3D toolpaths for CNC machines
*   [Bark-beetle-parametric-toolpaths](https://github.com/fellesverkstedet/Bark-beetle-parametric-toolpaths), a grasshopper plugin for digital fabrication (3D printers, CNC milling, Laser cutters, Robot arms and more).
    *   [Grasshopper plugin](https://github.com/visose/Robots) for programming KUKA and UR robots

Example
-------

*   [PlanetCNC](https://planet-cnc.com/), CNC USB Controllers, complete hardware and software solutions.
*   [Dorna](https://github.com/dorna-robotics/dorna), a small 5-axis robotic arm based on g2core
    *   [dorna\_arm\_ros](https://github.com/rakutentech/dorna_arm_ros), a ROS implementation
*   [RoboDK Robot Driver Template](https://github.com/egehandulger/robodkdriver)

Calibration
-----------

*   [Calibrating Stepper Motor Machines with Belts and Pulleys](https://www.norwegiancreations.com/2015/07/tutorial-calibrating-stepper-motor-machines-with-belts-and-pulleys/)

Other Packages
--------------

*   [PySLM Python Library for Selective Laser Melting and Additive Manufacturing](https://github.com/drlukeparry/pyslm/tree/master)