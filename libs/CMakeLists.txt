cmake_minimum_required(VERSION 3.0.0)
project(ogler-libs VERSION 0.1.0)

add_library(ogler-libs deps-maker.cpp)

add_subdirectory(glad/)
add_subdirectory(glm/)

target_link_libraries(ogler-libs PUBLIC glad glm)