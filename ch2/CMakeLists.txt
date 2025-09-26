cmake_minimum_required (VERSION 2.8 )




add_executable useHello useHello.cpp
target_link_libraries( useHello hello_shared)
