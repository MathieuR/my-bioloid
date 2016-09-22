my-bioloid
==========

## rviz standalone
roslaunch bioloid_typea_description rviz.launch standalone:=true

## rviz with control boilerplate
roslaunch ros_control_boilerplate bioloid_simulation.launch
roslaunch ros_control_boilerplate bioloid_visualize.launch

## gazebo
# If the robot fall when play is pressed, make sure the control are started:
* install the library: sudo apt-get install ros-kinetic-gazebo-ros-control
* make sure the namespace of the spawned controller manager and the libgazebo in urdf are matching

# launch gazebi and wait for the controller to be started
* roslaunch bioloid_typea_gazebo gazebo.launch

# start the walking script
* rosrun bioloid_typea_gazebo walker_demo.py

