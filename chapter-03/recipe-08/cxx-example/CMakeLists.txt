# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ch03-recipe08 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Boost 1.54 REQUIRED COMPONENTS filesystem)

add_executable(ch03-recipe08-cpp path-info.cpp)

target_link_libraries(ch03-recipe08-cpp
  PUBLIC
    Boost::filesystem
  )
