# C-Glad-GLFW-Cmake-Template

This project template automatically configures glad, glfw, OpenGL with the C programming language and the cmake build system so you won't have to

# Using C++ instead

Make these configurations in order to switch the language to c++ instead of c

Change this line:
```cmake
set(CMAKE_C_STANDARD 17)
```
To probably something like this:
```cmake
set(CMAKE_CXX_STANDARD 20) # Or maybe 23
```

Rename the main file from main.c to main.cpp and then change the
```cmake
add_executable(toy src/main.c)
```
to match the cpp file instead
```cmake
add_executable(toy src/main.cpp)
```
Those are all the changes that need to be made

# Licensing & Dependencies
The dependencies used in this repository are **not** my own; each has its respective license, linked to its GitHub repository.

- [GLFW](https://github.com/glfw/glfw?tab=Zlib-1-ov-file) - Licensed under the zlib/libpng license (see `third_party/glfw_LICENSE.txt`).

- [GLAD](https://github.com/Dav1dde/glad/tree/glad2?tab=License-1-ov-file) - GLAD is released into the public domain under the CC0-1.0 license but includes some files under MIT/Apache 2.0. See their repository for more details and refer to the LICENSE here `third_party/glad_LICENSE.txt`
