cmake_minimum_required(VERSION 3.28.2 FATAL_ERROR)

project(ALS)

add_executable(ALS src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(ALS glfw)

add_subdirectory(external/glad)
target_link_libraries(ALS glad)