cmake_minimum_required(VERSION 3.23.1)

project(sqlite
        VERSION 1.0
        LANGUAGES C)
	
file(GLOB SOURCES "src/*.c")

# Add a library with the above sources
add_library(${PROJECT_NAME} ${SOURCES})

target_include_directories( ${PROJECT_NAME}
    PUBLIC ${PROJECT_SOURCE_DIR}/include
)
