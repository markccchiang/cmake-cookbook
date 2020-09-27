# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ch02-recipe02 LANGUAGES CXX)

# define executable and its source file
add_executable(ch02-recipe02-cpp hello-world.cpp)

# let the preprocessor know about the system name
if(CMAKE_SYSTEM_NAME STREQUAL "Linux")
  target_compile_definitions(ch02-recipe02-cpp PUBLIC "IS_LINUX")
endif()
if(CMAKE_SYSTEM_NAME STREQUAL "Darwin")
  target_compile_definitions(ch02-recipe02-cpp PUBLIC "IS_MACOS")
endif()
if(CMAKE_SYSTEM_NAME STREQUAL "Windows")
  target_compile_definitions(ch02-recipe02-cpp PUBLIC "IS_WINDOWS")
endif()
