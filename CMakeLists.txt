cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

project(cmake-cookbook LANGUAGES C CXX)

# Chapter 1
add_subdirectory(chapter-01/recipe-01/c-example)
add_subdirectory(chapter-01/recipe-01/cxx-example)
add_subdirectory(chapter-01/recipe-02/c-example)
add_subdirectory(chapter-01/recipe-02/cxx-example)
add_subdirectory(chapter-01/recipe-03/cxx-example)
add_subdirectory(chapter-01/recipe-03/cxx-objlib-example)
add_subdirectory(chapter-01/recipe-04/cxx-example)
add_subdirectory(chapter-01/recipe-05/cxx-example)
add_subdirectory(chapter-01/recipe-06/example)
add_subdirectory(chapter-01/recipe-07/example)
add_subdirectory(chapter-01/recipe-08/cxx-example)
add_subdirectory(chapter-01/recipe-09/cxx-example)
add_subdirectory(chapter-01/recipe-10/cxx-example)

# Chapter 2
add_subdirectory(chapter-02/recipe-01/example)
add_subdirectory(chapter-02/recipe-02/cxx-example)
add_subdirectory(chapter-02/recipe-03/cxx-example)
add_subdirectory(chapter-02/recipe-04/cxx-example)
add_subdirectory(chapter-02/recipe-05/cxx-example)
add_subdirectory(chapter-02/recipe-06/cxx-example)

# Chapter 3
# recipe-01 ~ recipe-03: Python embedding
# recipe-04: Fortran embedding
add_subdirectory(chapter-03/recipe-05/cxx-example)
add_subdirectory(chapter-03/recipe-05/cxx-example-3.5)
# recipe-06: MPI
add_subdirectory(chapter-03/recipe-07/cxx-example)
add_subdirectory(chapter-03/recipe-07/cxx-example-3.5)
add_subdirectory(chapter-03/recipe-08/cxx-example)
# recipe-09: PkgConfig, libzeromq, libzmq, lib0mq
# recipe-10: ZeroMQ

# Chapter 4
# recipe-01: PythonInterp, BASH_EXECUTABLE
add_subdirectory(chapter-04/recipe-02/cxx-example)
