cmake_minimum_required(VERSION 2.8.3)
project(barista_gazebo)

find_package(catkin REQUIRED COMPONENTS
  
  std_msgs
  message_generation
)

add_service_files(
  FILES
  SaveWaypoint.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)


catkin_package(
      CATKIN_DEPENDS
      rospy
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
