cmake_minimum_required(VERSION 3.00)
project(feature2d)

set(CMAKE_CXX_STANDARD 11)

set(CUDA_USE_STATIC_CUDA_RUNTIME OFF)

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIR})

add_executable(HarrisCorner HarrisCorners.cpp)

add_executable(ShiTomasi ShiTomasi.cpp)

target_link_libraries(HarrisCorner ${OpenCV_LIBS})
target_link_libraries(ShiTomasi ${OpenCV_LIBS})