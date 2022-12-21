# CMake Tutorial

Simple tutorial for CMake and C++.

# Getting Started

Following this tutorial here: [CMake Tutorial - CMake 3.25.1 Documentation](https://cmake.org/cmake/help/latest/guide/tutorial/index.html)

1. Create a new folder and navigate inside: `my-cpp-project`
2. Create a new file called `main.cpp` and add a simple Hello World script:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!";
    return 0;
}
```

3. Create a new file called `CMakeLists.txt`:

```cmake
# Set a minimum version of CMake
cmake_minimum_required(VERSION 3.10)

# Name your project (no spaces)
# Version is optional
project(MyCppProject VERSION 1.0)

# Create an executable for your project
add_executable(MyCppProject main.cpp)
```

4. Create a `build` folder and navigate inside.
5. Generate a native build system for the project: `cmake ../`
   - This will default to whatever build system you have installed, like Visual Studio.
   - You could also run `cmake ../ -A x64` and get a Visual Studio solution
6. Now you can run the build: `cmake --build .`
   - You could also open the `.sln` file and run `Build Solution` for the same result.
7. Your `.exe` should be available in `build\Debug\`
8. Ideally you should make a `.gitignore` and add `build` to it.

## Set C++ version

Sets version to C++ 20:

```
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
```
