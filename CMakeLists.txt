cmake_minimum_required(VERSION 3.10)

project(KitcatDB VERSION 1.0 LANGUAGES C)

# Set the C standard 
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED True)

# Specify output directories
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../build)

# Include directories
include_directories(${PROJECT_SOURCE_DIR}/include)

# Collect source files automatically
file(GLOB SOURCES
    ${PROJECT_SOURCE_DIR}/src/*.c
)

# Create executable
add_executable(kitcat-db ${SOURCES})
