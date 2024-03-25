# SD_Workspace
This package is required to operate the robot using ROS1 Noetic

## Initiate ROS

roscore

## You can remote access the Pi by sourcing these lines in ~/.bashrc or just running them as commands

export ROS_MASTER_URI=http://10.250.106.136:11311
export ROS_HOSTNAME=10.250.106.136

## run the teleop_keyboard node

rosrun teleop_twist_keyboard teleop_twist_keyboard.py

## run rosserial node cmd that connects to arduino and identifies it as a node

rosrun rosserial_arduino serial_node.py

## Intructions should pop up for keyobard controls once this run

## For testing purposes, you can also run a suscruber node that pastes the keyboard commands you did via teleop keyoboard 

rosrun teleop_twist_keyboard teleop_subscriber.py
