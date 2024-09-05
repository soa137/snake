cmake_minimum_required(VERSION 3.16)
project(
    snake
    VERSION 1.0
    DESCRIPTION "Snake game"
    LANGUAGES CXX
)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_BUILD_TYPE Debug)

find_package(Qt5 COMPONENTS Core REQUIRED)
find_package(Qt5 COMPONENTS Widgets REQUIRED)
set(sources
    ./src/snake.h
    ./src/snake.cpp
   ./src/main.cpp
)

add_executable(snake ${sources})

# target_link_libraries(test PRIVATE Qt5::Core ${LINK_FLAGS})
target_link_libraries(snake PRIVATE Qt5::Core Qt5::Widgets ${LINK_FLAGS})