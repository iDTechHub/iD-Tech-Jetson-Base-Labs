cmake_minimum_required(VERSION 2.8.3)
project(motor_test)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  cv_bridge
  image_transport
)

catkin_package(
  CATKIN_DEPENDS roscpp rospy std_msgs cv_bridge image_transport
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(motor_test src/motor_test.cpp)
target_link_libraries(motor_test ${catkin_LIBRARIES})
