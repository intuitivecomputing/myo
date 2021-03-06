# Requirements
 - python >=2.6
 - pySerial
 - [ascii_graph](https://pypi.python.org/pypi/ascii_graph) (for the [emg_ascii_graph.py](scripts/emg_ascii_graph.py) node)

# Topics and Messages
There are a few topics generated by the myo-rawNode.py node. These are:

1. /myo_raw/myo_arm - ros_myo/MyoArm message telling which arm and direction of X axis is (supposedly) worn.
2. /myo_raw/myo_emg - ros_myo/EmgArray message with the EMG readings.
3. /myo_raw/myo_gest - ros_myo/MyoPose message with the pose/gesture ID.
4. /myo_raw/myo_gest_str - std_msgs/String with the pose/gesture name.
5. /myo_raw/myo_imu - a standard IMU message with quaternion pose, accelerometer and gyro axes.
6. /myo_raw/myo_ori - Vector3 containing roll, pitch, yaw in radians.
7. /myo_raw/myo_ori_deg - Vector3 containing roll, pitch, yaw in degrees.
8. /myo_raw/vibrate - UInt8 topic to publish vibration to make, accepts values 1, 2, 3. The higher the value the longer the vibration.

Note that for the pose/gestures to be published you need to do the [sync gesture](https://support.getmyo.com/hc/en-us/articles/200755509-How-to-perform-the-sync-gesture) first. 

With all the node running.

```
roslaunch ros_myo bringup.launch
```
