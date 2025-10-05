cmake_minimum_required(VERSION 3.10)

project(ImageBasics)

# OpenCV 패키지 찾기
find_package(OpenCV REQUIRED)

# 실행 파일 타겟 생성
add_executable(imageBasics imageBasics.cpp)
add_executable(undistortImage undistortImage.cpp)
# OpenCV 헤더 파일 경로를 타겟에 추가
target_include_directories(imageBasics PUBLIC ${OpenCV_INCLUDE_DIRS})
target_include_directories(undistortImagePUBLIC ${OpenCV_INCLUDE_DIRS})

# OpenCV 라이브러리를 타겟에 링크
target_link_libraries(imageBasics ${OpenCV_LIBS})
target_link_libraries(undistortImage${OpenCV_LIBS})
