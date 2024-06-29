cmake_minimum_required(VERSION 3.0)
project(NumeriXCore)

# Set the source files
set(SOURCES
    # ex. src/test.cpp
)

# Set the include directories
include_directories(include)

# Add the library 
add_library(NumeriXCore STATIC ${SOURCES})

# Emscripten specific settings for building for WebAssembly
set_target_properties(NumeriXCore PROPERTIES
    COMPILE_FLAGS "-s WASM=1"
    LINK_FLAGS "-s WASM=1"
)