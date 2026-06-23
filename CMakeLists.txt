cmake_minimum_required(VERSION 3.28.3)
project(RaycastPlatformer)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add local SFML
add_subdirectory(third_party/SFML)

add_library(core
    lib/test.cpp
)
target_include_directories(core PUBLIC include)

# Add executable
add_executable(ray_plat
    src/main.cpp
)
target_link_libraries(ray_plat PRIVATE 
    core 
    SFML::Graphics
    SFML::Window
    SFML::System)