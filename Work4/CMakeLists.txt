cmake_minimum_required(VERSION 3.23)
project(Work4)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_EXE_LINKER_FLAGS "-static -static-libgcc")
set(SFML_STATIC_LIBRARIES TRUE)

set(CMAKE_CXX_STANDARD 20)

add_executable(Work4 main.cpp Pacman.cpp Pacman.h Entity.cpp Entity.h Game.cpp Game.h Ghost.cpp Ghost.h)

set(SFML_DIR "C:/Users/lyaho/CS_Projects/C++/lib/SFML/GCC 7.3.0 MinGW (SEH) - 64-bit/SFML-2.5.1/lib/cmake/SFML")
target_link_libraries(Work4 sfml-graphics)
set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules ")
find_package(SFML 2.5.1 REQUIRED graphics network audio system)