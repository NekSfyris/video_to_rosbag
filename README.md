# video_to_rosbag

A ROS based package that takes as input a video file and makes it a rosbag under 'camera/color/image_raw' topic.

Has been tested for ros-kinetic and opencv 3.3.0 .

### Run

In first terminal:
```
$ roscore
```
Then in another terminal (first parameter is the video location, second is the output bag file name): 
```
$ cd ~/catkin_ws/src/video_to_rosbag
$ rosrun video_to_rosbag video_to_rosbag.py /home/nek/catkin_ws/src/video_to_rosbag/drone.avi rosbag_output
```
