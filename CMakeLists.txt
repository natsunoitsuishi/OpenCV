cmake_minimum_required(VERSION 4.0.0)
project(opencvProject)

set(OpenCV_DIR "${CMAKE_CURRENT_SOURCE_DIR}/opencv/build")

find_package(OpenCV REQUIRED)

add_executable(main main.cpp)
target_include_directories(main PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(main PRIVATE ${OpenCV_LIBS})