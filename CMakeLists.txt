cmake_minimum_required(VERSION 3.23)
project(GGL)

set(CMAKE_CXX_STANDARD 20)
set(SOURCE_FILES main.cpp)

add_executable(GGL_run ${SOURCE_FILES})

include_directories(factoriallib)
add_subdirectory(factoriallib)


target_link_libraries(GGL_run factoriallib_lib)

add_subdirectory(factoriallib_tests)
add_subdirectory(factoriallib_benchmarks)