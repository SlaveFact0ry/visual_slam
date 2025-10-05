find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS})

find_package(Pangolin REQUIRED)

add_executable(joinMap joinMap.cpp)
target_include_directories(joinMap PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
