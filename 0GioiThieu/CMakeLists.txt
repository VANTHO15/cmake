# CMake Version
cmake_minimum_required(VERSION 3.29.3)

include(CMakePrintHelpers)
include(GCC.cmake)

set(CMAKE_TOOLCHAIN_FILE ${CMAKE_SOURCE_DIR}/GCC.cmake)

# Khai báo tên dự án
project(ThoNV_Project)

# Build the executable based on the source files
add_executable(main main.c)

target_include_directories(main PRIVATE 
    ${CMAKE_SOURCE_DIR}
    )

file(GLOB MY_SOURCE_FILE ${CMAKE_SOURCE_DIR}/Folder/*.c)

message("\n")

message("${MY_SOURCE_FILE}")

message("\n")

