# c-glad-glfw-cmake-template

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
