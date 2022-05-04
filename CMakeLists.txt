cmake_minimum_required(VERSION 3.9.4)
project(calculationMatrixV12)

set(CMAKE_CXX_STANDARD 14)

set(CMAKE_CXX_STANDARD 11)

add_executable(calculationMatrix main.cpp calculation_cutoff_matrix.cpp calculation_matrix.h)

FIND_PACKAGE(OpenCV REQUIRED)
IF (OpenCV_FOUND)
    INCLUDE_DIRECTORIES(${OpenCV_INCLUDE_DIRS})
    TARGET_LINK_LIBRARIES(calculationMatrix ${OpenCV_LIBS})
ELSE (OpenCV_FOUND)
    MESSAGE(FATAL_ERROR "OpenCV library not found")
ENDIF (OpenCV_FOUND)

#find_library(OpenCV)
#find_package(OpenCV)

#include_directories(${OpenCV_INCLUDE_DIRS})


#target_link_libraries(untitled ${OpenCV_LIBS})