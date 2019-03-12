cmake_minimum_required(VERSION 2.8.12)

#project
project(app)

include_directories( ${MY_SOURCE_DIR}/../include)

set(CMAKE_CXX_STANDARD 11) 
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1y -Wall")
add_executable (app main.cc)
target_link_libraries (app sdll)

