cmake_minimum_required(VERSION 3.13)

project(shell-starter-cpp)


# // this collects the matching files from src, into a variable
# // named SOURCE_FILES
file(GLOB_RECURSE SOURCE_FILES src/*.cpp src/*.hpp)

set(CMAKE_CXX_STANDARD 23) # Enable the C++23 standard

# CREATES AN EXECUTABLE TARGET NAMED SHELL USING THOSE FILES
add_executable(shell ${SOURCE_FILES})

target_link_libraries(shell PRIVATE readline)
# this tells the linker than shell needs the readline library