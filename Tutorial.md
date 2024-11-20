![](logo-ucsdjsoeece-white.png)
---
## Tutorial Parking Assistant Device
Last update: 11/20/2024

Authors:
  - Clevant Yang
  - Danny Wu
  - Aria Mottaghi
---


## Introduction

TODO

### Learning Objectives

- Background Information
- Tools Needed
- Get Started
- References

## Background Information

We are developing a device to assist drivers with parking, specifically in compact spots. This will be done with a LiDAR sensor that will map a 2D birds eye view of obstacles in front and to the side of the car. This map will then be displayed on a screen for the driver to see and make judgements accordingly while parking. The device will also detect empty parking spots to then measure the width and judge whether or not it is too compact to park in.

## Tools Needed
- PC with Windows 10 or later to upload code to ESP32, other platforms are not tested
- Arduino IDE 2.x, download it [here][Arduino IDE Link]
- Visual Studio Code, download it [here][VSCode Link]
- youyeetoo FHL-LD20 8 Meters 360 deg Lidar Sensor, you can find it [here][Lidar Link]
- ESP32-S3 Dev Module for wireless transfer data, we are using ESP-WROOM-32, you can find it [here][ESP32 Link]
- A ESP32 screen, we are using [this screen][Screen Link]
- A suction cup to stable lidar on car, we are using [this one][Suction Cup Link]
- Cables and Wires, be aware the screen is using USB-C, ESP32 is using Micro-USB

## Getting Started

#### Arduino IDE
First thing first. There are some changes and library needed. Open Arduino IDE, go to File->prefrences->Additional boards manager URLs, add this link, like this
>https://dl.espressif.com/dl/package_esp32_index.json


There are some libraries are needed. Inside Arduino IDE->Library Manager

#### Lidar
TODO

#### ESP32
The lidar doesn't have a wifi, and we need to display sensor data coming from outside of the car. We need wireless transfer. So we will be using **ESP-NOW**. ESP-NOW is a wireless communication protocol defined by Espressif, which enables the direct, quick and low-power control of smart devices, without the need of a router.
#### Screen
The lidar will be sending 47-bytes hexadecimal data string, they are distance and angle of objects that your lidar detected. They can be represented in Polar coordinate, however, the screen use Cartesian coordinate, so we need to transform distances and angles to x and y axis.

### Required Downloads and Installations

List any required downloads and installations here.
Make sure to include tutorials on how to install them.
You can either make your own tutorials or include a link to them.


### Required Tools and Equipment

List any tools and equipment you need here.
(Ex, computer, soldering station, etc.)

## Part 01: Name

### Introduction

Briefly introduce what  you are teaching in this section.

### Objective

- List the learning objectives of this section

### Background Information

Give a brief explanation of the technical skills learned/needed
in this challenge. There is no need to go into detail as a
separation document should be prepared to explain more in depth
about the technical skills

### Components

- List the components needed in this challenge

### Instructional

Teach the contents of this section

## Example

### Introduction

Introduce the example that you are showing here.

### Example

Present the example here. Include visuals to help better understanding

### Analysis

Explain how the example used your tutorial topic. Give in-depth analysis of each part and show your understanding of the tutorial topic

## Additional Resources

### Useful links

List any sources you used, documentation, helpful examples, similar projects etc.



[Lidar Link]: https://www.amazon.com/youyeetoo-FHL-LD20-Raspberry-Triangulated-Start-Stop/dp/B0C3CX17FN
[ESP32 Link]: https://www.amazon.com/dp/B08D5ZD528?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1
[Screen Link]: https://www.amazon.com/dp/B0D7HN3XQ5?ref=ppx_yo2ov_dt_b_fed_asin_title
[Suction Cup Link]: https://www.amazon.com/ThtRht-Suction-Windshield-Camcorder-Recorder/dp/B0CPLV4B9F
[ESP-NOW Link]: https://www.espressif.com/en/solutions/low-power-solutions/esp-now
[Arduino IDE Link]: https://www.arduino.cc/en/software
[VSCode Link]: https://code.visualstudio.com/