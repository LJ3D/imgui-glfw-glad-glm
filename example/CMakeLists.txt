include(FetchContent)
cmake_minimum_required(VERSION 3.17)

project(example)

set(CMAKE_CXX_STANDARD 17)

set(BUILD_SHARED_LIBS OFF)
FetchContent_Declare(
        imgui-glfw-glad-glm
        GIT_REPOSITORY https://github.com/LJ3D/imgui-glfw-glad-glm
)
FetchContent_MakeAvailable(imgui-glfw-glad-glm)

add_executable(app main.cpp)

target_link_libraries(
        app
        imgui
        glm
)
