cmake_minimum_required(VERSION 2.8.6)
project(Graph)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_definitions(-std=c++11)

find_package(Boost
        1.44.0                      # Minimum or EXACT version e.g. 1.36.0
        REQUIRED                    # Fail with error if Boost is not found
        # [COMPONENTS <libs>...]    # Boost libraries by their canonical name
)
include_directories("C:\\Libs\\boost_1_44_0")
set(SOURCE_FILES
    GraphCount/GraphCount/Graph.cpp
    GraphCount/GraphCount/Main.cpp
    GraphCount/GraphCount/Algorithm.cpp
    GraphCount/GraphCount/Algorithm.h)

add_executable(Graph ${SOURCE_FILES})