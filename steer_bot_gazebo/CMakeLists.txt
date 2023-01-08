cmake_minimum_required(VERSION 2.8.3)
project(steer_bot_gazebo)

find_package(catkin REQUIRED COMPONENTS 
roslaunch
roscpp
rospy
std_msgs
message_generation
geometry_msgs
)

catkin_package()

catkin_install_python(PROGRAMS
steer_teleop_key/teleop_key.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

if (CATKIN_ENABLE_TESTING)
    roslaunch_add_file_check(launch)
endif()
