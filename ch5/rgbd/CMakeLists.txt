cmake_minimum_required(VERSION 3.10)


find_package(OpenCV REQUIRED)
find_package(Sophus REQUIRED)
find_package(Pangolin REQUIRED)

add_executable(joinMap joinMap.cpp)
include_directories(${Sophus_INCLUDE_DIRS})

target_include_directories(joinMap PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
