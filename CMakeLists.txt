cmake_minimum_required(VERSION 3.20)

message("Before 'project':")
message("  C: '${CMAKE_C_COMPILER}'")
message("  C++: '${CMAKE_CXX_COMPILER}'")

project(foo)

message("After 'project':")
message("  C: '${CMAKE_C_COMPILER}'")
message("  C++: '${CMAKE_CXX_COMPILER}'")

#if(POLICY CMP0038)
  # Policy CMP0038 introduced since CMake 3.0 so if we want to be compatible
  # with 2.8 (see cmake_minimum_required) we should put 'cmake_policy' under
  # condition.
  #cmake_policy(SET CMP0038 OLD)
#endif()

add_library(foo main.cpp)

message("Processing CMakeList")
message("Continue processing")