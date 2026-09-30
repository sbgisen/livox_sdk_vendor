cmake_minimum_required(VERSION 3.14)
project(livox_sdk_vendor)

find_package(ament_cmake REQUIRED)
find_package(ament_cmake_vendor_package REQUIRED)

# ament_vendor only forwards CMAKE_BUILD_TYPE when it is defined.
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

ament_vendor(
  livox_sdk2_vendor
  VCS_URL
  https://github.com/Livox-SDK/Livox-SDK2.git
  VCS_VERSION
  c0796f04c143143899c87a773d9f6b7136453c0b
)

ament_package()
