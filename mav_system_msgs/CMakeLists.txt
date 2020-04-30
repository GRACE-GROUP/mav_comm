cmake_minimum_required(VERSION 2.8.3)
project(mav_system_msgs)

find_package(catkin REQUIRED message_generation std_msgs)
include_directories(include ${catkin_INCLUDE_DIRS})

add_definitions(-std=c++11)

add_message_files()

#add_service_files()

generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
