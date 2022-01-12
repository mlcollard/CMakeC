# @file CMakeLists.txt
# 
# CMake files for the CProgram project

# Can be run by any version of CMake >= this
cmake_minimum_required(VERSION 3.22)

# Project info
project(CProgram)

# C standard
set(CMAKE_C_STANDARD 17)

# Assume all *.c source-code files
file(GLOB SOURCE "*.c")

# Application is based on .c file only
add_executable(CProgram ${SOURCE})
target_compile_options(CProgram PRIVATE -Wall)

# run command
add_custom_target(run $<TARGET_FILE:CProgram>)
