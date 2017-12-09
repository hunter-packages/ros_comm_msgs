cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
  URL "https://github.com/ruslo/hunter/archive/v0.21.19.tar.gz"
  SHA1 "5ead1e069b437930d0de8a21824b20fb52b37b50"
)

project(ros_comm)
hunter_add_package(catkin)
hunter_add_package(ros_message_generation)
hunter_add_package(ros_message_runtime)
hunter_add_package(ros_std_msgs)

add_subdirectory(rosgraph_msgs)
add_subdirectory(std_srvs)
