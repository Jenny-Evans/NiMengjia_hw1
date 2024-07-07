cmake_minimum_required(VERSION 3.10)

project(NiMengjia_hw1)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

include_directories(inc)

file(GLOB SOURCE_FILES "src/*.c")

add_executable(AlgebraProject ${SOURCE_FILES})
