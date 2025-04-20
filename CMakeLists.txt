# Minimum CMake version required
cmake_minimum_required(VERSION 3.10)

# Project name
project(LeetCodeProblems)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)


add_library(leetcode_problems problems.h leetcode/lists.cpp)

# Include directories
target_include_directories(leetcode_problems PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

add_executable(run main.cpp)
target_link_libraries(run leetcode_problems)
