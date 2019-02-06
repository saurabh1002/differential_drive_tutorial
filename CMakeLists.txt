cmake_minimum_required(VERSION 2.8.3)
project(differential_drive_tutorial)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  roscpp
  rospy
  std_msgs
  message_generation
)

find_package(geometry_msgs REQUIRED)
find_package(gazebo REQUIRED)

################################################
## Declare ROS messages, services and actions ##
################################################

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

###################################
## catkin specific configuration ##
###################################

catkin_package(
   DEPENDS gazebo_ros roscpp message_runtime
)

###########
## Build ##
###########

link_directories(${GAZEBO_LIBRARY_DIRS})
include_directories(${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS} ${GAZEBO_INCLUDE_DIRS})
include_directories(${geometry_msgs_INCLUDE_DIRS})

## Declare a C++ library
add_library(${PROJECT_NAME} src/main.cc)

## Specify libraries to link a library or executable target against
target_link_libraries(${PROJECT_NAME} ${GAZEBO_LIBRARIES} ${catkin_LIBRARIES})
