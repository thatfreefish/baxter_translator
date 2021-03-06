cmake_minimum_required(VERSION 2.8.3)
project(translator_driver)

find_package(catkin
  REQUIRED COMPONENTS
    roscpp
    rospy
    gazebo_ros
    gazebo_ros_control
    controller_manager
    baxter_core_msgs
)

# Depend on system install of Gazebo
# find_package(GAZEBO REQUIRED)
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GAZEBO_CXX_FLAGS}")

# find_package(Boost REQUIRED COMPONENTS system)

catkin_package(
  CATKIN_DEPENDS
  baxter_core_msgs
  gazebo_ros_control
  roscpp
  rospy
  controller_manager_msgs
)

catkin_python_setup()

# link_directories(
#   ${GAZEBO_LIBRARY_DIRS}
#   ${catkin_LIBRARY_DIRS}
# )

# include_directories(include
#   ${Boost_INCLUDE_DIR}
#   ${catkin_INCLUDE_DIRS}
#   ${GAZEBO_INCLUDE_DIRS}
# )

# add_library(baxter_gazebo_ros_control
#   src/baxter_gazebo_ros_control_plugin.cpp
# )

# target_link_libraries(baxter_gazebo_ros_control
#   ${catkin_LIBRARIES}
#   ${GAZEBO_LIBRARIES}
#   gazebo_ros_control
# )

