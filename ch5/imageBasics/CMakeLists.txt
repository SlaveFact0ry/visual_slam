set( CMAKE_CXX_FLAGS "-std=c++14" )

find_package( OpenCV REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS })
message(STATUS "OpenCV version: ${OpenCV_VERSION}")
message(STATUS "OpenCV include dirs: ${OpenCV_INCLUDE_DIRS}")
message(STATUS "OpenCV libraries: ${OpenCV_LIBS}")
add_executable( imageBasics imageBasics.cpp)

target_link_libraries( imageBasics $ {OpenCV_LIBS} )
