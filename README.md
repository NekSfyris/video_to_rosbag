# video_to_rosbag

A ROS package that takes as input a video file and makes it a rosbag under 'camera/color/image_raw' topic.

Has been tested for ros-kinetic and OpenCV 3.3.0 .

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

# rosbag_to_video

For the reverse function, meaning from rosbag to images, do (make sure to check the paths for your case in your launch file):
```
$ roslaunch video_to_rosbag rosbag_to_images.launch
```
