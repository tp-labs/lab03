cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(root)

add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

add_executable(example_s solver_application/equation.cpp)
add_executable(example_h hello_world_application/hello_world.cpp)

target_link_libraries(example_s solver_lib formatter_ex)
target_link_libraries(example_h formatter_ex)
