# oculus
Packages for Oculus Rift Development Kit 2.



citations
----------------
oculus_rviz_plugins
https://github.com/ros-visualization/oculus_rviz_plugins

ros_ovr_sdk
https://github.com/OSUrobotics/ros_ovr_sdk

rviz_fps_plugin
https://github.com/uos/rviz_fps_plugin
----------------

install OVR SDK
---
Extruct ovr_sdk_linux_0.5.0.1.tar.xz into 
oculus_pkg/ros_ovr_sdk/sdk/ovr_sdk_linux_0.5.0.1
---
$ make release
$ sudo make install
---

Oculus Rift + PS3 controller
----
Open 6 terminals.
$ sros
----
$ roscore
----
$ rosrun ros_ovr_sdk ovrd
!!!Be careful for the initial potision of Oculus Rift!!!
----
$ rosrun rviz_joy_control joy_control.py 
----
$ sudo chmod a+rw /dev/input/js0
$ rosrun joy joy_node
----
$ cd bag_files
$ rosbag play -l 2017-06-27-13-27-59.bag
----
$ rviz
----
Select FPS Motion from "+".
----

conecting motoman PC
$hello_motoman
(=$rosaddress client 192.168.2.100)
$rosaddress exit
