cmake_minimum_required(VERSION 3.9 FATAL_ERROR)

project(ch03-recipe07 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenMP REQUIRED)

find_package(Eigen3 3.3 REQUIRED CONFIG)

if(TARGET Eigen3::Eigen)
  message(STATUS "Eigen3 v${EIGEN3_VERSION_STRING} found in ${EIGEN3_INCLUDE_DIR}")
endif()

add_executable(ch03-recipe07-cpp linear-algebra.cpp)

find_package(BLAS)

if(BLAS_FOUND)
  message(STATUS "Eigen will use some subroutines from BLAS.")
  message(STATUS "See: http://eigen.tuxfamily.org/dox-devel/TopicUsingBlasLapack.html")
  target_compile_definitions(ch03-recipe07-cpp
    PRIVATE
      EIGEN_USE_BLAS
    )
  target_link_libraries(ch03-recipe07-cpp
    PUBLIC
      ${BLAS_LIBRARIES}
    )
else()
  message(STATUS "BLAS not found. Using Eigen own functions")
endif()

target_link_libraries(ch03-recipe07-cpp
  PUBLIC
    Eigen3::Eigen
    OpenMP::OpenMP_CXX
  )
