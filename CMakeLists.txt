cmake_minimum_required(VERSION 2.8.12)
#project name
PROJECT(testdll)

#SET_PROPERTY(GLOBAL PROPERTY USER_FOLDERS ON)
#SET_PROPERTY(TARGET fdll PROPERTY FOLDER "fdll")
#SET_PROPERTY(TARGET sdll PROPERTY FOLDER "sdll")
#SET_PROPERTY(TARGET app  PROPERTY FOLDER "app")

#head file path
INCLUDE_DIRECTORIES(
include
)

add_subdirectory(fdll)
add_subdirectory(sdll)
add_subdirectory(app)
