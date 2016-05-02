# icclab_turtlebot
Base scripts for the turtlebots at ICCLab.

NOTE DEPENDENCIES: 
- the rplidar model uses a mesh from the "hector_sensors_description" package, so you should have that installed
- the actual rplidar ROS node we're using allows us to stop the rotation motor, and it's here: https://github.com/negre/rplidar_ros.git

# TL;DR

In the launch directory you will find:
- minimal_with_rplidar.launch : launches the "minimal" turtlebot_bringup script + the rplidar node
- gmapping_icclab.launch : gmapping using the rplidar input on /scan topic instead of the kinect
- amcl_icclab.launch : amcl using the rplidar

In the base directory, the file 10-local.rules makes sure that when the rplidar is connected with 
USB it's given a consistent name through a symlink (/dev/rplidar) you should save the file in
/etc/udev/rules.d/10-local.rules on your turtlebot


