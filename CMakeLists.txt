cmake_minimum_required(VERSION 3.22)
project(radius_icr_msgs)

# Default to C++17
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

find_package(std_msgs)
find_package(geometry_msgs)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/RadiusICR.msg"
  DEPENDENCIES std_msgs geometry_msgs
)

ament_package()
