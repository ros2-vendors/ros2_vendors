# `ros2_vendors`

`ros2_vendors` is a metarepository that includes the `ros2_vendors.repos` configuration file for building ROS 2 vendor packages. A ROS 2 vendor package is a special package used to wrap third-party dependencies, making integration with the ROS 2 build and distribution system easier. These packages provide a standardized way to include external libraries or tools in a ROS 2 workspace.

`ros2_vendors.repos` is used by `vcstool` to clone and manage multiple Git repositories in a ROS 2 workspace. Written in YAML format, it lists the repositories required to build a complete ROS 2 workspace, ensuring all necessary vendor packages are included.


```bash
$ mkdir ros2_ws && cd ros2_ws
$ curl -O https://raw.githubusercontent.com/ros2/ros2/jazzy/ros2_vendors.repos

$ vcs import src < ros2_vendors.repos

$ colcon build
```
