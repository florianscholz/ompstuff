cmake_minimum_required(VERSION 3.5)
project(untitled)

#Enable OpenMP

find_package(OpenMP)
if (OPENMP_FOUND)
    set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
endif()

#Enable C++11

set(CMAKE_CXX_STANDARD 11)


set(SOURCE_FILES main.cpp)
add_executable(omptest ${SOURCE_FILES})