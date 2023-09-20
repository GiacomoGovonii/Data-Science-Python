# ERC Remote Navigation Simulation

This repository provides a Gazebo simulation of the Navigation and Science Task for the EuropeanRoverChallenge Remote competition. \
For the dockerized version, skip to the [Using Docker](#using-docker) section.

## Table of Contents
1. [Prerequisites](#prerequisites)
1. [Building](#building)
1. [Updating](#updating)
1. [Launching](#launching)
1. [Using Docker](#using-docker)
1. [ROS API](#ros-api)
    1. [Subscribed Topics](#subscribed-topics)
    1. [Published Topics](#published-topics)
    1. [Services](#services)
    1. [Parameters Set](#parameters-set)
1. [Troubleshooting](#troubleshooting)


The command mapping was set for the Xbox 360 controller and looks like this:
| Xbox 360 controller       | Command                                |
|---------------------------|----------------------------------------|
| RB button                 | enable - hold it to send commands      |
| Left joystick Up/Down     | linear velocity                        |
| Right Joystick Left/Right | angular velocity                       |
| A button                  | drop the next probe                    |
| B button                  | despawn probes and reset probe counter |

To modify it, you can edit the `joy_mapping.yaml` file inside the `leo_erc_teleop` package.

## Using Docker

---
**NOTE**

All of the commands in this section should be executed as the `root` user, unless you have configured docker to be [managable as a non-root user](https://docs.docker.com/engine/install/linux-postinstall/).

---
