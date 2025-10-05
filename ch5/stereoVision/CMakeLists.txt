cmake_minimum_required(VERSION 3.10)
project(StereoVisionProject)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenCV REQUIRED)
find_package(Pangolin REQUIRED)

add_executable(stereoVision stereoVision.cpp)

target_include_directories(stereoVision PUBLIC
    ${OpenCV_INCLUDE_DIRS}
    ${Pangolin_INCLUDE_DIRS}
)

target_link_libraries(stereoVision
    ${OpenCV_LIBS}
    ${Pangolin_LIBRARIES}
)
