################################################################################
# Set minimum required version of cmake, project name and compile options
################################################################################
cmake_minimum_required(VERSION 3.0.2)
project(multi_robot)
################################################################################
# Find catkin packages and libraries for catkin and system dependencies
################################################################################
find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  geometry_msgs
  nav_msgs
  roscpp
  sensor_msgs
  std_msgs
  tf
)
find_package(gazebo REQUIRED)
################################################################################
# Declare catkin specific configuration to be passed to dependent projects
################################################################################
catkin_package(
 CATKIN_DEPENDS gazebo_ros geometry_msgs nav_msgs roscpp sensor_msgs std_msgs tf
)
include_directories(
  include
  ${catkin_INCLUDE_DIRS}
  ${GAZEBO_INCLUDE_DIRS}
  ${SDFormat_INCLUDE_DIRS}
)
