find_package(Pangolin REQUIRED)

add_executable(sereoVision stereoVision.cpp)
target_link_libraries(stereoVision ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
