# CMake 최소 요구 버전 설정 (이전 경고 메시지 해결)
cmake_minimum_required(VERSION 3.10)

# 프로젝트 이름 설정
project(ImageBasicsProject)

# OpenCV 패키지 찾기
find_package(OpenCV REQUIRED)

# 실행 파일 타겟 생성
add_executable(imageBasics imageBasics.cpp)

# OpenCV 헤더 파일 경로를 타겟에 추가
target_include_directories(imageBasics PUBLIC ${OpenCV_INCLUDE_DIRS})

# OpenCV 라이브러리를 타겟에 링크
target_link_libraries(imageBasics ${OpenCV_LIBS})
