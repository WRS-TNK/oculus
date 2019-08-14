# oculus
Packages for Oculus Rift Development Kit 2.

# Build
### Install OVR SDK
```bash
$ cd oculus_pkg/ros_ovr_sdk/sdk/ovr_sdk_linux_0.5.0.1
$ make -j`nproc` release
$ sudo make install
```

### Build all packages
```bash
$ cd <catkin_ws>
$ catkin build
```

# Execute
Run `ros_ovr_sdk`.  
**!!! Be careful for the initial potision of Oculus Rift !!!**
```bash
$ rosrun ros_ovr_sdk ovrd
```

Then, run `joy_control` node.
```bash
$ sudo chmod a+rw /dev/input/js0
$ rosrun joy joy_node
$ rosrun rviz_joy_control joy_control.py 
```

After that, you can see Oculus view via Rviz.  
To do that, **Select FPS Motion from "+".**

# Citations
- oculus_rviz_plugins  
  https://github.com/ros-visualization/oculus_rviz_plugins
- ros_ovr_sdk  
  https://github.com/OSUrobotics/ros_ovr_sdk
- rviz_fps_plugin  
  https://github.com/uos/rviz_fps_plugin

