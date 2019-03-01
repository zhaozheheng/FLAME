cmake_minimum_required(VERSION 3.11)
project(FLAME)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)

set(SOURCE_FILES main.cpp posemapper.h lbs.h)
add_executable(FLAME ${SOURCE_FILES})

include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(FLAME ${OpenCV_LIBS})