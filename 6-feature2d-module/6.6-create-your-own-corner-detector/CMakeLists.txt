cmake_minimum_required(VERSION 2.8)


project(ownCornerDetector)


set(CUDA_USE_STATIC_CUDA_RUNTIME OFF)


find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})



add_executable(own main.cpp)


target_link_libraries( own ${OpenCV_LIBS})