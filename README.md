# Implementation notes

## My computer setting
* ubuntu 18.04 (melodic)

## eFast & eHarris [code](https://github.com/uzh-rpg/rpg_corner_events)

**How to run it**
```sh
$ roslaunch corner_event_detector bag.launch
$ rosbag play shapes_6dof.bag
```

**ERRORS**

```sh
Traceback (most recent call last):
  File "/opt/ros/melodic/lib/rqt_gui/rqt_gui", line 6, in <module>
    import rospkg
ModuleNotFoundError: No module named 'rospkg'
[rqt_gui_corners-5] process has died [pid 2762, exit code 1, cmd /opt/ros/melodic/lib/rqt_gui/rqt_gui --perspective-file /home/suhu/catkin_ws/src/corner_event_detector/cfg/viewers.perspective __name:=rqt_gui_corners __log:=/home/suhu/.ros/log/8be1dc26-bf97-11eb-b52f-3c7c3f511c73/rqt_gui_corners-5.log].
log file: /home/suhu/.ros/log/8be1dc26-bf97-11eb-b52f-3c7c3f511c73/rqt_gui_corners-5*.log
```

**Solution**

1. Goto /opt/ros/melodic/lib/rqt_gui/rqt_gui
2. change first line from `#!/usr/bin/env python` to `#!/usr/bin/env python2`

## ARC [code](https://github.com/ialzugaray/arc_star_ros)

**How to run it**
```sh
$ roslaunch arc_star_ros arc_star.launch
$ rosbag play shapes_6dof.bag
```

## Fa-Harris [code](https://github.com/ruoxianglee/fa_harris)

**How to run it**
```sh
$ roslaunch fa_harris corner.launch
$ roslaunch fa_harris corner.launch rosbag_flag:=1 rosbag_path=/path/to/ros_bag.bag
```
