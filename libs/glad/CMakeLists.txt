cmake_minimum_required(VERSION 3.0.0)
project(glad VERSION 2)

add_library(glad src/gl.c include/glad/gl.h include/KHR/khrplatform.h)
target_include_directories(glad PUBLIC include/)