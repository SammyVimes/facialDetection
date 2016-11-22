cmake_minimum_required(VERSION 3.6)
project(facialDetection)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
include_directories( ${OpenCV_INCLUDE_DIRS} )
FIND_PACKAGE( OpenCV REQUIRED core highgui objdetect video imgproc)
set(OpenCV_FOUND TRUE)

set(SOURCE_FILES
    config.cpp)

add_executable(facialDetection ${SOURCE_FILES})
target_link_libraries(facialDetection ${OpenCV_LIBS})