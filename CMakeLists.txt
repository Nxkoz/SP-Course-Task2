cmake_minimum_required(VERSION 3.29)

project(task2)

set(CMAKE_CXX_STANDARD 20)

add_library(calculator STATIC src/calculator.cpp)
target_include_directories(calculator PUBLIC ${PROJECT_SOURCE_DIR}/include)
add_executable(task2 src/main.cpp)
target_link_libraries(task2 calculator)

set(CMAKE_MAKE_PROGRAM "ninja")
