cmake_minimum_required(VERSION 3.28.3)
project(RaycastPlatformer)

# Include headers

# Library
add_library(core
    lib/test.cpp
)
target_include_directories(core PUBLIC include)

# Add executable
add_executable(ray_plat
    src/main.cpp
)
target_link_libraries(ray_plat PRIVATE core)