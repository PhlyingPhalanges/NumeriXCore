# NumeriXCore

NumeriXCore is a high-performance numerical analysis library designed for various scientific and engineering applications. This library is implemented in C++ and can be compiled to WebAssembly using Emscripten, making it suitable for both native and web-based applications.

## Features

- Iterative Methods for Solving Equations
- Solutions of Systems of Linear Equations
- Handling of Special Matrices
- Solutions for Simultaneous Nonlinear Equations
- Computation of Eigenvalues and Eigenvectors
- Polynomial Interpolation and Approximation
- Numerical Integration Techniques
- Solutions to Initial and Boundary Value Problems for ODEs
- Finite Element Method

## Getting Started

### Prerequisites

- C++17 or higher
- CMake 3.0 or higher
- Emscripten (for WebAssembly build)

### Building the Library

1. **Clone the repository:**
    ```sh
    git clone https://github.com/PhlyingPhalanges/NumeriXCore.git
    cd NumeriXCore
    ```

2. **Create a build directory and navigate into it:**
    ```sh
    mkdir build
    cd build
    ```

3. **Run CMake to configure the project:**
    ```sh
    cmake ..
    ```

4. **Build the project:**
    ```sh
    make
    ```

### Building for WebAssembly

1. **Install Emscripten:** Follow the instructions on the [Emscripten website](https://emscripten.org/docs/getting_started/downloads.html).

2. **Activate the Emscripten environment:**
    ```sh
    source /path/to/emsdk/emsdk_env.sh
    ```

3. **Create a build directory and navigate into it:**
    ```sh
    mkdir build
    cd build
    ```

4. **Run CMake with Emscripten toolchain:**
    ```sh
    emcmake cmake ..
    ```

5. **Build the project:**
    ```sh
    emmake make
    ```

## Usage

Include the `NumeriXCore` library in your project and link it during the build process. Here is a simple example:

### C++

```cpp
#include <iostream>
#include "iterative_methods.hpp"

int main() {
    // Example usage of the library
    double result = simple_iteration([](double x) { return cos(x); }, 1.0, 1e-6);
    std::cout << "Root: " << result << std::endl;
    return 0;
}

## Acknowledgements

This library was developed with insights gained from various textbooks and academic resources on numerical analysis. Key references that informed the principles and methods applied in this library include:

- Süli, E., & Mayers, D. F. (2003). An Introduction to Numerical Analysis. Cambridge: Cambridge University Press.
- Another APA citation here once I find one

These resources provided a solid foundation in numerical methods, which was instrumental in the development of NumeriXCore.
