# set minimum cmake version
cmake_minimum_required(VERSION 3.9 FATAL_ERROR)

# project name and language
project(ch03-recipe05 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenMP REQUIRED)

add_executable(ch03-recipe05-cpp-01 example.cpp)

target_link_libraries(ch03-recipe05-cpp-01
  PUBLIC
    OpenMP::OpenMP_CXX
  )
