cmake_minimum_required(VERSION 3.23.2)

project(PongGame VERSION 1.0)

add_executable(PongGame src/main.cpp src/Game/game.cpp src/Game/game.h)
add_subdirectory(deps/SDL/)

target_include_directories(
    PongGame PUBLIC deps/SDL/
)

target_link_directories(
    PongGame PRIVATE deps/SDL/
)

target_link_libraries(
    SDL2
)

set (CMAKE_CXX_FLAGS "-I/Library/Frameworks/SDL2.framework/Headers -F/Library/Frameworks -framework SDL2")