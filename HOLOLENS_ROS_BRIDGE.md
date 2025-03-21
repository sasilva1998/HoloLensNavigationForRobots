# HoloLens ROS Bridge

The purpose of this is to generate a connection between the HoloLens and ROS, in a way that the HoloLens would send data from its sensors.

## How to launch

The packages used in ROS are in the `linux` directory. Specifically the one that is needed is `hololens_ros_bridge`. That package should be installed in you workspace. Then follow the instructions:

1. Install the **MSRHoloLensSpatialMapping** app into the HoloLens as described in [Setup Instructions](Setup/SETUP.md).
2. Modify the configs in `hololens_ros_bridge/launch/holo_test.launch`.
3. Run the **MSRHoloLensSpatialMapping** app in the HoloLens.
4. Run in a terminal `roslaunch hololens_ros_bridge holo_test.launch`

Then you should have the pointcloud and transform of the HoloLens published.

## API reference documentation

### Published Topics

**/hololens/pc** ([sensors_msgs/PointCloud](http://docs.ros.org/en/lunar/api/sensor_msgs/html/msg/PointCloud.html))

        This is a pointcloud generated by the depth camera.
