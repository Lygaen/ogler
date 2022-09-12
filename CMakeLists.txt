cmake_minimum_required(VERSION 3.0.0)
project(ogler VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

include(CTest)
enable_testing()

file(GLOB_RECURSE SOURCES src/*.cpp include/*.h)
add_library(ogler ${SOURCES})
set_target_properties(ogler PROPERTIES LINKER_LANGUAGE CXX)

add_subdirectory(libs/)
target_link_libraries(ogler PUBLIC ogler-libs)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
