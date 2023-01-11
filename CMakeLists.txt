cmake_minimum_required(VERSION 3.0.0)
project(minimal-imgui VERSION 0.1.0)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_FLAGS  "-Wall -Wextra -Wshadow -Wnon-virtual-dtor -pedantic -Werror")

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
list(APPEND CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake")

include_directories(include
include/backends)

set(SOURCES
    src/imgui_draw.cpp
    src/imgui_demo.cpp
    src/imgui_widgets.cpp
    src/imgui.cpp
    src/imgui_tables.cpp
    src/backends/imgui_impl_opengl3.cpp
    src/backends/imgui_impl_sdl.cpp
)

if(STATIC)
add_library(minimal-imgui ${SOURCES})
else() 
add_library(minimal-imgui SHARED ${SOURCES})
endif()

target_link_libraries(minimal-imgui PRIVATE
    SDL2::SDL2
    GLEW::glew
    ${OPENGL_LIBRARIES} ${GLUT_LIBRARY}
    )