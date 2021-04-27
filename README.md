# The CWRU `glennan_second_floor` ROS Package

## Introduction

This package was create for use with CWRU Robotics platforms and courses.  It provides a simulation and mapt of the second floor of the hallways of the Glennan building.

## Use (Map)

The map is of adequate quality for basic navigation on the second floor.

It can be launched:

`roslaunch glennan_second_floor glennan_second_floor_map.launch`

### Input Parameters

There is one input parameter:
- `map_file` -- The path to an alternate map file



The map is in the `maps/glennan_second_floor_model_map.pgm` file and the configuration for the `map_server` is in the `configs/glennan_second_floor_model_map.yaml`.

## Use (World)

The simulation world is a simple 2D floor plan of the second floor extruded into 3D.

It can be launched:

`roslaunch glennan_second_floor glennan_world.launch`

### Input Parameters

This launch file leverages the typical `empty_world.launch` file from the `gazebo_ros` package.  It takes a subset of those parameters:

- `world_name` - The full path to the world file to use.  default `world_name:=$(find glennan_second_floor)/worlds/glennan_world.world`

