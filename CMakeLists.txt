cmake_minimum_required(VERSION 3.2)

project(OpenGL)

set(CMAKE_CXX_STANDARD 20)

add_executable(OpenGL src/glad.c main.cpp)

INCLUDE_DIRECTORIES(include)
link_directories(lib)
target_link_libraries(OpenGL ${PROJECT_SOURCE_DIR}/lib/libglfw.dylib)

#其中OpenGL为您的项目名称；${PROJECT_SOURCE_DIR}为固定语法，用于寻找项目路径；glad.c需要在main.cpp之前。
