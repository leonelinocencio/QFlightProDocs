# Qualcomm Flight Pro ROS Software

Nearly all of the ROS packages released for Qualcomm Flight are compatible with Qualcommm Flight Pro.  You simply need to add a cmake variable to your build command inside the docker container.

```
catkin_make -DCMAKE_BUILD_TYPE=Release -DQC_SOC_TARGET=APQ8096 install
```

inside your development docker container.  Note that you'll have to run ```source /opt/ros/indigo/setup.bash``` and also ```source devel/setup.bash``` after generating your msh headers (the first run of catkin_make).


Compatible packages:
* Vision Packages 
  * [snap_cam_ros](https://github.com/ATLFlight/snap_cam_ros)
  * [snap_dfs](https://github.com/ATLFlight/dfs-ros-example)
  * [snap_vio](https://github.com/ATLFlight/snap_vio)
  * [snap_msgs](https://github.com/ATLFlight/snap_msgs)
  * [snap_cpa](https://github.com/ATLFlight/snap_cpa)
  * [snap_cam_manager](https://github.com/ATLFlight/snap_cam_manager)  (ROS-independent)
* Other packages
  * [snap_imu](https://github.com/ATLFlight/snap_imu)
  * [qflight_descriptions](https://github.com/ATLFlight/qflight_descriptions)
  * [snav_ros](https://github.com/ATLFlight/snav_ros)
  * [snav_msgs](https://github.com/ATLFlight/snav_msgs)
  * [snav_fci](https://github.com/ATLFlight/snav_fci)  
