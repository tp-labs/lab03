cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(formatter)

set(SOURCES formatter.cpp)
set(HEADERS formatter.h)

add_library(formatter ${SOURCES} ${HEADERS})
target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
