cmake_minimum_required(VERSION 2.8.3)
project(adas_msgs)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  message_generation
rospy
  
)

add_message_files(
  FILES
  cluster_visualiser.msg
)


generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  DEPENDS 
    roscpp
)

catkin_package(
  CATKIN_DEPENDS 
    message_runtime
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)

