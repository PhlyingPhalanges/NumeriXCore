cmake_minimum_required(VERSION 3.0)
project(NumeriXCore)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)

# Set the source files
set(SOURCES
    src/approximation_2norm.cpp
    src/boundary_value_problems.cpp
    src/eigenvalues_eigenvectors.cpp
    src/finite_element_method.cpp
    src/initial_value_problems.cpp
    src/iterative_methods.cpp
    src/linear_systems.cpp
    src/nonlinear_systems.cpp
    src/numerical_integration_i.cpp
    src/numerical_integration_ii.cpp
    src/piecewise_polynomial_approximation.cpp
    src/polynomial_approximation_infinity.cpp
    src/polynomial_interpolation.cpp
    src/special_matrices.cpp
    src/utilities.cpp
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