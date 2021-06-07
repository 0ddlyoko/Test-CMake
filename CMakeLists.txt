cmake_minimum_required(VERSION 3.10.2)

# Project name & version
project(Stresser VERSION 2.0.1)

# C14
set(CMAKE_CXX_STANDARD 14)

configure_file(src/Base.hpp.in ${PROJECT_BINARY_DIR}/src/Base.hpp)


add_executable(${PROJECT_NAME}
        src/main.cpp
        src/Base.hpp.in
        src/Base.cpp
        )

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_BINARY_DIR})

