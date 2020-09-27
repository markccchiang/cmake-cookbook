# set minimum cmake version
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# project name and language
project(ch03-recipe05 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenMP REQUIRED)

INCLUDE_DIRECTORIES(/usr/local/opt/libomp/include)

add_executable(ch03-recipe05-cpp-02 example.cpp)

target_compile_options(ch03-recipe05-cpp-02
  PUBLIC
    ${OpenMP_CXX_FLAGS}
  )

set_target_properties(ch03-recipe05-cpp-02
  PROPERTIES
    LINK_FLAGS ${OpenMP_CXX_FLAGS}
  )

target_link_libraries(ch03-recipe05-cpp-02 ${OpenMP_CXX_LIBRARIES})