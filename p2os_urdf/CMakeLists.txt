cmake_minimum_required(VERSION 2.8.3)
project(p2os_urdf)

find_package(catkin REQUIRED COMPONENTS geometry_msgs sensor_msgs std_msgs tf urdf kdl_parser)

catkin_package(
    CATKIN_DEPENDS tf urdf geometry_msgs sensor_msgs std_msgs kdl_parser
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

set(CMAKE_CXX_FLAGS "-std=c++11")

install(DIRECTORY 
   launch defs meshes models
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
 )
