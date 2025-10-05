find_package(Pangolin REQUIRED)

add_executable(stereoVision stereoVision.cpp)
target_include_directories(stereoVision PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(stereoVision ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
