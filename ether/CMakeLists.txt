project(MyHello CXX)
cmake_minimum_required(VERSION 2.8)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()


include_directories("./include")

file(
    GLOB_RECURSE
    source_files
    src/*
)

add_executable(hello ${source_files})