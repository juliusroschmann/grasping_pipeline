cmake_minimum_required(VERSION 2.8.3)
project(grasping_pipeline)

find_package(catkin REQUIRED 
genmsg 
rospy
actionlib_msgs
geometry_msgs
#hsrb_interface_py
haf_grasping
sensor_msgs
#handover
object_detector_msgs
vision_msgs
#table_plane_extractor
#placement
v4r_util
)

## Generate actions in the 'action' folder
 add_action_files(
   DIRECTORY action
   FILES
   FindGrasppoint.action
   ExecuteGrasp.action
 )
## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
   std_msgs  
   actionlib_msgs
   geometry_msgs
   object_detector_msgs
 )

catkin_package()
include_directories()

