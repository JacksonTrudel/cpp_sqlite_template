# go into ./build and run: 
# to clean WITHIN ./build!! VERY DANGEROUS: `rm -rf *`
# `cmake -S ../. -B . && make && ./sqlite_example`
cmake_minimum_required(VERSION 3.23.1)

set (CMAKE_CXX_STANDARD 11)

project(sqlite_example 
        VERSION 1.0
        LANGUAGES CXX)

add_subdirectory(libs/sqlite)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME}
    sqlite
)
