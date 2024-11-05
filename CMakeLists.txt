cmake_minimum_required(VERSION 3.25)

project(dctlib)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(dctlib STATIC lib/dctlib/src/dctlib.cpp)

target_include_directories(dctlib PUBLIC lib/dctlib/include)

add_executable(main main.cpp)

target_link_libraries(main PRIVATE dctlib)