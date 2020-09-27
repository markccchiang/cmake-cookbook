# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ch04-recipe02 LANGUAGES CXX)

# require C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# example library
add_library(ch04-recipe02-sum_integers sum_integers.cpp)

# main code
add_executable(ch04-recipe02-sum_up main.cpp)
target_link_libraries(ch04-recipe02-sum_up ch04-recipe02-sum_integers)

# testing binary
add_executable(ch04-recipe02-cpp_test test.cpp)
target_link_libraries(ch04-recipe02-cpp_test ch04-recipe02-sum_integers)

# enable testing functionality
enable_testing()

# define test
add_test(
  NAME ch04-recipe02-catch_test
  COMMAND $<TARGET_FILE:ch04-recipe02-cpp_test> --success
  )
