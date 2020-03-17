cmake_minimum_required(VERSION 2.8.3)
project(video_to_rosbag)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  sensor_msgs
  message_generation
  cv_bridge
  rosbag
)



generate_messages(
  DEPENDENCIES
    sensor_msgs
    std_msgs
)

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS
    sensor_msgs
    message_runtime
    std_msgs
    cv_bridge
    image_transport
    rosbag
)


include_directories(
  "include"
  ${catkin_INCLUDE_DIRS}
  ${OpenCV_INCLUDE_DIRS}
)

