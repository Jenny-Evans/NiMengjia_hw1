cmake_minimum_required(VERSION 3.10)

project(algebra-hw)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

include_directories(inc)

file(GLOB SOURCE_FILES "src/*.c")

add_executable(AlgebraProject ${SOURCE_FILES})

find_package(MATH_LIBRARY)
if(MATH_LIBRARY_FOUND)
    target_link_libraries(AlgebraProject ${MATH_LIBRARY})
endif()

target_compile_options(AlgebraProject PRIVATE -Wall)
