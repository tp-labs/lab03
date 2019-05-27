cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(homework)

add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

add_executable(hw hello_world_application/hello_world.cpp)
add_executable(solver solver_application/equation.cpp)

target_link_libraries(hw formatter_ex)
target_link_libraries(solver solver_lib formatter_ex)

