cmake_minimum_required(VERSION 3.31)

set(CMAKE_C_STANDARD 17)
include(FetchContent)

project(toy)

find_package(OpenGL REQUIRED)

FetchContent_Declare(
    glfw
    GIT_REPOSITORY https://github.com/glfw/glfw.git
    GIT_TAG 3.4
)
FetchContent_Declare(
        glad
        GIT_REPOSITORY https://github.com/Dav1dde/glad.git
        GIT_TAG 658f48e72aee3c6582e80b05ac0f8787a64fe6bb
        GIT_PROGRESS   TRUE
        SOURCE_SUBDIR  cmake
)
FetchContent_MakeAvailable(glfw glad)
glad_add_library(glad_gl_core_43 STATIC REPRODUCIBLE LOADER API gl:core=4.3)

add_executable(toy src/main.c)
target_include_directories(toy PRIVATE glad_gl_core_43 glfw)
target_link_libraries(toy PRIVATE glad_gl_core_43 glfw OpenGL::GL)
