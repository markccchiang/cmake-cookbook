# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ch01-recipe03 LANGUAGES CXX)

# generate a library from sources
add_library(message
  STATIC
    Message.hpp
    Message.cpp
  )

add_executable(ch01-recipe03-cpp-01 hello-world.cpp)
target_link_libraries(ch01-recipe03-cpp-01 message)
