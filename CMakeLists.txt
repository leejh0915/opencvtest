#cmake_minimum_required(VERSION 3.22)
#project(opencvtest)
#
#SET(CMAKE_CXX_STANDARD 14)
#SET(CMAKE_CXX_STANDARD_REQUIRED YES)
#
#add_executable(test main.cpp)

cmake_minimum_required(VERSION 3.22)
project(opencvtest)
set(CMAKE_CXX_STANDARD 14)
include(ExternalProject)

ExternalProject_Add(OpenCV
        GIT_REPOSITORY https://github.com/opencv/opencv.git
        GIT_TAG 4.4.0
        INSTALL_COMMAND ""
        )

set(OpenCV_DIR ${CMAKE_BINARY_DIR}/opencv-build)

add_executable(opencvtest main.cpp)
