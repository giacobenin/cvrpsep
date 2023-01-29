cmake_minimum_required(VERSION 3.24)
project(bna LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)

#Necessary for shared library on Windows
if (MSVC)
    set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
endif()

add_library(cvrpsep SHARED)
target_include_directories(cvrpsep PRIVATE "${PROJECT_SOURCE_DIR}")
add_subdirectory("cvrpsep")

add_executable(bna)
target_sources(bna PRIVATE "bna/main.cpp")
target_link_libraries(bna PRIVATE cvrpsep)

install(TARGETS cvrpsep FILE_SET HEADERS)