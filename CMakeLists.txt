cmake_minimum_required(VERSION 3.4...3.18)
project(example)

set(CMAKE_CXX_STANDARD 14)

find_package(pybind11 CONFIG REQUIRED)

add_library(example MODULE example.cpp)
target_link_libraries(example PRIVATE pybind11::module)
