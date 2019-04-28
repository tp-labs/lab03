cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(formatter_ex)

add_library(formatter_ex STATIC formatter_ex.cpp)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib ${CMAKE_CURRENT_BINARY_DIR}/formatter)
target_include_directories(formatter_ex PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(formatter_ex formatter)
